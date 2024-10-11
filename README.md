# ✈️ San Francisco Airport Passenger Dashboard
### Project Overview
This data projects aims to provide insights into the San Francisco Airport, specifically passenger traffic.


### Data Source

Data for this analysis has been taken from Kaggle 

[https://www.kaggle.com/datasets/rajsengo/sfo-air-traffic-passenger-and-cargo-statistics?select=Air_Traffic_Passenger_Statistics.csv](https://www.kaggle.com/datasets/rajsengo/sfo-air-traffic-passenger-and-cargo-statistics?resource=download&select=Air_Traffic_Passenger_Statistics.csv)


### Tools

- SQL Server - Data Cleaning and Analysis
- PowerBI - Data Analysis, Creating Dashboard


### Data Cleaning/Preparation

The dataset was quite clean, so I checked for missing values and adjusted date to the correct format.

```sql
SELECT  ROW_NUMBER() OVER(ORDER BY activity_period) as ID,
		activity_period,
		LEFT(activity_period, 4) as activity_year, 
		RIGHT(activity_period,2) as activity_month,
		operating_airline, 
		operating_airline_iata, 
		geo_summary, 
		geo_region, 
		activity_type, 
		price_category, 
		terminal, 
		boarding_area, 
		passenger_count
FROM Air_Traffic_Passenger_Statistics
WHERE operating_airline_iata IS NOT NULL


```

### Data Analysis

The data has been analyzed based on following questions:

1. 

### Results







✈️ ✈️ ✈️
