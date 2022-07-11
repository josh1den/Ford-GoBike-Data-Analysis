# Ford GoBike Data Analysis
## by Josh Iden


## Dataset

> This data set includes information about individual rides made in a bike-sharing system covering the greater San Francisco Bay area. The dataset consists of 183,412 rows and 16 columns.

> Features included in this dataset:
- Duration of ride
- Start Time
- End Time
- Start Station & Location (Latitude & Longitude)
- End Station & Location (Latitude & Longitude)
- User Type (Subscriber or Customer)
- Member Birth Year
- Member Gender

> First, I inspected the data and found the following issues which required
attention:

1. Start/End trip time columns were in str format. Converted to datetime object.
2. Start/End station Id column was in float type, converted to integer.
3. Start/End station Id column contained null values which were determined inconsequential to the analysis and were left as is.
4. Member gender column contained null values. Replace nulls with "Not Given"
5. Member birth year column contained null values. Replaced nulls with None.

> Then performed the following transformations:


1. Created a day of week column
2. Created a categorical weekday/weekend column
3. Created an age column subtracting year of birth from the current year
4. Created a distance column based on the starting and ending geocoordinates
5. Created a minutes series based on distance given in seconds in order to gain a clearer insight of ride duration



## Summary of Findings

1. 89% of all rides were by Subscribers (regular riders). Customers (casual riders) account for 11% of all rides.
2. Males account for 71% of all rides.
3. Weekdays average nearly twice as many rides per day than weekends.
4. Customers averaged over 2x the duration of rides than subscribers, but only an average distance of 10.6% more than Subscribers, indicating that casual riders may take more time getting from one station to the next due to less rush or less familiarity with the route, station, or process.
5.	Females tend to ride bikes for great duration and distance than males
6.	Males are likelier than females to be Subscribers rather than Customers, and amongst riders who declined to provide a gender, those riders were far likelier to be Customers than Subscribers
7.	Surprisingly, although Weekends (Saturday and Sunday) have higher average ride duration than Weekdays, Weekend rides are on average actually actually  *shorter* in distance than Weekdays.



## Key Insights for Presentation

1. Weekdays are nearly twice as popular as weekends
2. Riders in their 30s and 40s ride fastest, followed by riders in their 20s and 50s tend on average to ride about the same speeds
2. Riders tend to be younger on the weekends than weekdays, supporting the evidence that the increase of ridership during the weekdays is due to riders using the bikes to commute to and from work or other weekday commitments.
