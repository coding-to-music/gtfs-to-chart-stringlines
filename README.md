# gtfs-to-chart-stringlines

# 🚀 Generate stringline charts from GTFS transit data 🚀

https://github.com/coding-to-music/gtfs-to-chart-stringlines

From / By https://github.com/BlinkTagInc/gtfs-to-chart


## Environment variables:

```java

```

## GitHub

```java
git init
git add .
git remote remove origin
git commit -m "first commit"
git branch -M main
git remote add origin git@github.com:coding-to-music/gtfs-to-chart-stringlines.git
git push -u origin main
```

## Typical usage

```shell
yarn install
yarn start
```

## create config-mbta.json

```json
{
  "agencies": [
    {
      "agency_key": "mbta",
      "url": "https://cdn.mbta.com/MBTA_GTFS.zip"
    }
  ],
  "sqlitePath": "/tmp/gtfs"
}
```

## create config.json using the config-sample.json 

```shell
cp config-sample.json config.json
```

## Install gtfs-to-chart globally

```shell
npm install gtfs-to-chart -g

gtfs-to-chart --version

2.0.6
```

## contents of config-sample.json

```json
{
  "agencies": [
    {
      "agency_key": "bart",
      "url": "http://www.bart.gov/dev/schedules/google_transit.zip"
    }
  ],
  "sqlitePath": "/tmp/gtfs"
}
```

## Running

```shell
gtfs-to-chart --configPath config.json
```

Output

```shell
Starting GTFS import for 1 file using SQLite database at /tmp/gtfs
Downloading GTFS from http://www.bart.gov/dev/schedules/google_transit.zip
Download successful
Importing GTFS from /tmp/tmp-141173-eank3fXmavG0/gtfs.zip
Importing - agency.txt - 1 lines imported
Importing - areas.txt - No file found
Importing - attributions.txt - No file found
Importing - calendar_dates.txt - 32 lines imported
Importing - calendar.txt - 13 lines imported
Importing - fare_attributes.txt - 2500 lines imported
Importing - fare_leg_rules.txt - No file found
Importing - fare_products.txt - No file found
Importing - fare_rules.txt - 2500 lines imported
Importing - fare_transfer_rules.txt - No file found
Importing - feed_info.txt - 1 lines imported
Importing - frequencies.txt - No file found
Importing - levels.txt - No file found
Importing - pathways.txt - No file found
Importing - routes.txt - 14 lines imported
Importing - shapes.txt - 38044 lines imported
Importing - stop_areas.txt - No file found
Importing - stop_times.txt - 61853 lines imported
Importing - stops.txt - 186 lines imported
Importing - transfers.txt - 41 lines imported
Importing - translations.txt - No file found
Importing - trips.txt - 4225 lines imported
Importing - calendar_attributes.txt - 11 lines imported
Importing - directions.txt - 14 lines imported
Importing - route_attributes.txt
Warning: Check route_attributes.txt for invalid data between lines 0 and 14.

file:///home/tmc/.nvm/versions/node/v16.19.1/lib/node_modules/gtfs-to-chart/node_modules/gtfs/lib/import.js:473
    throw error;
    ^
[  SqliteError: route_attributes.route_id
  
  - import.js:466 importLines
    [lib]/[gtfs-to-chart]/[gtfs]/lib/import.js:466:7
  
  - import.js:547 Parser.<anonymous>
    [lib]/[gtfs-to-chart]/[gtfs]/lib/import.js:547:11
  
  - node:events:513 Parser.emit
    node:events:513:28
  
  - readable:1358 endReadableNT
    node:internal/streams/readable:1358:12
  
  - task_queues:83 processTicksAndRejections
    node:internal/process/task_queues:83:21
  
] {
  code: 'SQLITE_CONSTRAINT_PRIMARYKEY'
}
```

## Contents of route_attributes.txt

```shell
route_id,category,subcategory,running_way
1,2,201,1
2,2,201,1
3,2,201,1
4,2,201,1
5,2,201,1
6,2,201,1
7,2,201,1
8,2,201,1
11,2,201,1
12,2,201,1
19,3,301,1
20,3,301,1
2,2,201,1
1,2,201,1
```

## Boston MBTA data

https://transitfeeds.com/p/mbta/64/latest

https://transitfeeds.com/p/mbta/64/latest/download

## create config-mbta.json

```json
{
  "agencies": [
    {
      "agency_key": "mbta",
      "url": "https://cdn.mbta.com/MBTA_GTFS.zip"
    }
  ],
  "sqlitePath": "/tmp/gtfs"
}
```

## Running

```shell
gtfs-to-chart --configPath config-mbta.json
```

