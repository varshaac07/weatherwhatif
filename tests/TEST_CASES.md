# WeatherWhatIf – Test Cases

These are test scenarios. Record the actual outcome after running each test; do not mark a test as passed until it has been executed.

|  ID  |                               Test                             |              Expected behaviour               |

| TC01 | Enter Chennai and two different available forecast times       | Display weather data and compare both options |
| TC02 | Leave the location blank                                       | Display an input validation message |
| TC03 | Enter a location that cannot be found                          | Display a location-not-found message |
| TC04 | Select the same time twice                                     | Ask the user to choose different times |
| TC05 | Select a date outside the available forecast period            | Display a forecast-unavailable message |
| TC06 | Disconnect the internet before requesting a forecast           | Display an error message |
| TC07 | Compare a time slot with a thunderstorm-related weather code   | Include the thunderstorm rule in the risk calculation |
| TC08 | Open the page on a mobile-sized screen                         | Display a responsive layout |

## Sample Test Data

- Location: Chennai
- Activity: Outdoor event
- Option A: 09:00
- Option B: 17:00
- Date: A date within the available forecast period

Actual weather values vary by date and API response.

## Test Results

For each test, record:
- Actual result
- Pass or fail
- Date tested
- Notes or defects found
