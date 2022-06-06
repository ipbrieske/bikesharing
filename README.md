# Overview 
This presentation is an analysis of bike-sharing data from New York City to project performance of a a similar service in Des Moines, IA. The project data originates from !(https://ride.citibikenyc.com/system-data), provided via a partnership between CitiBank and Lyft. 

These initial slides have been built using Tableau - a data visualization software meant to create beautiful, professional presentations using data in a litany of forms - seek to visualize ridership information along a number of axes, to get a better sense of the userbase of the bikesharing network. 

The Tableau Story can be accessed at ![this link](https://public.tableau.com/app/profile/isaac.brieske/viz/Citibike_Challenge_16543247255220/Story1?publish=yes) to follow along using the interactive aspect of the presentation. 

# Results

Our initial analysis has been split into 7 sections, each seeking to answer questions about the bikesharing network. Users are encouraged to follow along with the ![Tableau Story](https://public.tableau.com/app/profile/isaac.brieske/viz/Citibike_Challenge_16543247255220/Story1?publish=yes). 

## Trips per Day

Our first question to get a sense of the network was simple: Which days of the week had the highest and lowest demand on the system? We have highlighted the most in-demand days for emphasis. We initially expected weekdays would have the highest ridership, as more users were able to take leisure trips using the network. As it happened, Thursdays, Fridays, and Saturdays experienced the highest demand. Wednesdays and Sundays had the lowest ridership. The Wednesday lull is interesting: ~266,000 trips as a weekly low precedes the Thursday high of ~409,000 trips. Why this lull occured during August remains a question. 

![Trips Per Day](https://github.com/ipbrieske/bikesharing/blob/main/Images/TripsPerDay.png)

## Trip Duration

The vast majority of trips lasted for 4 - 6 minutes in length. The system appears to be immensely popular for travelling along short distances. The gridded, high density of bike stations facilitates this usage pattern, as visualized in the last section of the presentation. It should be noted, however, that there are hundreds of trips that lasted 2 to 3 hours in length, and such usage could be an opportunity for growth. 

![Trip Duration](https://github.com/ipbrieske/bikesharing/blob/main/Images/TripDuration.png)

## Trip Duration by Gender

Given an option of self-reporting as Male, Female, or Unknown, Male users represented a significant percentage of users. Despite this, usage times remained similar between each of the gender groups. All groups converged on the 46 - 47 minute mark as the longest standard trips taken. 

![Trip Duration by Gender](https://github.com/ipbrieske/bikesharing/blob/main/Images/TripDurationByGender.png)

## Weekday Trips

To get a better sense of the peaks and valleys of system demand, we next looked at the number of rides taken per hour of each weekday. Sundays and Saturdays show a much smoother rise and fall between low and high demand. During the workweek, demand peaks during rush hour in the morning and afternoon. From this, we can more clearly see the source of the low Wednesday demand: a paucity of afternoon ridership. Further study into this Wednesday afternoon lull is needed. 

![Weekday Trips](https://github.com/ipbrieske/bikesharing/blob/main/Images/WeekdayTrips.png)

## Weekday Trips by Gender

Usage patterns did not differ significantly between Male and Female riders; the same smooth rise in weekend ridership and peaks during weekday rush hours followed similar patters. Riders identifying as Unknown did see greater numbers during the weekends, to be further explained further in our next slide. 

![Weekday Trips by Gender](https://github.com/ipbrieske/bikesharing/blob/main/Images/WeekdayTripsByGender.png)

## User Type Rips by Gender and Weekday

When the user base is filtered based on being a Subscriber to the network or not, an interesting pattern emerges. We see that self-reporting of gender is higher amongst subscribers to the network. When looking at just non-subscribers, we see the highest number of people reporting as Unknown during Saturdays and Sundays. This seems to imply that 'one-time' or 'walk-up' customers are less inclined to commit to sharing data about themselves, and that data security is a concern amongst the non-subscriber userbase. 

![User Type Trips by Gender and Weekday](https://github.com/ipbrieske/bikesharing/blob/main/Images/RiderType.png)

## Starting Locations

We finish with a map of the CitiBike network in New York City, highlighting the bike stations serving as the starting location for the highest number of trips. Lower Manhattan sports the highest number of points of origin, with usage dropping off above W 59th Street at Central Park, but still remains higher uptown than in Brooklyn. Usage drops off heavily near the edges of the network, as would be expected from the preference for shorter trip durations. 

Though not included in this visualization, the bike stations in Jersey City and Hoboken held the highest number of outliers in terms of trip duration, with the most long-duration users originating from those stations. Further research is necessary as to why. 

![Ride Locations](https://github.com/ipbrieske/bikesharing/blob/main/Images/RideLocations.png)

# Summary

From this analysis we can draw a number of conclusions. The average rider on the network in August of 2019 was a male subscriber leaving from a station in Manhattan during rush hour on a Thursday, or sometime during daylight hours during the weekend. Both male and female riders used the network at similar rates, with non-subscriber ridership rising during the weekends. 

This analysis gives us a rough understanding of who used the network during the time period in question. By using further data analysis tools such as the Pandas library in Python, many more months of rider data could be added to the visualizations, enhancing the accuracy of the picture drawn. 

A few interesting questions remain: What accounts for the lull in ridership accross all user groups during Wednesday afternoons? Examinations outside the provided dataset must be made, such as alternative traffic (subways, bus) patterns on that day. We also are curious about atypical users, such as the users that take long-duration trips, or trips during late hours. Ridership reaches tens of thousands of riders per hour during peak times, so ensuring bikes are being maintained appropriately and during appropriate times would be valuable knowledge. 