Output

```shell
Starting GTFS import for 1 file using SQLite database at /tmp/gtfs
Downloading GTFS from https://cdn.mbta.com/MBTA_GTFS.zip
Download successful
Importing GTFS from /tmp/tmp-182845-5Sj01ZrXnN4T/gtfs.zip
Importing - agency.txt - 1 lines imported
Importing - areas.txt - 32 lines imported
Importing - attributions.txt - No file found
Importing - calendar_dates.txt - 54 lines imported
Importing - calendar.txt - 90 lines imported
Importing - fare_attributes.txt - No file found
Importing - fare_leg_rules.txt - 456 lines imported
Importing - fare_products.txt - 87 lines imported
Importing - fare_rules.txt - No file found
Importing - fare_transfer_rules.txt - 37 lines imported
Importing - feed_info.txt - 1 lines imported
Importing - frequencies.txt - No file found
Importing - levels.txt - 74 lines imported
Importing - pathways.txt - 7999 lines imported
Importing - routes.txt - 219 lines imported
Importing - shapes.txt - 258537 lines imported
Importing - stop_areas.txt - 758 lines imported
Importing - stop_times.txt - 1605036 lines imported
Importing - stops.txt - 9743 lines imported
Importing - transfers.txt - 5312 lines imported
Importing - translations.txt - No file found
Importing - trips.txt - 65139 lines imported
Importing - calendar_attributes.txt - 90 lines imported
Importing - directions.txt - 378 lines imported
Completed GTFS import for 1 agency
mbta: Generating charts [===================================----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------] 35/219
Warning: No trips found for route CR-Foxboro on May 5, 2023
mbta: Generating charts [============================================================================================================================-----------------------------------------------------------------------------------------------] 124/219
Warning: No trips found for route Shuttle-Generic-CommuterRail-South on May 5, 2023

Warning: No trips found for route Shuttle-Generic-CommuterRail-North on May 5, 2023

Warning: No trips found for route Shuttle-Generic-CommuterRail on May 5, 2023

Warning: No trips found for route Shuttle-Generic-Blue on May 5, 2023

Warning: No trips found for route Shuttle-Generic on May 5, 2023
mbta: Generating charts [===============================================================================================================================================================================--------------------------------------------] 175/219
Warning: No trips found for route 195 on May 5, 2023
mbta: Generating charts [============================================================================================================================================================================================-------------------------------] 188/219
Warning: No trips found for route Shuttle-JFKPark on May 5, 2023
mbta: Generating charts [==============================================================================================================================================================================================-----------------------------] 190/219
Warning: No trips found for route Shuttle-JFKKendall on May 5, 2023
mbta: Generating charts [=================================================================================================================================================================================================--------------------------] 193/219
Warning: No trips found for route Shuttle-GovernmentCenterWonderland on May 5, 2023

Warning: No trips found for route Shuttle-Generic-Worcester on May 5, 2023

Warning: No trips found for route Shuttle-Generic-Red-Trunk on May 5, 2023

Warning: No trips found for route Shuttle-Generic-Red-Braintree on May 5, 2023

Warning: No trips found for route Shuttle-Generic-Red-Ashmont on May 5, 2023

Warning: No trips found for route Shuttle-Generic-Red on May 5, 2023

Warning: No trips found for route Shuttle-Generic-Providence on May 5, 2023

Warning: No trips found for route Shuttle-Generic-Orange on May 5, 2023

Warning: No trips found for route Shuttle-Generic-Newburyport on May 5, 2023

Warning: No trips found for route Shuttle-Generic-Needham on May 5, 2023

Warning: No trips found for route Shuttle-Generic-Middleborough on May 5, 2023

Warning: No trips found for route Shuttle-Generic-Mattapan on May 5, 2023

Warning: No trips found for route Shuttle-Generic-Lowell on May 5, 2023

Warning: No trips found for route Shuttle-Generic-Kingston on May 5, 2023

Warning: No trips found for route Shuttle-Generic-Haverhill on May 5, 2023

Warning: No trips found for route Shuttle-Generic-Green-Trunk on May 5, 2023

Warning: No trips found for route Shuttle-Generic-Green-E on May 5, 2023

Warning: No trips found for route Shuttle-Generic-Green-D on May 5, 2023

Warning: No trips found for route Shuttle-Generic-Green-C on May 5, 2023

Warning: No trips found for route Shuttle-Generic-Greenbush on May 5, 2023

Warning: No trips found for route Shuttle-Generic-Green-B on May 5, 2023

Warning: No trips found for route Shuttle-Generic-Green on May 5, 2023

Warning: No trips found for route Shuttle-Generic-Franklin on May 5, 2023

Warning: No trips found for route Shuttle-Generic-Fitchburg on May 5, 2023

Warning: No trips found for route Shuttle-Generic-Fairmount on May 5, 2023

Warning: No trips found for route Shuttle-Generic-Elevator on May 5, 2023
mbta: Generating charts [===========================================================================================================================================================================================================================] 219/219

mbta: charts created at /home/tmc/ap/vol6/gtfs-to-chart-stringlines/charts/mbta
```


