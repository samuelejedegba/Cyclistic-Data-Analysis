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
