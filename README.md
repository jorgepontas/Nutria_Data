# Analysis of Nutria Populations and Wild Sightings/Shootings in Germany

This repository contains an analysis of the nutria populations and the trends in wild sightings and shootings in Germany. The analysis is based on publicly available data sources and provides insights into the population trends of nutrias as well as changes in sightings and shootings over time.

## Data Sources

| Dataset                          | Description                                                  | Link                                                                         |
| -------------------------------- | ------------------------------------------------------------ | ---------------------------------------------------------------------------- |
| Nutria Populations               | Official nutria population data from BLE (Federal Agency for Agriculture and Food) | [BLE Nutria Population Data](https://www.ble.de/DE/Projekte/Aktuell/Projekte_Vorhaben/Integriertes-Pest-Management/Nutria-Monitoring/Nutria-Monitoring_node.html) |
| Wild Sightings and Shootings     | Data on nutria sightings and shootings                        | [DJV Wildtierportal](https://www.wildtierportal.de/)                         |

## Dataset Structures

### Nutria Populations

| Column      | Description                         |
| ----------- | ----------------------------------- |
| Year        | Year of data collection             |
| Region      | Region in Germany                   |
| Population  | Nutria population in the region     |

### Wild Sightings and Shootings

| Column      | Description                              |
| ----------- | ---------------------------------------- |
| Year        | Year of data collection                  |
| Region      | Region in Germany                        |
| Sightings   | Number of wild sightings of nutrias      |
| Shootings   | Number of nutrias shot by hunters        |

## Analysis Results

The analysis includes the following results:

1. Trend analysis of nutria populations in Germany.
2. Visualization of the geographic distribution of nutria populations.
3. Temporal trend of wild sightings of nutrias in different regions.
4. Temporal trend of nutria shootings by hunters.
5. Comparison of nutria populations with sightings and shootings to identify changes in population activity.

## Data Cleaning

The cleaning script (`cleaning_script.R`) demonstrates the code used for cleaning the raw data. The script removes missing values, corrects formatting issues, and performs other cleaning operations to prepare the data for analysis.

```R
# Load the "dplyr" package for data transformation
library(dplyr)

# Load the raw dataset
raw_data <- read.csv("raw_data.csv")

# Remove missing values
clean_data <- na.omit(raw_data)

# Perform additional cleaning operations
# ...

# Save the cleaned data
write.csv(clean_data, "clean_data.csv", row.names = FALSE)
```
## License

This project is licensed under the MIT License. For more details, please see the License File.