## Original README.md

<p align="center">
  ➡️
  <a href="#installation">Installation</a> |
  <a href="#quick-start">Quick Start</a> |
  <a href="#configuration">Configuration</a>
  ⬅️
  <br /><br />
  <img src="docs/images/gtfs-to-chart-logo.svg" alt="GTFS-to-Chart" />
  <br /><br />
  <a href="https://www.npmjs.com/package/gtfs-to-chart" rel="nofollow"><img src="https://img.shields.io/npm/v/gtfs-to-chart.svg?style=flat" style="max-width: 100%;"></a>
  <a href="https://www.npmjs.com/package/gtfs-to-chart" rel="nofollow"><img src="https://img.shields.io/npm/dm/gtfs-to-chart.svg?style=flat" style="max-width: 100%;"></a>
  <img src="https://img.shields.io/badge/License-MIT-yellow.svg">
  <br /><br />
  Generate stringline charts from GTFS transit data.
  <br /><br />
  <a href="https://nodei.co/npm/gtfs-to-chart/" rel="nofollow"><img src="https://nodei.co/npm/gtfs-to-chart.png?downloads=true" alt="NPM" style="max-width: 100%;"></a>
</p>

<hr>

`gtfs-to-chart` creates stringline charts showing all vehicles on a transit route from GTFS data.

