# Airfare-Analysis
Airfare Analysis using R and Excel

The purpose of this project is to analyze the change in Airfares over Date, Time, Festivals, Weekends or various other factors. 

# Tools Used
Excel, R, Google Flight QPX API

# Data Overview
-> Data collection Range: Data is available for dates from 28-09-2017 to 08-11-2017
-> Data collected on a gap of 3 hours (starting 2 am) every day for next 15 days’ Flights. 
Notes:
-> Pricing details is available only for 3 airlines i.e. Jet Airways, Air India, Vistara. 
-> Only DEL to BOM flights and vice versa considered. 
-> No information about flights with stops. Only non-stop flights considered.

# Data Description
Number of observations : 243557
Number of variables : 10
Independent Variables : 
Type : Aircraft,  Carrier
Time : Departure Time, Arrival Time, Duration, Date of Search, Time of Search
Location : Source, Destination
Dependent Variable : Airfare

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
-> Type
  Aircraft
  Carrier
-> Location
  Source
  Destination
-> Time
  Departure Time (HH:MM:SS)
  Arrival Time (Date + Time)
  Departure Time of Day
    Late Night (12 am to 4 am)
    Morning (4 am to 12 pm )
    Afternoon (12 pm to 17 pm)
    Evening (17 pm to 20 pm)
    Night (20 pm to 12 am)
  Search Time of Day
    Same as Departure Time of Day
  Departure Date of Month (DD)
  Departure Month of Year
  Search Date of Month (DD)
  Search Month of Year
  Lag (Number of days between Search and Departure) (0-15 Days)
    Same Day
    1-2 Days
    3-7 Days
    A Week or more
  Weekday or Weekend Departure (Saturday and Sunday as Weekend)
  Weekday or Weekend Search (Saturday and Sunday as Weekend)
  Duration (Flight Duration in minutes)
  Date of Search (YYYY:MM:DD)
  Time of Search (HH:MM:SS)
  Departure Date (YYYY:MM:DD)
  Departure Weekday (Monday, Tuesday and so on)
  Search Weekday (Monday, Tuesday and so on)

# EDA & Visualization


