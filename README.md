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
    - [Validate Address and its Components](#validate-address-and-its-components)
    - [Identify and Calculate Ideal Route Details](#identify-and-calculate-ideal-route-details)
    - [Convert Coordinates into Addresses and vice-versa](#convert-coordinates-into-addresses-and-vice-versa)
    - [Search for Places using Text](#search-for-places-using-text)
    - [Get Details of Place using Place Id](#get-details-of-place-using-place-id)
4. [Error Handling](#error-handling)
5. [Logging](#logging)
6. [API Collection](#api-collection)
7. [Contributing](#contributing)
8. [License](#license)

## Getting Started

### Prerequisites

Before using this MuleSoft project, ensure you have:

- MuleSoft Anypoint Studio installed.
- A Google Maps Platform account with API key access and requisite features enabled.

### Installation

1. Clone the project repository:

   ```bash
   git clone https://github.com/yourusername/medspeed-googlemaps-sapi.git
   ```

2. Import the project into Anypoint Studio.

3. Configure the Google Maps connection and environment properties (details below).

## Configuration

Configure the Google Maps connection by setting this Github Actions Environment Secret - `GOOGLE_MAPS_API_KEY`

### Environment Properties

Adjust the environment properties in the `src/main/resources/properties/{env}.yaml` file as needed where `env` is either of local, qa, uat or prod.

## Usage

Please refer to Exchange for [API Contract](https://anypoint.mulesoft.com/exchange/f015bd3e-6860-45a2-8012-1af3eec6fdba/medspeed-googlemaps-sapi)

### Validate Address and its Components

> Endpoint: **POST /validateAddress** <br/>
> Functionality: Validates an address and its components, standardize the address for mailing, and determine the best known geocode for it
> API reference: https://developers.google.com/maps/documentation/address-validation/reference/rest/v1/TopLevel/validateAddress

### Identify and Calculate Ideal Route Details

> Endpoint: **POST /routes** <br/>
> Functionality: Finds the ideal route from A to Z, calculates ETAs and distances for matrices of origin and destination locations, and also offers new features
> API reference: https://developers.google.com/maps/documentation/routes/reference/rest/v2/TopLevel/computeRoutes

### Convert Coordinates into Addresses and vice-versa

> Endpoint: **GET /geocode** <br/>
> Functionality: Converts addresses or Place IDs to latitude/longitude coordinates and vice-versa
> API reference:
> - https://developers.google.com/maps/documentation/geocoding/requests-geocoding
> - https://developers.google.com/maps/documentation/geocoding/requests-reverse-geocoding

### Search for Places using Text

> Endpoint: **POST /places** <br/>
> Functionality: Searches for place information based on a text search string
> API reference: https://developers.google.com/maps/documentation/places/web-service/text-search

### Get Details of Place using Place Id

> Endpoint: **GET /places/{placeId}** <br/>
> Functionality: Gets details about a particular establishment or point of interest
> API reference: https://developers.google.com/maps/documentation/places/web-service/place-details

## Error Handling

The project includes error handling mechanisms to gracefully handle Google Maps API errors. Refer to the exception strategies in the flows for details.

## Logging

Logging is configured to provide visibility into the flow execution. Check the logs in Anypoint Studio or the deployed application for troubleshooting.

## API Collection 

Please refer the below API collection link to explore the endpoint(s) in real time.
<br/><br/>
[<img src="https://run.pstmn.io/button.svg" alt="Run In Postman" style="width: 128px; height: 32px;">](https://medspeed-mulesoft-testing.postman.co/collection/32024449-dd84c206-3e48-4373-b22a-604c4966eadb?source=rip_markdown)

## Contributing

We welcome contributions! If you find a bug or have a feature request, please open an issue or submit a pull request.

## License

This project is licensed under the [MIT License](LICENSE).
