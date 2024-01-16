# MuleSoft Google Maps System API Project README

Welcome to the MuleSoft Google Maps System API Project! This README provides essential information to help you set up and understand the integration with Google Maps APIs using MuleSoft.

## Overview

This MuleSoft project is designed to interact with the Google Maps APIs, providing seamless integration with Google Maps Platform. The project includes flows and configurations to perform common Google Maps operations like Address Validation, Geocodes Conversion, Places Search Using Text, Place Details Using PlaceId, Route Details and Distance Calculation.

## Table of Contents

1. [Getting Started](#getting-started)
    - [Prerequisites](#prerequisites)
    - [Installation](#installation)
2. [Configuration](#configuration)
    - [Environment Properties](#environment-properties)
3. [Usage](#usage)
    - [Executes A Salesforce Query](#executes-a-salesforce-query)
    - [Create/Update Salesforce Object](#createupdate-salesforce-object)
    - [Delete Salesforce Object](#delete-salesforce-object)
    - [Calls An Apex Service](#calls-an-apex-service)
    - [Calls Salesforce Composite API](#calls-salesforce-composite-api)
4. [Error Handling](#error-handling)
5. [Logging](#logging)
6. [API Collection](#api-collection)
7. [Contributing](#contributing)
8. [License](#license)

## Getting Started

### Prerequisites

Before using this MuleSoft project, ensure you have:

- MuleSoft Anypoint Studio installed.
- A Google Maps account with API key access and requisite features enabled.

### Installation

1. Clone the project repository:

   ```bash
   git clone https://github.com/yourusername/mulesoft-salesforce-system-api.git
   ```

2. Import the project into Anypoint Studio.

3. Configure the Google Maps connection and environment properties (details below).

## Configuration

Configure the Google Maps connection by setting this Github Actions Environment Secret - `GOOGLE_MAPS_API_KEY`

### Environment Properties

Adjust the environment properties in the `src/main/resources/properties/{env}.yaml` file as needed where `env` is either of local, qa, uat or prod.

## Usage

Please refer to Exchange 

### Executes A Salesforce Query

> Endpoint: **POST /query** <br/>
> Functionality: Executes and return the SOQL query response

### Create/Update Salesforce Object

> Endpoint: **PUT /object** <br/>
> Functionality:  Updates a salesforce object if exists, otherwise creates a new one

### Delete Salesforce Object

> Endpoint: **DELETE /object** <br/>
> Functionality:  Deletes a salesforce object

### Calls An Apex Service

> Endpoint: **POST /apex** <br/>
> Functionality: Makes a call to salesforce apex service

### Calls Salesforce Composite API

> Endpoint: **POST /composite** <br/>
> Functionality:  Makes a call to composite API of salesforce

## Error Handling

The project includes error handling mechanisms to gracefully handle Salesforce API errors. Refer to the exception strategies in the flows for details.

## Logging

Logging is configured to provide visibility into the flow execution. Check the logs in Anypoint Studio or the deployed application for troubleshooting.


## Contributing

We welcome contributions! If you find a bug or have a feature request, please open an issue or submit a pull request.

## License

This project is licensed under the [MIT License](LICENSE).
