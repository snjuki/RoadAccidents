# Road Accidents Analysis in Kenya 2012-2023

## Table of Contents

- [Project Overview](#project-overview)
- [Data Sources](#data-sources)
- [Recommendations](#recommendations)

### Project Overview

This data analysis project aims to provide insights into the road accidents causes and trends in Kenya between years 2012 to 2023. By analyzing the data as downloaded from the World Bank website, we are able to understands the various aspects of road accidents wiyh the aim of minimizing them.

### Data Sources

Sales Data: The primary dataset used for this analysis is the "road_crashes.csv" file, containing detailed information about each accident as reported on social media.

### Tools

- Excel - Data Cleaning
- Python-Extracting features- splitting date-time data into separate day, month, year columns.
- PowerBI - Creating reports


### Data Cleaning/Preparation

In the initial data preparation phase, we performed the following tasks:
1. Data loading and inspection.
2. Data cleaning and formatting.
3. Extracting features
```python
import pandas as pd
df=pd.read_csv(r'C:\Users\user\Downloads\KEN_2012-2023_RTC_v01_M_CSV\ma3route_crashes_algorithmcode.csv')
df['time'] = pd.to_datetime(df['crash_datetime']).dt.time
df['month'] = pd.to_datetime(df['crash_datetime']).dt.month
df['year'] = pd.to_datetime(df['crash_datetime']).dt.year
df.to_csv(r'C:\Users\user\Downloads\KEN_2012-2023_RTC_v01_M_CSV\Kenya_crashes.csv', index=False)
```

### Exploratory Data Analysis

EDA involved exploring the sales data to answer key questions, such as:

- What is the overall trends of road accidents over the years?
- Which periods are most prone to accidents: Month, Day of the week, Time of day?
- Which type of accidents produces highest percentage of fatalities: Matatu, MotorBike or Pedestrian
-On which roads and geographical area do most accidents happen.

### Data Analysis

![Road Crashes](https://github.com/user-attachments/assets/33e89bcb-0a67-4860-844a-09a894b32b57)



### Results/Findings

The analysis results are summarized as follows:
1. The number of road accidents have been reducing over the years.
2. The accidents with the highest fatality rates are those invoving pedestrians and Motor cycles.
3. Most Accidents happen on the month of December, Fridays and during 06:00 to 09:00 Hrs.
4. Geographically , most accidents happen in Nairobi CBD

### Recommendations

Based on the analysis, we recommend the following actions:
- Sensitize pedestrians and motor cycle riders on road safety to reduce fatalities.
- Drunken driving is likely to the reason why more accidents happen on Fridays-more enforcement is needed.
- Enhance Road Signage and Lighting at CBD 
-More accurate ,detailed and centralized accident data need to be captured by the authorities 

### Limitations
The data collected by World Bank was cloud-sourced from social media posts, this definitely affected the accuracy of the data as this is not an official source.


### References

 [World Bank Road Crashes data](https://bit.ly/4f1YBTP)

