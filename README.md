# OpenAQ Data Ingest Pipeline 
[![Build Status](https://travis-ci.org/openaq/openaq-fetch.svg?branch=master)](https://travis-ci.org/openaq/openaq-fetch)

## Overview
This is the main data ingest pipeline for the [OpenAQ](https://openaq.org) project.

Starting with `fetch.js`, there is an ingest mechanism to gather global air quality measurements from a variety of sources. This is currently run every 10 minutes and saves all unique measurements to a database.

[openaq-api](https://github.com/openaq/openaq-api) powers the API and more information on the data format can be found in [openaq-data-format](https://github.com/openaq/openaq-data-format).

## Installing & Running
To run the API locally, you will need both [Node.js](https://nodejs.org) and [MongoDB](https://www.mongodb.org/) installed.

Install necessary Node.js packages by running

`npm install`

Make sure you have MongoDB running locally and then you can get help with

`node fetch.js --help`

For the above to work, you will need to have certain environment variables set as in the table below

| Name | Description | Default |
|---|---|---|
| INDIA_KIMONO_TOKEN | Token to be used for accessing Kimono API | not set |
| MONGOLAB_URI | Database URL | mongodb://localhost:27017/openAQ |
| SENDGRID_PASSWORD | Email service password | not set |
| SENDGRID_USERNAME | Email service username | not set |
| API_URL | URL of openaq-api | http://localhost:3004/v1/webhooks |
| WEBHOOK_KEY | Secret key to interact with openaq-api | '123' |

## Tests
To confirm that everything is working as expected, you can run the tests with

`npm test`

## Contributing
There are a lot of ways to contribute to this project, more details can be found in the [contributing guide](CONTRIBUTING.md). 
