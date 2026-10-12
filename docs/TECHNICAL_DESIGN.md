# WeatherWhatIf – Technical Design Document

## 1. System Architecture

The current prototype uses a browser-based architecture.

1. **Presentation layer:** HTML and CSS display the interface.
2. **Input layer:** JavaScript validates the location, date, activity and time slots.
3. **Geocoding layer:** The Open-Meteo Geocoding API resolves a location into coordinates.
4. **Weather data layer:** The Open-Meteo Forecast API supplies hourly weather variables.
5. **Decision engine:** JavaScript rules calculate and compare risk indicators.
6. **Output layer:** The application displays forecast details, scores and a recommendation.

## 2. Workflow

User Input → Validation → Geocoding → Forecast Retrieval → Risk Calculation → Comparison → Recommendation.

## 3. Inputs

- Location
- Date
- Activity type
- First time slot
- Second time slot

## 4. Weather Variables

- Temperature
- Precipitation probability
- Precipitation amount
- Wind speed
- Weather code

## 5. Decision Logic

The prototype applies weighted rules to the weather variables. The resulting score is constrained to a range of 0–100. A lower score is treated as comparatively preferable.

The weights are illustrative and have not been validated against historical incidents or expert-defined safety thresholds.

## 6. Error Handling

The application checks for missing inputs, identical time slots, unknown locations and unavailable forecast data. It displays a message if a request fails.

## 7. Current Scope

This implementation is a frontend prototype. It does not currently include a Python Flask backend, persistent storage or live IMD warning integration.

## 8. Future Scope

- Add a backend service.
- Integrate verified official warning information where access is available.
- Validate decision rules against appropriate historical data and expert guidance.
- Expand automated testing and accessibility checks.

## 9. External Dependencies

- Open-Meteo Geocoding API
- Open-Meteo Forecast API

## 10. Limitations

Weather forecasts are uncertain. The application is for planning support and educational demonstration, not emergency guidance or a guarantee of safe conditions.
