# Ford GoBike System Data Analysis and Visualizations
## by Bilal Almajnooni


## Dataset

The dataset is Ford GoBike system, it included 183412 observations and 16 variables. 

We did some data wrangling, it is as follows:
- Drop rows that contain null values.
- `start_time` and `end_time` should *datetime* instead of *object*.
- `start_station_id`, and `end_station_id` should be *int* instead of *float*.
- `user_type`, `member_gender`, and `bike_share_for_all_trip` should be *category* instead of *object*.
- Derive age from `member_birth_year` and create `member_age` column to store the values in it.
- Manually fix a data entry error for a biker having birth year of 1878 to 1978.
- Derive minutes from `duration_sec` and create `duration_mins` column to store the values in it.
- Derive hour, day of the week from `start_time` and create `start_hour` and `start_day` columns and store the values in it.
- limit the dataset by taking only data of people aged 60 and younger.
- limit the dataset by taking trip durations of less than 60 minutes.


## Summary of Findings

Findings based on:

### Univariate Exlporation:

- What is the range of trip length for most bike users?
    >Looking at this plot, we can determine that most bike users tend to take short trips that ranges from 4 to 16 minutes with an average of 10 minutes.
- Which start/end station had the most visits?
    >It seems that stations 58 (Market St at 10th St), and 67 (San Francisco Caltrain Station 2  (Townsend St at 4th St)) are the most visited as either a start or an end station from bike users.
- At what time do people usually use the service? and when do they finish?
    >The majority of users start to use the service from early morning at 6am with a peak hour at 8am. And for the afternoon, there is decent activity until we reach 5pm where there are more users using the services.
The peak hours for bike trips are 8AM and 5PM.

### Bivariate Exlporation:

- What age group is the most active for each gender?
    >Both genders, as well as other group, have smiliar distribution. We can say that the age group 25-42 are the most active. Late 20's and early 30's users are at the peak of activity compared to others.
- Do users that have a subcription take longer trips than customers?
    >On average, Customers take 5 mintues longer trips than subsrcibers.
- Do subsrcibers have their own lineup of bikes or do they use the same ones customers use?
    >It seems that it is not the case in which a bike is reserved for a subscriber. However there are cases in which no customers have ridden bikes that subscribers rode, and vice versa.

### Multivariate Exlporation:

- How many trips did the bikes take from the same start station to the same end station?
    >It looks like there have been occasions of bikes to take the same route of trip more than once, even up to 7 times.
- What is the peak trip duration and age for bikers on each day of the week?
    >On weekdays, users in their mid 30's tend use the bikes the most with an average duration of 7.5 minutes. However, during the weekends, users in their early 30's are more noticable in using the bikes to take a trip that lasts less than 7.5 minutes on average.


## Key Insights for Presentation

- What is the range of trip length for most bike users?
- Do users that have a subcription take longer trips than customers?
- How many trips did the bikes take from the same start station to the same end station?
- What is the peak trip duration and age for bikers on each day of the week?