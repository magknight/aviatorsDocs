path: tree/master/docs/
source: acars.md

# ACARS
## What is it?
ACARS is a global network that allows aircraft to communicate with ATSUs (Air Traffic Service Units), their airline dispatch, Airport management and more. It can transmit text messages between facilities, with reply capability. More details on the real world system can be found at [SKYbrary](https://www.skybrary.aero/index.php/Aircraft_Communications,_Addressing_and_Reporting_System)
In the 787: Aviator's Edition, we've implimented a subset of the real ACARS features using the Hoppie network. Hoppie is a ACARS-esque web service managed by Jeroen Hoppenbrouwers, and intergrated into some VATSIM ATS (Air Traffic Service) clients (Such as the EuroScope TOPSKY, vSMR and UAC plugins). At the moment, we have implemented PDC/DCL and METAR/TAF/ATIS request. In the future, we may add full CPDLC and ADS-C capabilities based on the development of ATS clients and user uptake.

!!! tip
    Although Hoppie is not managed by any online networks, its PDC services are normally only available on VATSIM, due to the availability of ATCS clients that support it.


## Getting started
* Make sure you have a working 787: Aviator's Edition install with version **1.5.0** or later - The feature did not exist before the release of 1.5.0
* Navigate to the MFD COMM page using one of the MFD control panels, and select **MANAGER** in the top bar, then **ACARS** in the main menu
* Go to [Hoppie](https://www.hoppie.nl/acars/system/register.html) and request an ACARS logon code - it'll be emailled to you within 24h, although it is normally nearly instant. *The logon code expires after 120 days of inactivity - if this happens, just request a new one*
* Copy the 10-15 characther logon code from the email, and click the **PASTE** button on the MFD ACARS page
* Check the **ENABLE ACARS** box 
* Make sure you've entered a callsign into the CDU - when this is complete, the ACARS options should become active.
* You should now be good to go!

## Things you can do with ACARS
### Request a VATSIM ATIS
- Navigate to the MFD COMM page using one of the MFD control panels, and select **FLIGHT INFORMATION** in the top bar

!!! tip
    If this option is blue, check you've set a callsign in the CDU

- Click **ATIS REQUEST**
- Enter the ICAO code of the airport you would like an ATIS for
- Navigate to the **NEW MESSAGES** page to read your message
- When finished, click **EXIT** in the bottom right corner of the message page. *The message has not been deleted forever, just marked as read. You can find it in the **REVIEW**/**FLIGHT INFO UPLINKS...** page
- Now you've done that, the same methodology also applies to requesting a METAR or TAF

### Request a pre-departure clearance 
- Ensure you are at an airport that is providing Hoppie PDC/DCL
    - You can check the currently online facilities on the [Hoppie website](https://www.hoppie.nl/acars/system/log.html)

!!! tip
    Locations that commonly have VATSIM Hoppie services include EGKK, EGLL, EGCC, LOWW, EFHK, EDDF, EDDM, EDDH and EVRA

- Navigate to the MFD COMM page using one of the MFD control panels, and select **FLIGHT INFORMATION** in the top bar
- Click **DEPARTURE CLEARANCE REQUEST**
- Fill out the fields on the page

!!! tip
    ATC FACILITY is probably the ICAO code for your airport if service is provided by DEL/GND/TWR, or the ICAO FIR identifier for CTR-provided services

- Once complete, hit the SEND button. This sends your PDC/DCL request to the ATSU. Getting a response may take up to 5 mins during normal operations, or conciderably more during high-workload periods
- You will recieve a response, normally one of 2 types
    - "Unable, call on voice"
    - "Request recieved, standby"
    - Clearance
- Certain response fields are automatically uplinked to the aircraft systems for some pre-defined message types, such as frequencies and initial altitudes
- Once a clearance is recieved, and you have checked that you are able to comply with it, hit the ACCEPT button.
- When this is done, you can click **CANC**, located below the **MASTER WARNING** lights to clear the message from the PFD.