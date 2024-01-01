# Convert Date Time Zone
## A simple Date Time conversion repo

[![Build Status](https://travis-ci.org/joemccann/dillinger.svg?branch=master)](https://github.com/nishanksalesforce/convert-date-time)

This is a simple repo to convert your dateTime with your specified timeZone. This code supports only UTC to GMT conversion, GMT to UTC conversion. You can also get the current date and time with the specific timezone. 

## Features

- Get current dateTime in ISO format in UTC or GMT.
- Convert dateTime from GMT to UTC and vice-versa.


## Usage

This git repo is hosted on heroku:

- [Host URL] - https://convert-date-time.herokuapp.com/
- [Path 1] - /dateTimeConversion
- [Path 2] - /getCurrentDateTime

Callout method supported - GET
## Examples

### 1. Convert Date from UTC to GMT

###### Endpoint: https://convert-date-time.herokuapp.com/dateTimeConversion?dateTime=2021-05-15T17:21:30.000Z&convertTo=Asia/Kolkata
#
#
| Param | Description | Required |
| ------ | ------ | ------ |
| dateTime | ISO formatted date to convert into GMT | Yes |
| convertTo | GMT timezone name  | Yes |


#### Correct Reponse 

```sh
{
    "success": true,
    "date": "2021-05-15",
    "time": "5:47 pm",
    "dateTime": "2021-05-15T17:47:08.213Z"
}
```

#### Incorrect Reponse 

```sh
{
    "success": false,
    "message": "Required field missing or Date not in proper ISO format."
}
```


### 2. Convert Date from GMT to UTC

###### Endpoint: https://convert-date-time.herokuapp.com/dateTimeConversion?dateTime=2021-05-15T17:21:30.000Z&convertTo=UTC&convertFrom=Asia/Kolkata
#
#
| Param | Description | Required |
| ------ | ------ | ------ |
| dateTime | ISO formatted date to convert into GMT | Yes |
| convertFrom | GMT timezone name  | Yes |
| convertTo | UTC  | Optional (Default UTC) |


#### Correct Reponse 

```sh
{
    "success": true,
    "date": "2021-05-15",
    "time": "11:51 am",
    "dateTime": "2021-05-15T11:51:30.000Z"
}
```

#### Incorrect Reponse 

```sh
{
    "success": false,
    "message": "Required field missing or Date not in proper ISO format."
}
```



### 3. Get Current Date Time in ISO Format

###### Endpoint: https://convert-date-time.herokuapp.com/getCurrentDateTime?convertTo=Asia/Kolkata
#
#
| Param | Description | Required |
| ------ | ------ | ------ |
| convertTo | UTC or any GMT timezone  | Optional (Default UTC) |


#### Correct Reponse 

```sh
{
    "success": true,
    "date": "2021-05-15",
    "time": "6:06 pm",
    "dateTime": "2021-05-15T18:06:24.322Z"
}
```

#### Incorrect Reponse 

```sh
{
    "success": false,
    "message": "Required field missing or Date not in proper ISO format."
}
```



## Params for Response

| Param | Description | 
| ------ | ------ | 
| success | Flag to show the response status of the callout  | 
| date | In YYYY-MM-DD format  | 
| time | In AM/PM format  | 
| dateTime | In ISO format  | 
| message | only when error occurs during callout  | 



## Development

This code is written on node js. Hosted on Heroku. 

## Build by
##### Nishank Gupta
#
#
**Free API, Enjoy CODING!**
