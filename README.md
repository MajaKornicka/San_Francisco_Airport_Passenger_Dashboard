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

1. Which airlines are the most popular?
2. What is the ratio of passengers flying low vs. other fare?
3. What is the ratio of domestic and international passenger traffic?
4. How did the traffic of passengers changed over the years?
5. What is the geographical region distribution like? Which continent generates the most traffic for the San Francisco Airport?
6. Which boarding areas are the most popular and is there correlation to the airport entrance for passengers?

### Results

<li> The dataset covered years 2005 - 2020 - during that time approx. 668 mln of passengers travelled through San Francisco Airport.

<li> 90 airlines are operating in this airport. The most popular one is definitely United Airlines (258 mln of passengers), next is SkyWest Airlines, American Airlines and Delta Air Lines. All of them are 
     american companies, which makes perfect sense in regards to the majority of the traffic being domestic traffic (77%).
	
<li> There is almost even split between arriving and departing passengers, with only 0,23% of passengers transiting through the airport. Since 2005 there has been almost steady increase in passenger 	 
     trafiic, with significant drop in 2020 - obviously the beginning of COVID 19 pandemic, which stopped traffic all over the world. The highest peak was noted in 2018 and 2019 - approx. 57 mln 
     passengers, in 2020 the numbers reached only 16 mln.

<li> As mentioned before, the majority of traffic is domestic, so inside United Stated. However when it comes to the international traffic the bigegst number of passengeres flies to or from Asia (9% of 
     total), Europe (6%) and Canada (3%).
<li> Only 16% of all passengers flies with low fare tickets.

<li> The analysis of boarding areas doesn't give us much information, as the San Francisco Airport is constructed very passenger friendly - all terminals are easily accesible from the underground 
     parking/buses/taxis area in the middle of the airport. Only boarding areas A and G are located little bit more conveniently close to the exit to the city. These areas are located in the International 
     Terminal. The biggest traffic is in the boarding areas F (terminal 3 - domestic flights) and G (international). Looking at the overview map of the airport boarding area F really seems to be the 
     biggest and the most extensive.




✈️ ✈️ ✈️
