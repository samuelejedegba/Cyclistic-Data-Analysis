# Cyclistic-Data-Analysis

![](https://github.com/samuelejedegba/Cyclistic-Data-Analysis/blob/main/Intro_image.jpg)

## Introduction
In 2016, Cyclistic launched a successful bike-share offering. Since then, the program has grown to a fleet of 5,824 bicycles that are geo-tracked and locked into a network of 692 stations across Chicago. The bikes can be unlocked from one station and returned to any other station in the system.
There are two types of cyclists that use Cyclistic Bike-share services; Those who purchase casual tickets known as “Casual Riders” and those who purchase annual memberships known as “Members.” The marketing team believes that maximizing the number of annual members will be key to future growth. Rather then creating a marketing campaign that targets new customers, there is a good chance to convert casual riders into members.

**_Disclaimer_** : This project was undertaken after the completion of my google data analytics programme.

## Problem Statement
1. What is the most effective marketing strategy of converting Cyclistic’s casual riders to annual memberships
2. How do annual members and casual riders use Cyclistic bikes differently?

## Skills/Concepts Demonstrated:
- Excel
- SQL
- Power BI

## Dataset
The dataset was aquired from [here](https://divvy-tripdata.s3.amazonaws.com/index.html) . I downloaded from March 2022 to February 2023 for this analysis.

## Cleaning and Analysis
**Step 1** - **Importing Dataset**

This being my first big project created some issues in my data cleaning and analysis project. First, I wanted to perform all my analysis and cleaning on Power BI. But I discovered how easy this could be done on SQL and so I proceeded to use it. The first realisation I came to was that I had learnt a lot of SQL codes, using an inbuilt schema, so I had to learn to import files into my SQL. This was easy enough but this dataset was CSV, which meant I had to import it as a flatfile. I did this and kept getting errors. Because I was pressed for time to complete this analysis, I did not want to investigate these errors, so instead I converted all 12 CSV files to Excel and imported them into my SQL. It worked! I did not get any error message.

_PS_ - I have investigated why I kept getting errors and I can now import flat files into my SQL

**Step 2** - **Joining Dataset**

![](https://github.com/samuelejedegba/Cyclistic-Data-Analysis/blob/main/Joining_Tables.PNG)
I ran the above query to Join the dataset. Looking at the it closely, one would realise 'Cyclistic 9' has a different query from the others. This was because I kept encountering another problem I was not used to. For some reason, one of the columns in the that table had a different data type from its counterpart columns. The error message 'Msg 8114, Level 16, State 5, Line 1 Error converting data type nvarchar to float.' kept showing up. It took me a while to figure it out, but I did. In my 'Union Query', I converted the column from 'Float' to 'Nvachar.' That worked as well and I ended up with one very large dataset.

**Step 3** - **Creating Smaller Tables**

1[](https://github.com/samuelejedegba/Cyclistic-Data-Analysis/blob/main/Creating%20Tables%201.PNG)
The above set of queries was done to create smaller tables with important information needed for the analysis. I created the following:
1. A table with the total number of rides in the year using 'Count' Function.
2. A table with total number of rides for Members and Casuals using 'Count' function and 'Group By' statement.
3. The ride time in minutes in of each rider in the entire dataset, using 'datediff' function and subracting the start time of each ride to the end time.
4. The total ride time of Member Riders and Casual Riders, using the 'Sum' function and the 'Group By' Command.
5. A table with the total ride time in minutes, but grouped into days of the week using the 'Datename', 'DatePart' and 'Datediff' functions.
6. A table with the type of riders (Members and Casuals) and the weekday they use the service using 'Count' Function and the 'Group by' and 'Order by' statements.
![](https://github.com/samuelejedegba/Cyclistic-Data-Analysis/blob/main/Creating_tables_2.PNG)
Step 3 continues with the above set of queries. I created the following:
1. A table with each type of rider with the ride time in minutes using 'Count' functions and 'Group by' and 'Order by' statements.
2. 2 tables with the average number of rides per day. One for Member riders and the other for Casual riders using the 'AVG' function.
3. 2 tables with the total number of rides per bike type. One for Member riders and the other for Casual riders using the 'Count' function and the 'Group by' statement.
![](https://github.com/samuelejedegba/Cyclistic-Data-Analysis/blob/main/creating_tables_3.PNG)
Final part of Step 3 in the above image. I created a table with the total ride time (in minutes) per month for casual and member riders. This was to determine the month with the longest rides.

**Step 4** - **Exporting my Tables**

When I had issues combining my dataset into one large dataset, I thought of many solutions. I thought of combining them on Excel or Power Query before importing it into SQL for my cleaning and manipulation. But with the number of rows in the combined dataset (over 5 million) that was not possible as Excel has a limit to obeservations it can take. This meant exporting to excel would also be a problem. I had to take my dataset straight to Power BI which was another thing I had not learnt. Thank God for Youtube, I was able to solve this problem in minutes. Now it was time for Visualization!

## Visualization

![](https://github.com/samuelejedegba/Cyclistic-Data-Analysis/blob/main/Number_of_rides.PNG)
The above image shows the total number of rides in the last 12 months. The rides are broken down into Member Rides and Casual Rides and one can notice that there are more Member rides than casual rides.

![](https://github.com/samuelejedegba/Cyclistic-Data-Analysis/blob/main/Share_of_Rides.PNG)
The above places more emphasis on how the total number of rides are shared between Member riders and Casual Riders. While Member riders have 59.52% share of the rides, Casual Riders have just 40.48% share of the total rides.

![](https://github.com/samuelejedegba/Cyclistic-Data-Analysis/blob/main/Average_ride_minutes_per_day.PNG)
The above chart reveals an interesting story. Even though Member riders take more rides in general, Casual riders average longer rides per day. The average minutes of a ride per day among Casual Riders is 27.4 Minutes while Member riders is only 11.6 Minutes. On average, Casual Riders ride longer distances than Member riders.

![](https://github.com/samuelejedegba/Cyclistic-Data-Analysis/blob/main/Rides_per_day.PNG)
Why do Casual Riders ride longer distances on average? The above chart seems to give an insight to why. On Monday to Friday, Member Riders take way more rides than Casual Riders. But Weekends tell a different story. On saturday, the number of rides are almost the same between the two groups and on Sunday, Casual Riders take more rides than Member riders. This suggests that Member Riders use Cyclistic bikes to comute to and from work during the weekdays while Casual Riders (who ride more during weekends) do this for leisure. 

![](https://github.com/samuelejedegba/Cyclistic-Data-Analysis/blob/main/Average_rides_per_start_time.PNG)
To buttress the above point further, the chart above shows the average start time of the rides during the year. The chart shows a spike between 6am and 9am, which is the average start time for work and 3pm to 6pm which is the average closing time from work.

![](https://github.com/samuelejedegba/Cyclistic-Data-Analysis/blob/main/rides_per_month.PNG)
The above image shows the total rides per month. The total rides rise between June and August before falling in september. This is understandable as more people will use bike rides during the summer than winter.

![](https://github.com/samuelejedegba/Cyclistic-Data-Analysis/blob/main/member_rides_per_bike_type.PNG)
![](https://github.com/samuelejedegba/Cyclistic-Data-Analysis/blob/main/Casual_rides_per_bike_type.PNG)

The above images compares the share of rides per bike type to of Members to that of Casual riders. The Member Riders do not use the Docked Bike which also supports the claim that they are mostly everyday workers. Docked bikes have a specific station where the bike must be returned. This is why they are likely not used by the Member riders as they always have a specific destination which is not the dock station. However, 7.82 percent of Casual Rides are done with the Docked Bikes. These people have no specific destination in mind and are happy to use thes bikes for leisure and drop them at the Dock station.

## Conclusion and Reccomendation
1. To encourage Casual Riders to become members, Cyclistic needs to put a system in place that rewards longer ride times for Member Riders. Only members should have dicounted fees for longer rides per day. This would encourage casual riders who take longer rides per day to become members to benefit from this reward.
2. Casual Rides peak during weekends as from the data gotten, these riders do this for mostly leisure and exercises. A reward system for Members during weekends would not just make Member Riders ride more during weekends, but encourage Casual Riders to switch to membership and take advantage of this reward.
3. The reward system should also be specific for docked bikes. Even though Member Riders do not use Docked bikes, a reward system (like discount fees) should be made for MEmber Riders who use Docked bikes. These would encourage those Casual Riders who use the Docked Bikes to switch to membership and take advantage of this reward.
4. Cyclistic should take advantage of the summer months with aggressive promotion during the winter for Casual riders to become Members. Discount deals, free rides and reward points for longer rides during the summer for Member riders should be advertised. A summer challenge for member riders only where those with the longest rides get rewarded should be promoted.

## Things to Consider
The scope of this analysis is very limited and Data on Marketing style, pricing and Age and Gender should have been useful data to enhance this report.
