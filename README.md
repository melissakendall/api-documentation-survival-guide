# API Documentation Survival Guide

In this repository, you will find resources used in the API Documentation: A Survival Guide presentation, including Swagger, Blueprint and RAML files.

# Table of Contents

- [API Documentation Survival Guide](#api-documentation-survival-guide)
- [Table of Contents](#table-of-contents)
  - [Dredd Demo](#dredd-demo)
    - [Requirements](#requirements)
    - [Steps](#steps)
  - [Testing ReDoc](#testing-redoc)

## Dredd Demo

### Requirements 

First ensure you have the following installed.

* [Node.js](https://nodejs.org/en/download/) 
  * These demos were done on v 10.16.0 on a Windows machine
* [Postman](https://www.getpostman.com/)
* [Dredd's Requirements](https://dredd.org/en/latest/quickstart.html)

### Steps

1. Install Dredd `npm install --global`
2. Import reference.raml into Postman
3. Create an example in postman for /TimeZones, using the below as a response

```json
[
    {
        "Id": "Alaskan Standard Time",
        "Name": "(UTC-09:00) Alaska",
        "SupportsDaylightSavingTime": true
    }
]
``` 

4. Create a Mock for the collection in Postman
5. Run Dredd

```
dredd reference.apib https:{{PostmanMockUrl}}.mock.pstmn.io/v1
```

Dredd will fail because the response returns headers that are not in the spec.

## Testing ReDoc

Open `index.html`.