[E.J. Marey](https://en.wikipedia.org/wiki/%C3%89tienne-Jules_Marey) was the first person to propose this type of graphical train schedule.

The chart generated shows stations across the x-axis, spaced to scale. Each line on the chart represents a transit vehicle moving through time. The slope of the line indicates speed at that point in the journey, with steeper slopes indicating slower speeds (as more time is passing as the vehicle moves). 

<img width="598" alt="SFMTA 14R Stringline Chart" src="https://user-images.githubusercontent.com/96217/87837133-6753cd80-c847-11ea-9df6-5807dbec9b20.png">

Try out some live interactive charts created  with GTFS-to-chart:

* [SFMTA Route 14R Pre-COVID-19](https://gtfs-charts.brendannee.vercel.app/sfmta-2020-03-10/14R.html)
* [SFMTA Route 14R Post-COVID-19](https://gtfs-charts.brendannee.vercel.app/sfmta-2020-07-21/14R.html)

* [SacRT Blue line Pre-COVID-19](https://gtfs-charts.brendannee.vercel.app/sacrt-2020-03-10/Blue.html)
* [SacRT Blue line Post-COVID-19](https://gtfs-charts.brendannee.vercel.app/sacrt-2020-07-21/Blue.html)


For routes that operate in two directions, both are shown on the same chart. Lines sloping downwards are vehicles heading one way and lines sloping upwards are vehicles heading in the reverse direction. The point at which lines cross indicates the exact time and location where two vehicles heading in the opposite direction pass each other.

If express service is offered on a route, the chart will show where express vehicles overtake non-express vehicles. This is shown where two lines sloped in the same direction cross.

If a vehicle has a scheduled stop with a different departure time than arrival time, the line will be vertical for a short distance at the stop representing the dwell time at the stop.

This library can be used to generate stringline charts for any transit agency that provides data in [GTFS format](https://developers.google.com/transit/gtfs/). To generate charts for a specific agency, just add the agency name and URL of the GTFS file in a `config.json` file as described below.

Not all transit routes work well with this type of visualization.

* Routes where not all trips follow the same pattern will not work well. For instance, a bus route that sometimes makes some different stops depending on the trip.
* Routes where one direction follows a different pattern than the other. For instance, a bus route that takes a completely different route on the way back.
* Circular routes do not currently work well, as the line jumps across the chart for the last stop.

Are you using `gtfs-to-chart`? Let us know via email (brendan@blinktag.com) or via opening a github issue or pull request if your agency is using this library.

## Credits

This library was based off of code developed by [Mike Bostock](https://observablehq.com/@mbostock/mareys-trains).

## Installation

If you would like to use this library as a command-line utility, you can install it globally directly from [npm](https://npmjs.org):

    npm install gtfs-to-chart -g

If you are using this as a node module as part of an application, you can include it in your project's `package.json` file.

## Quick Start

### Command-line example

    gtfs-to-chart --configPath /path/to/your/custom-config.json

### Code example

```js
import gtfsToChart from 'gtfs-to-chart';
import { readFile } from 'fs/promises';
const config = JSON.parse(await readFile(new URL('./config.json', import.meta.url)));

gtfsToChart(config)
.then(() => {
  console.log('Chart Generation Successful');
  process.exit();
})
.catch(err => {
  console.error(err);
  process.exit(1);
});
```

## Configuration

Copy `config-sample.json` to `config.json` and then add your projects configuration to `config.json`. This is a JSON file, so ensure that your config.json is valid JSON.

    cp config-sample.json config.json

All files starting with `config*.json` are .gitignored - so you can create multiple configuration files such as `config-caltrain.json`.

| option | type | description |
| ------ | ---- | ----------- |
| [`agencies`](#agencies) | array | An array of GTFS files to be imported. |
| [`beautify`](#beautify) | boolean | Whether or not to beautify the HTML output. |
| [`chartDate`](#chartdate) | string | The date to use for generating the stringline chart. |
| [`templatePath`](#templatepath) | string | Path to custom pug template for rendering chart html. |

### agencies

{Array} Specify the GTFS files to be imported in an `agencies` array. GTFS files can be imported via a `url` or a local `path`.

Each file needs an `agency_key`, a short name you create that is specific to that GTFS file. For GTFS files that contain more than one agency, you only need to list each GTFS file once in the `agencies` array, not once per agency that it contains.

To find an agency's GTFS file, visit [transitfeeds.com](http://transitfeeds.com). You can use the
URL from the agency's website or you can use a URL generated from the transitfeeds.com
API along with your API token.

* Specify a download URL:
```json
{
  "agencies": [
    {
      "agency_key": "county-connection",
      "url": "http://cccta.org/GTFS/google_transit.zip"
    }
  ]
}
```

* Specify a path to a zipped GTFS file:
```json
{
  "agencies": [
    {
      "agency_key": "myAgency",
      "path": "/path/to/the/gtfs.zip"
    }
  ]
}
```
* Specify a path to an unzipped GTFS file:
```json
{
  "agencies": [
    {
      "agency_key": "myAgency",
      "path": "/path/to/the/unzipped/gtfs/"
    }
  ]
}
```

* Exclude files - if you don't want all GTFS files to be imported, you can specify an array of files to exclude.

```json
{
  "agencies": [
    {
      "agency_key": "myAgency",
      "path": "/path/to/the/unzipped/gtfs/",
      "exclude": [
        "shapes",
        "stops"
      ]
    }
  ]
}
```

### beautify

{Boolean} Whether or not to beautify the HTML output. Defaults to `false`.

```json
"beautify": false
```

### chartDate

{String} The date to use for generating charts in YYYYMMDD format. Charts will be for service on this date. Defaults to today's date.

```json
"chartDate": "20200505"
```


### templatePath

{String} Path to a folder containing (pug)[https://pugjs.org/] template for rendering charts. This is optional. Defaults to using the templates provided in `views/chart`. All files within the `/views/custom` folder will be .gitignored, so you can copy the `views/chart` folder to `views/custom/myagency` and make any modifications needed. Any custom views folder should conatain pug templates called `chart_page.pug` and  `overview_page.pug`.

```json
"templatePath": "views/custom/my-agency/"
```

## Running

To generate charts, run `gtfs-to-chart`.

    gtfs-to-chart

By default, `gtfs-to-chart` will look for a `config.json` file in the project root. To specify a different path for the configuration file:

    gtfs-to-chart --configPath /path/to/your/custom-config.json

This will download the GTFS file specified in `config.js` .  Then, `gtfs-to-chart` will build the HTML charts and save them in `charts/:agency_key`.

### Options

`configPath`

Allows specifying a configuration json file. Defaults to config.json in the current directory.

    gtfs-to-chart --configPath /path/to/your/custom-config.json

`skipImport`

Skips importing GTFS into SQLite. Useful if you are rerunning with an unchanged GTFS file. If you use this option and the GTFS file hasn't been imported, you'll get an error.

    gtfs-to-chart --skipImport

## Processing very large GTFS files.

By default, node has a memory limit of 512 MB or 1 GB. Use the `max-old-space-size` option. For example to allocate 2 GB:

    node --max-old-space-size=2000 /usr/local/bin/gtfs-to-chart

## Contributing

Pull requests are welcome, as is feedback and [reporting issues](https://github.com/blinktaginc/gtfs-to-chart/issues).

### Tests

    npm test

