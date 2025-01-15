# Weather and Football Information API

This project is a Node.js-based API that provides weather information, random dog facts, and football league standings using external APIs. It demonstrates asynchronous programming and RESTful API design while integrating third-party services.

## Table of Contents

1. [Features](#features)
2. [Setup Instructions](#setup-instructions)
3. [API Endpoints](#api-endpoints)
4. [Environment Variables](#environment-variables)
5. [Acknowledgments](#acknowledgments)

---

## Features

- Fetches current weather data for a specified city.
- Provides a random dog fact.
- Retrieves football league standings for La Liga (2023 season).
- Simple front-end hosting using Express's static file server.

---

## Setup Instructions

### Prerequisites

- Node.js (v16 or higher)
- npm (Node Package Manager)

### Steps

1. Clone the repository:

   ```bash
   git clone <repository-url>
   cd <repository-name>
   ```

2. Install dependencies:

   ```bash
   npm install
   ```

3. Set up environment variables:

   Create a `.env` file in the root directory and add the following:

   ```env
   WEATHER_API=<Your Weather API Key>
   FOOTBALL_KEY=<Your Football API Key>
   ```

   Replace `<Your Weather API Key>` and `<Your Football API Key>` with your respective API keys from [WeatherAPI](https://www.weatherapi.com/) and [API-Football](https://rapidapi.com/api-sports/api/api-football/).

4. Start the server:

   ```bash
   node index.js
   ```

5. Access the API:

   Open your browser or API client and navigate to `http://localhost:3000`.

---

## API Endpoints

### `/weather`

- **Method**: GET
- **Query Parameters**: `city` (required)
- **Description**: Fetches current weather details for the specified city along with a random dog fact.
- **Response Example**:

  ```json
  {
      "weather": {
          "temperature": 25.5,
          "description": "Partly cloudy",
          "icon": "//cdn.weatherapi.com/weather/...",
          "coordinates": {
              "lat": 51.51,
              "lon": -0.13
          },
          "feelsLikeTemperature": 27,
          "humidity": 60,
          "pressure": 1012,
          "windSpeed": 15.2,
          "countryCode": "GB",
          "rainVolumeLast3Hours": 0.5
      },
      "dog": ["Dogs can smell your feelings!"]
  }
  ```

### `/api/football`

- **Method**: GET
- **Description**: Fetches La Liga standings for the 2023 season.
- **Response Format**: Response format depends on the API-Football service.

---

## Environment Variables

The application uses environment variables to manage sensitive API keys. Ensure the following keys are set in your `.env` file:

- `WEATHER_API`: API key for WeatherAPI.
- `FOOTBALL_KEY`: API key for API-Football.

## Acknowledgments

- [WeatherAPI](https://www.weatherapi.com/) for weather data.
- [API-Football](https://rapidapi.com/api-sports/api/api-football/) for football league standings.
- [Dog Facts API](https://kinduff.github.io/dog-api/) for random dog facts.
