# Billboard Hot 100 Number Ones
This week we are exploring the Billboard Hot 100 Number Ones Database. This workbook contains substantial data about every song to ever top the Billboard Hot 100 between August 4, 1958 and January 11, 2025. It was compiled by Chris Dalla Riva as he wrote the book Uncharted Territory: What Numbers Tell Us about the Biggest Hit Songs and Ourselves. It also often powers his newsletter Can't Get Much Higher.

## Dataset
* **Source:** [Tidy Tuesday - 26.08.2025](https://github.com/rfordatascience/tidytuesday/blob/main/data/2025/2025-08-26)

## Tech Stack
* `pandas`
* `matplotlib`
* `musicbrainz api`

## Key Steps
1. **Step 1. Exploring Dataset**
2. **Step 2. Cleaning Data**
3. **Step 3. Exploring Data Using Visualisations**
4. **Step 4. Preparing data for Power BI Dashboard**

## Project Objective
This week i am exploring Billboard Hot 100 Number Ones Dataset provided as part of Tidy Tuesday 26.08.2025

* Have #1 hits become shorter over time?
There's a clear trend of #1 hits becoming shorter over time, a shift likely influenced by the rise of streaming platforms.
* Does the relation between artist age and chart success change across time?
The relationship between artist age and chart success isn't static. It reflects broader trends in music consumption and societal values, with a notable increase in the average age of artists achieving #1 success.
* Which keys are most common in #1 hits? Do our key preferences differ by genre?
Certain major keys like G, C, and D are most common in #1 hits. The data suggests that key preferences often differ by genre, influenced by common instruments.
* What lyrical topics have dominated #1 hits across different decades?
While themes of love have been a constant, a considerable shift occurred in the 2000s, where topics of lust and sex gained dominance
* How has the prevalence of explicit content changed over time?
There has been a significant increase in explicit content since the 1990s and 2000s, driven by societal changes and the internet bypassing traditional censorship.

## Exploring Dataset
This is a very wide dataset with some columns missing quite a few of the values. At this stage we need to decide how to approach this? Is working with 100+ columns optimal not only from analysis perspective but also from performance perspective. We can't even view the entire 100+ columns using standard .info() , i think the best way to work with this dataset is to only use what we need to answer our questions. This will benefit overall technical perforamnce, but will also make working with the dataset easier.

## Data cleaning
This is a very wide datset, with over 100 columns of data. While i would love to utilise every single column of data and use the entirety of this dataset i think the best approach would be to extract selected columns in to a new dataframe to make working with this data easier. We could always add extra columns if neccesary. This will prevent us from carrying out unnecessary data cleaning steps, again if there is need for any extra columns that have missing values we could always add these if needed. Initially i will extract the data required to deal with the initial questions. I've utilised music brainz public api to fill out missing genre details for the songs. 

## Exploridng Data Using Visualisations
Have #1 hits become shorter over time?.
![Average Song Duration in Seconds](/python_screenshots/average_song_duration_seconds.png "Average Song Duration in Seconds")  

Does the relation between artist age and chart success change across time?
![Average Front Person Age](/python_screenshots/average_front_person_age.png "Average Front Person Age")  

Which keys are most common in #1 hits? Do our key preferences differ by genre?
![Most Popular Keys](/python_screenshots/most_frequently_used_keys.png "Most Popular Keys")  
![Most Popular Keys by Genere](/python_screenshots/genre_key_usage.png "Most Popular Keys by Genre")  

What lyrical topics have dominated #1 hits across different decades?
![Lyrical Topics](/python_screenshots/all_top_topics_by_decade.png "Lyrical Topics")

## Creating a Power BI Dashboard
In this step i have created a power bi dashboard with exported dataset from python

![Power Bi Dashboard](/dashboard_screenshots/main.JPG "Power Bi Dashboard")  
![Power Bi Dashboard filtered by topic](/dashboard_screenshots/filtered_topic.JPG "Power Bi Dashboard filtered by topic")  
![Power Bi Dashboard filtered by genre](/dashboard_screenshots/filtered_genre.JPG "Power Bi Dashboard filtered by genre")  
![Star Schema Data Model](/dashboard_screenshots/star_chema.JPG "Star Schema Data Model")  