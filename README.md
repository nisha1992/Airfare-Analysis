# Airfare-Analysis
Airfare Analysis using R and Excel

The purpose of this project is to analyze the change in Airfares over Date, Time, Festivals, Weekends or various other factors. 

# Tools Used
Excel, R, Google Flight QPX API


# Insights
Link : https://www.slideshare.net/nishachandrani/airfare-analysis
1. On same day and 1-2 Days Lag, frequency of flights are highest in the 8-9k fare range.
2. On 3-7 Days Lag, frequency of flights are highest in the 7-8k fare range.
3. On A week or more Lag, frequency of flights are highest in the 6-7k fare range.
4. During the festivals and the pre/post festivals weekends, average airfares seem to be
approx. 1.2x higher.
5. Average airfare on Sundays, Mondays and Saturdays are around 0.5x than the other
days.
6. Average airfare during morning (6 am) are highest.

# Fun Facts about Airlines
1. Airbus and Boeing has been characterized as a duopoly in the large jet airliner market since the
1990s.
2. Airbus is European while Boeing has its roots in United States.
3. Airbus planes have a curved and rounded nose, while the Boeing planes are round but slightly
pointed.
4. The Boeing 737 and Airbus A320 are two of the most popular single-aisle planes flying.
5. The Airbus A380 super-jumbo is a plane capable of ferrying from 550 to 800 passengers with its
two full-length decks and the promise of amenities such as sleeper cabins, cocktail lounges and a
gym.
6. Boeing has a 787 – Dreamliner to compete with A380.

# Project Description

# Data Overview
- Data collection Range: Data is available for dates from 28-09-2017 to 08-11-2017
- Data collected on a gap of 3 hours (starting 2 am) every day for next 15 days’ Flights. 
- Notes:
- Pricing details is available only for 3 airlines i.e. Jet Airways, Air India, Vistara. 
- Only DEL to BOM flights and vice versa considered. 
- No information about flights with stops. Only non-stop flights considered.

# Data Description
- Number of observations : 243557
- Number of variables : 10
- Independent Variables : 
- Type : Aircraft,  Carrier
- Time : Departure Time, Arrival Time, Duration, Date of Search, Time of Search
- Location : Source, Destination
- Dependent Variable : Airfare

# Outliers Analysis
Outliers can be calculated using Inter Quartile Range.

      Inter Quartile Range =  (8775 – 6067) = 2708
      Upper Outlier Range = 3rd Quartile + 1.5*IQR = 12,837
      Lower Outlier Range = 1st Quartile - 1.5*IQR = 2005

Around 7.8% of the prices are in the outlier range i.e  >12,837 INR. 
No Prices lie in the range of < 2005 INR
Most contribution towards Outlier fares are because of the less Lag 
(Number of days between search and departure). 
And it seems convenient too, since fares 
are less if we book in advance otherwise fares seem to surge as the departure date draws near.

# Feature Engineering
Feature Engineering is the art and science of selecting and/or generating the new independent variables from already present raw variables in a data table for more accurate Data Analysis.
1. Aircraft
2. Carrier
3. Location
4. Source
5. Destination
6. Departure Time (HH:MM:SS)
7. Arrival Time (Date + Time)
8. Duration (Flight Duration in minutes)
9. Date of Search (YYYY:MM:DD)
10. Time of Search (HH:MM:SS)
11. Departure Date (YYYY:MM:DD)
12. Departure Weekday (Monday, Tuesday and so on)
13. Search Weekday (Monday, Tuesday and so on)
14. Departure Time of Day (Late Night (12 am to 4 am), Morning (4 am to 12 pm ), Afternoon (12 pm to 17 pm),Evening (17 pm to 20 pm),Night (20 pm to 12 am)
15. Search Time of Day
16. Same as Departure Time of Day
17. Departure Date of Month (DD)
18. Departure Month of Year
19. Search Date of Month (DD)
20. Search Month of Year
21. Lag (Number of days between Search and Departure) (0-15 Days)(Same Day,1-2 Days,3-7 Days,A Week or more)
22. Weekday or Weekend Departure (Saturday and Sunday as Weekend)
23. Weekday or Weekend Search (Saturday and Sunday as Weekend)

# EDA & Visualization
![alt text](https://github.com/nisha1992/Airfare-Analysis/blob/master/AirfareoveAircrafts.png)
![alt text](https://github.com/nisha1992/Airfare-Analysis/blob/master/AirfaresoverAircrafts.png)
![alt text](https://github.com/nisha1992/Airfare-Analysis/blob/master/AirfarevsDepartTimeofDay.png)
![alt text](https://github.com/nisha1992/Airfare-Analysis/blob/master/AirfarevsDepartureDates.png)
![alt text](https://github.com/nisha1992/Airfare-Analysis/blob/master/AirfarevsDepartureTOD.png)
![alt text](https://github.com/nisha1992/Airfare-Analysis/blob/master/AirfarevsLag.png)
![alt text](https://github.com/nisha1992/Airfare-Analysis/blob/master/AirfarevsLagBoxplot.png)
![alt text](https://github.com/nisha1992/Airfare-Analysis/blob/master/AirfarevsWeekdays.png)
![alt text](https://github.com/nisha1992/Airfare-Analysis/blob/master/DeparturDatesvsAirfare.png)
![alt text](https://github.com/nisha1992/Airfare-Analysis/blob/master/SearchTODvsAirfare.png)
![alt text](https://github.com/nisha1992/Airfare-Analysis/blob/master/WeekdayendvsAirfare.png)



