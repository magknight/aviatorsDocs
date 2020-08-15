path: tree/master/docs/
source: extremeData.md

# Extreme airport data
Navigraph and company don't have access to the *extreme* airport data, which includes things like intersections and fancy runway lengths. We needed this for our EFB, so we made a format for it, detailed here:

## Airport files
Airport Data is stored in the ``./airportData``[^1] folder in the 787, in ``icao.json`` files, where icao is the 4 letter capitalised ICAO code for the airport (``EGKK.json``, ``EGLL.json`` etc.). 
Airport data files must conform to JSON specification - if one does not, it will be ignored
[^1]: For example, ``C:\X-Plane 11/Aircraft/Magknight787/airportData/``

### Structure
The example is Gatwick, because of course it is.
```json
EGKK.json
{
    "elevation": 203,
    "betterName": "London Gatwick",
    "meters": false,
    "dataSource": "NATS/UK AIP",
    "credits": "@Jacob W",
    "lastUpdated": "2020 07 27",
    "runways": [
        {
            "name": "26L",
            "heading": 258,
            "slope": 0.06,
            "tora": 10679,
            "toda": 11152,
            "asda": 10879,
            "lda": 9288,
            "lineupTurn": 90,
            "obstacles": [
                {
                    "height": 3,
                    "distance": 500,
                    "lateral": 0
                }
            ],
            "intx": [
                {
                    "name": "A1",
                    "distance": 371
                },
                {
                    "name": "B1",
                    "distance": 1175
                },
                {
                    "name": "C1",
                    "distance": 2595
                }
            ]
        },
        {
            "name": "08R",
            "heading": 78,
            "slope": -0.06,
            "tora": 10364,
            "toda": 10863,
            "asda": 10607,
            "lda": 9075,
            "lineupTurn": 90,
            "obstacles": [],
            "intx": [
                {
                    "name": "H1",
                    "distance": 748
                },
                {
                    "name": "G1",
                    "distance": 1237
                }
            ]
        },
        {
            "name": "26R",
            "heading": 258,
            "slope": 0.04,
            "tora": 8415,
            "toda": 8868,
            "asda": 8415,
            "lda": 7047,
            "lineupTurn": 90,
            "obstacles": [],
            "intx": []
        },
        {
            "name": "08L",
            "heading": 78,
            "slope": -0.04,
            "tora": 8415,
            "toda": 9974,
            "asda": 8415,
            "lda": 7389",
            "lineupTurn": 0,
            "obstacles": [],
            "intx": []
        }
    ]
}
```

### elevation
* Elevation above MSL in feet

### betterName
* A better name for the airport, if you don't like what the navdata normally gives

### meters
* Are distances in meters? If false, distances are in feet

### dataSource 
* Where did you get the data? 
    * Often it'd be the country AIP

### credits
* Names of people involved in the data preporation

### lastUpdated
* The date that the data was last validated/edited
* Format is ``yyyy mm dd`` - no other date formats are valid, because all other date formats are wrong.

### Runways
* JSON array containing all the runways for the airport

#### name
* The name of the runway:
* 08R, 26L, 25R, 36C, etc
* Runways are not to be named Steve, Sabrina or Deogee

#### Heading
* Magnetic heading of the runway

#### slope
* Slope of the runway in %

#### tora
* Take Off run available for the runway
* Feet or meters dependent on setting of ``meters`` globally

#### toda
* Take Off distance available
* Feet or meters dependent on setting of ``meters`` globally

#### asda
* Accelerate-Stop Distance Available
* Feet or meters dependent on setting of ``meters`` globally

#### lda
* Landing Distance Available
* Feet or meters dependent on setting of ``meters`` globally

#### lineupTurn
* Turn angle required for runway entry at full length
* If backtrack, then 180
* For a normal runway, 90
* Valid entrys are ``0,90,180``

#### obstacles
* Array of obstacles on the approach to the runway
* Not actually used for anything currently

#### intx
* Array of runway intersections

##### name
* common name of the intersection
* Normally a taxiway ID or holding point name

##### distance
* Distance from beginning of the runway
    * This isn't great, but it is better than nothing at all
* Feet or meters dependent on setting of ``meters`` globally
