# US Domestic Flight Cancellation and Diversion Analysis (2015)
### (Tableau Project)

# Introduction

## Data
This data comes from a Kaggle dataset, it tracks the on-time performance of US domestic flights operated by large air carriers in 2015.

- `flights.csv`: 274,964 flight records (rows) * 33 columns
- `airports.csv`: airports' information
- `cancel_reason.csv`: full-name of cancel reasons
- `airlines.csv`: full-name of airlines

# Data Analysis

## Cancellation

### Cancellation Reasons
There are three reasons for flight cancellations:
1.	Weather (54.07%)
2.	Airline/carrier (28.42%)
3.	National Air System (17.51%)
Although there is another reason, security, mentioned by the Kaggle website, it does not appear in the row data.

The top 3 airlines that have the most cancellations are:
1.	Southwest Airlines Co.
2.	Atlantic Southeast Airlines
3.	American Eagle Airlines Inc.

![Cancellation Reasons](1)

### Cancellation Rates
However, the top 3 airlines with the highest cancellation rate are a bit different:
1.	American Eagle Airlines Inc. (5.11%)
2.	Atlantic Southeast Airlines (2.94%)
3.	US Airways Inc. (1.95%)

![Cancellation Rates](2)

### Bad Weather Cancellations
Bad Weather has led to most cancellations, but the row data does not show whether they were affected by the weather of the departure or arrival airport.

This map only shows the departure airports of those cancelled flights. We can find that the flights departure from
1.	Dallas/Fort Worth International airport and
2.	Chicago O’Hare International airport
has been cancelled most, which were 231 and 217 in the whole year respectively.

![Bad Weather Cancellations Map](3)
![Bad Weather Cancellations](4)

## Diversion
### Airlines of Diverted Flights
Southwest Airlines Co. had the most diverted flight (181), which is almost two times than the second most Atlantic Southeast Airlines (99).
![Airlines of Diverted Flights](5)
![Diverted Rates](6)

However, the diverted rates of most airlines are similar.

### Destinations of Diverted Flights
The flights towards
1.	Hartsfield-Jackson Atlanta International Airport and
2.	Dallas/Fort Worth International Airport (mentioned above as having the most cancellations due to bad weather)
were diverted most, 57 and 56 respectively.
![Destinations of Diverted Flights Map](7)
![Destinations of Diverted Flights](8)

## Delay
### Total Delayed Time
1.  Southwest Airlines Co. had the longest delay time, which was 289,992 minutes, followed by
2.	Atlantic Southeast Airlines (187,908mins) and
3.	Skywest Airlines Inc.(166,148mins)
Delayed for Weather Reasons
The top 3 airports that had the longest delay time due to weather reasons were:
1.	Chicago O’Hare International Airport (24,381mins)
2.	Dallas/Fort Worth International Airport (16,276mins)
3.	Hartsfield-Jackson Atlanta International Airport (15,987mins)
![Total Delayed Time](10)
![Total Delayed Time](11)

### Delayed for Airline Reasons
1.  Southwest Airlines Co. had the longest delay time due to airline reasons (182,670mins), followed by:
2.	American Airlines Inc. (133,674mins) and
3.	Delta Air Lines Inc. (125,178mins)
![Delayed for Airline Reasons]()
![Delayed for Airline Reasons]()
12 13

### Delayed for Weather Reasons
1. Chicago O'Hare International Airport
2. Dallas / Fort Worth International Airport
3. Hartsfield-Jackson Atlanta International Airport
![Delayed for Weather Reasons]()
![Delayed for Weather Reasons]()
14 15

### Delayed for Security Reasons
The top 3 airport that had the longest delay time due to security reasons were:
1.	Dallas/Fort Worth International Airport (374mins)
2.	Phoenix Sky Harbour International Airport (362mins)
3.	Los Angeles International Airport (348mins)
![Delayed for Security Reasons]()
![Delayed for Security Reasons]()16 17

### Great Months for Flying
The trends were similar for both of them. There were the least cancellations, diversions delayed time in September 2015, followed by April. February and June were bad travel time in 2015.
![Great Months for Flying]()
![Great Months for Flying]()

### Great Days of Week for Flying
Saturday would be great for travel, while those who flighted on Monday had a larger chance to have bad experience in 2015.
![Great Days of Week for Flying]()
![Great Days of Week for Flying]()

# Design
In terms of maps, I found it might not be easy for readers to quickly get information regarding the numbers, but only using bar chart would lose important geographic information (for example, the map of cancellations for weather is similar to the one of destination of diverted flights). Thus, I put the bar chart at the bottom of each map for users’ convenience. The bar chart and map share a filter.

Thought bar chart is more accurate, I found it would be boring to always use it. Thus, I used bubble chart to show less important information (e.g. diverted rates).

5 reasons of delay are shown in row data. While weather and security delays might tell us which airport we could use less, the airline reasons would help us choose flight when planning a trip.

Some fly-in-and-fly-out persons fly on Monday and come back on Friday. Thus, I decided to explore whether there was a rule of the delayed flights during a week. Line Chart could provide a clear view of this rule.
