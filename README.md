# AirQloud Analysis

A Python library for analyzing data from IoT AirQo devices to provide insights on sensor health, device uptime, data completeness, and more.

## Installation

```bash
pip install airqloudanalysis
```

## Features

- Sensor health analysis
- Device uptime monitoring
- Data completeness metrics
- Battery performance analysis
- Support for device-specific and AirQloud-level analysis

## Usage

```python
import airqloudanalysis as aqa

# Initialize with your API token
token = "your_api_token"
for google sheets
file_path = "file path"

airQlouds = ["Kampala", "Nairobi"]
or 
deviceNames = ['aq_g4_95', 'aq_23']

start = "2023-01-01"
end = "2023-01-31"
maintenenceDate = date(2025, 3, 1)


# Get device data
df = aqa.airqloudlist_api(token, airQlouds)

# Process data for the specified date range
processed_data = aqa.process_data(df, start, end)

# Calculate uptime
uptime_data = aqa.calculate_uptime(processed_data, start, end)

# Create summary
device_time_diff = aqa.timeLastPost(df)
summary = aqa.create_summary_df(df, device_time_diff, uptime_data)

# Generate reports
summary_report = aqa.export_summary_csv_api(summary, airQlouds, [])
```

## Noticable changes to this library
Library version change
The library version holds various changes to the following functions;

### Calculate_uptime
Altered to use start and end date to fill in the null while computing the collective uptime  and now takes in two extra parameters: start and end date 
    Function call is calculate_uptime(dataframe df, string start, string end)

### Online devices list 
This provides a variation of the timeLastPost function providing a list of online devices, their device numbers, time difference, and the airqlouds they belong to
    Function call is onlineDeviceList(dataframe df):

### Offline devices list
This provides a variation of the timeLastPost function providing a list of offline devices, their device numbers, time difference, and the airqlouds they belong to
    Function call is offlineDeviceList(dataframe df):

## Full Documentation

For complete documentation and examples, please visit:
https://docs.google.com/document/d/1Dc4zQceYjoXDwmHKy99hp7x49kq8LtoSAXBA-1HMwA4/edit?usp=sharing

The repository for this library 
https://github.com/OlukaGibson/deviceAnalysisLibrary.git

## License

This project is licensed under the terms of the license included in the repository.

## Author

- AirQo - <gibson@airqo.net>
