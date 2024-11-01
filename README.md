# Crime and Temperature Data Analysis

This project examines the relationship between weather conditions and crime rates. By analyzing temperature and crime datasets, we aimed to uncover potential correlations between climatic variables and crime occurrences. We employed various visualizations and statistical methods to better understand and interpret these relationships.

![Screenshot 2024-10-29 115352](https://github.com/user-attachments/assets/cdcbce8e-06cf-43ff-a7f6-e53dab83fd0b)

![Screenshot 2024-10-29 115517](https://github.com/user-attachments/assets/244827e0-78cc-470a-9370-29643bfbcce3)

![Screenshot 2024-10-29 115447](https://github.com/user-attachments/assets/1f96be7f-cda4-4a93-a825-2d92550dc168)

---

## Project Overview

This analysis explores two distinct datasets:
1. **Temperature Dataset** - Contains meteorological data such as temperature, wind speed, precipitation, and cloudiness.
2. **Crime Dataset** - Includes data on crime categories, outcomes, and the locations of offenses.

These datasets were analyzed individually and then combined to examine potential correlations between weather conditions and crime occurrences in Colchester.

---

## Methods and Analysis

### 1. **Data Preprocessing and Initial Analysis**

- Assigned the temperature and crime data to separate variables for independent analysis.
- Conducted frequency analyses using one-way tables (e.g., for wind speed in the temperature dataset) and two-way tables (e.g., for crime categories and outcomes).
- Created several visualizations to understand data distributions and relationships among variables:
  - **Histograms** for average air temperature.
  - **Density Plot** for wind gust speed distribution.
  - **Frequency Polygon Plot** for maximum air temperature.

### 2. **Exploratory Data Analysis (EDA)**

To interpret each dataset visually:
- **Box Plot**: Analyzed minimum temperature variations across wind directions.
- **Jitter Plot**: Explored dew point temperature and relative humidity, with additional smoothing to view trends in maximum temperature against sunshine duration.
- **Pair Plot**: Inspected relationships between minimum, maximum, and average temperatures, highlighting the stronger correlation between average and maximum temperatures.
- **Time Series Plot**: Examined maximum temperatures across months from January to December, by extracting the month from each date using the `lubridate` library.

### 3. **Crime Data Visualization**

- **Map Visualization**: Using `leaflet`, generated maps of Colchester to visualize crime distribution by location, displaying specific streets and crime types.
- **Bar Plot with Heat Colors**: Displayed counts of crimes by category for 2023.
- **Time Series Plot**: Illustrated monthly crime count variations in 2023.
- **Pie Chart**: Showcased the proportion of each crime category in Colchester for 2023.
- **Correlation Matrix**: Identified positive and negative correlations between variables, allowing us to observe feature dependencies.

### 4. **Combining Datasets for Correlation Analysis**

To explore the relationship between weather and crime:
- **Merged Datasets**: Combined temperature and crime datasets using the `date` column, adding the `month` field for monthly aggregation.
- **Correlation Analysis**: Correlated climate variables (e.g., visibility, wind speed, precipitation, cloudiness, and average temperature) with crime data. Average precipitation showed the strongest positive correlation with crime rates.

---

## Key Findings

Our analysis revealed a notable positive correlation between **precipitation levels** and the **number of crimes**. This suggests that higher precipitation may be associated with an increase in crime. Other weather factors, such as wind speed and temperature, also contributed to variations in crime counts, albeit to a lesser extent.

---

## Conclusion

This study underscores the importance of climate factors, particularly precipitation, in potentially influencing crime rates. Future studies could benefit from incorporating additional meteorological variables or expanding the geographical focus.

---

## Project Files

- **R Scripts**: Contains code for data manipulation and visualization.
- **Data Files**: Crime and temperature datasets used for analysis.
- **Figures**: Generated visualizations for each data relationship.

## Requirements

To run this analysis, ensure the following libraries are installed:

```R
install.packages(c("ggplot2", "dplyr", "lubridate", "leaflet"))
