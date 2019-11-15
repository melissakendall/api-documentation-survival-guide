# API Documentation Survival Guide

In this repository, you will find resources used in the API Documentation: A Survival Guide presentation, including Swagger, Blueprint and RAML files.

# Table of Contents

- [API Documentation Survival Guide](#api-documentation-survival-guide)
- [Table of Contents](#table-of-contents)
  - [Requirements](#requirements)
  - [Installation](#installation)

## Requirements

* Node.js
* Postman
* [Dredd](https://dredd.org/en/latest/quickstart.html)

## Installation

```npm install```

## Testing Out Dredd

```npm install --global```

* Import reference.raml into Postman
* Create an example for /TimeZones, using the below as a response

```json
[
    {
        "Id": "Alaskan Standard Time",
        "Name": "(UTC-09:00) Alaska",
        "SupportsDaylightSavingTime": true
    }
]``` 

* Create a Mock for the collection in Postman
* Run Dredd

```
dredd reference.apib https:{{PostmanMockUrl}}.mock.pstmn.io/v1
```

Notice it fails because of the additional headers received in postman.