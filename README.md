# WeatherWhatIf – Weather Information & Decision Assistant

## Project Overview

WeatherWhatIf helps users compare possible time slots for outdoor activities, travel, sports and commuting using weather forecast data.

Users enter a location, date, activity and two time slots. The application retrieves hourly weather forecasts and uses rule-based scoring to identify the comparatively lower-risk option.

## Problem Statement

People often find it difficult to use weather forecasts to decide when to conduct outdoor events, travel or participate in other activities.

## Features

- Location-based weather forecast retrieval
- Comparison of two time slots
- Temperature, precipitation probability, rainfall and wind information
- Rule-based risk indicator
- Explanation of the recommended time slot
- Responsive web interface

## Technologies Used

- HTML
- CSS
- JavaScript
- Open-Meteo Geocoding API
- Open-Meteo Forecast API
- GitHub Pages for hosting

## Setup Instructions

1. Download or clone this repository.
2. Open `index.html` in a modern web browser.
3. Ensure an internet connection is available to retrieve weather data.
4. Enter a location, date, activity and two different time slots.
5. Click **Compare weather options**.

No API key is required for this prototype's Open-Meteo requests.

## Architecture

User Input → Input Validation → Location Geocoding → Weather Forecast Retrieval → Rule-Based Risk Scoring → Comparison → Recommendation Display.

## Decision Engine

The application evaluates forecast variables such as precipitation probability, rainfall, wind speed, temperature and thunderstorm-related weather codes. Activity-specific weights contribute to a risk indicator between 0 and 100.

The scores are illustrative decision-support indicators, not scientifically validated predictions of safety.

## Data Sources

- Open-Meteo: https://open-meteo.com/en/docs
- India Meteorological Department: https://mausam.imd.gov.in/

## Current Limitations

- Official IMD warning integration is not implemented.
- The prototype does not include a Flask backend or database.
- Risk-scoring rules require further validation and testing.
- Forecast data availability depends on the selected date and the API.

## Future Enhancements

- Integration of verified official weather warnings
- Backend services and improved data validation
- Expanded testing across locations and weather scenarios
- Further validation of decision rules

## License

This project is released under the MIT License. See the LICENSE file for details.

## Team

ACCI-SENCE
