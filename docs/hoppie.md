path: tree/master/docs/
source: hoppie.md
# Intergrating with Hoppie
The existing documentation for the Hoppie network is somewhat sparce, so here are some of my findings from developing the 787 ACARS features.

The live web server is at ``http://www.hoppie.nl/acars/system/connect.html``.
Most of my requests are handled by async GET requests. 
**Every** request should have logon code and callsign:
``connect.html?logon=${logonCode}&from=${callsign}``

## Requests
### VATSIM ATIS
```
type=inforeq
packet=vatatis+icao
```
such as 
```
type=inforeq
packet=vatatis+EGKK
```

### METAR
```
to=SERVER
type=inforeq
packet=metar+icao
```
such as 
```
to=SERVER
type=inforeq
packet=metar+EGKK
```

### TAF
```
to=SERVER
type=inforeq
packet=taf+icao
```
such as 
```
to=SERVER
type=inforeq
packet=taf+EGKK
```

### PDC/DCL
Pre-departure clearance is the other fairly simple thing to do, and it's supported by the majority of ATC clients. 
```
to=atcFacility
type=telex
packet=REQUEST PREDEP CLEARANCE
${callsign} ${acType} TO ${destinationIcao}
AT ${departureIcao} STAND ${stand}
ATIS ${atisLetter}
```
such as 
```
to=EGKK
type=telex
packet=REQUEST PREDEP CLEARANCE
TOM9AG B789 TO LEPA
AT EGKK STAND 49
ATIS Y
```

## Responses
To get the response to the request, assuming it isn't an inforeq, you need to POLL.
### Poll
To get messages from the server, you poll for them. Use a get request, and do it every 30 seconds (ish)
```
to=SERVER
type=poll
```
#### Things you might get as a response
```
ok {LOVV cpdlc {/data2/15//WU/CONTACT @WIEN SOUTH CTR@ @133.80}}
```
They come in the format of:
```
ok {${facility} ${type} {${packet}}} {${facility} ${type} {${packet}}} {${facility} ${type} {${packet}}}
```
If there are no messages, you'll just get a response of
```
ok 
```
Noting the space that comes after ``ok``.
This took me an absolute age to figure out, so my code for managing splitting the response into useful data is:

```lua
if result == "ok " then -- no messages there, just finish
    return true
end

if string.sub(result, 1, 3) == "ok " then -- if the result is still ok
    message = string.gsub(result, "^ok", "") -- get rid of the ok bit
    local messageTable = {}
    for row in string.gmatch(message, " {.-}}") do -- split by outer {}
        row = string.gsub(row, "{%d- ", "{") -- get rid of random numbers that show up
        from, type, packet = string.match(row, "{(%w-) (%w-) {(.-)}") -- split message to 3 var
        if packet ~= "" then -- if there is a packet, send it to the packet sorting stuff
            sortPacket(from, type, variable)
        end
    end
end
```