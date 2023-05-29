# Envision.github.io

# "Tuning into your tastes": Exploring popular song features and trends
___

## Executive Summary:


## Motivation:
Streaming services have brought about a significant transformation in the music industry, offering users convenient and cost-effective access to a vast catalog of songs. These services play a pivotal role in shaping artist visibility, revenue streams, and listening preferences. Moreover, the publicly available APIs provided by streaming platforms like Spotify, Apple Music, and Amazon Music offer unparalleled insights into various dimensions, including geography, audio features, and time, shedding light on trends among both artists and listeners.<br>
<br>
Throughout our project, we embarked with a set of guiding questions:<br>
* What are the most popular audio features, and how have they evolved over time?<br>
* How has the popularity of artists changed over time?<br>
* Is there a correlation between the evolution of audio features among top artists and the overall trends in popular music?<br>
<br>
While not all of these questions fell strictly within the scope of our analysis, they served as initial guiding points. Ultimately, our deep passion for music and curiosity propelled us to undertake this project, as we sought personal enjoyment and a deeper understanding of the subject matter.



## Aims & Objectives:
### Main objectives:


## Data and Data Challenges:
We used two sources of data for our research:<br>
* Billboard (Billboard API) via Python Package (pypi.python.org/pypi/billboard.py) 
* Spotify (Spotify API) (https://developer.spotify.com/documentation/web-api)<br>

### Data Challenges:
Throughout the data collection section of our investigation our team encountered several challenges.<br>

#### Step 1 Challenges
In Step 1, our objective was to investigate the top 10 artists of the past 5 years using Billboard’s weekly ‘Billboard Hot 100’ chart. Below is a cropped screenshot of the Billboard chart.<br>
<img src="./Billboard Chart.png" style="height:65%;width:65%">

Challenge|Solution|Outcome
:---|:---|:---
A major hurdle we faced was the absence of a direct Billboard API to access the required data. In fact, the Billboard API was officially terminated in May 2013. As a result, we couldn't retrieve the aggregated data or directly aggregate it through Billboard's resources.<br>Our direct search for the most popular artists proved unsuccessful since the Billboard Hot 100 primarily features popular songs rather than individual artists.|Fortunately, we discovered a Python package called Billboard.py that proved instrumental in creating code to aggregate the data. This enabled us to identify the artists with the most entries on the weekly charts over the past five years.<br>However, we identified a strong correlation between the number of songs an artist had entered and their popularity. For example, Drake had 800 songs entered over the five-year period.|This challenge provided valuable insight into the importance of seeking out existing solutions to overcome problems in data analysis.<br>This challenge deepened our understanding of the nature of imperfect data and the necessity to make justifiable statistical leaps when drawing conclusions, a common task for data scientists.




#### Step 2 Challenges
In Step 2, our objective was to investigate the audio features of the top 50 songs per month over the past five years.

Challenge|Solution|Outcome
:---|:---|:---
Spotify's weekly charts did not provide easy access to their historical data, making it challenging for us to collect the required information.|After extensive research, we discovered that Spotify's historical data was stored in CSV files (insert photo). Therefore, we manually downloaded the CSV files and imported them into pandas dataframes for analysis.|This process taught us a valuable lesson about the accessibility of data. It served as a reminder that data is often not readily available and may require substantial effort to obtain. Additionally, we recognized the importance of data transformation when working with diverse data sources, as traditional organizations may employ storage formats that are less convenient but contain vital data, that data scientists have to work with while conducting analysis or transitioning an organization to a more modern data storage method. 

Below is a screenshot of our Spotify CSV File from Microsoft Excel.<br>
<img src="./CSV File.png" style="height:65%;width:65%">

#### Step 3 - We needed to get historical trends to find out who the Top 10 artists have been throughout the past 5 years (2018 - 2023) 
1. We used Billboard python package, as it was more accessible than the API 
2. Use used the datetime package to get the top 100 Billboard chart for every week since May 2018
3. We looped over each chart and calculated how many features each artists has had in total throughout 260 weeks; we created the ranking and we were amazed to see that a Country singer has been the 2nd top charted artist, after Drake, of course. 
<img width="484" alt="Screenshot 2023-05-29 at 12 32 09" src="https://github.com/sashaciocirlan/LSE---DS105L---Envision/assets/12870658/54f6ef69-a7f6-4d7f-97d0-b0bee2ea9404">

# 
#### Step 5 - We compare the Top Songs of the 10 most featured artists on the Billboard charts, in the past 5 years
Challenges 


### Methodology: 
1. Fetch the audio features for the top songs of the top artists
2. Calculate the average audio features for each top artist
3. Convert the artist data into a DataFrame
<img width="582" alt="Screenshot 2023-05-29 at 12 18 06" src="https://github.com/sashaciocirlan/LSE---DS105L---Envision/assets/12870658/379b34d3-f5bb-4f32-879c-2954c72cf4f0">

### Data Cleaning - Cleaned data frame, sorted artists by rank in charts, renamed columns and made them easier to work with in future visualisations 
<img width="1151" alt="Screenshot 2023-05-29 at 12 18 29" src="https://github.com/sashaciocirlan/LSE---DS105L---Envision/assets/12870658/2603282e-453d-4057-bae9-d6a1086adc2d">

### Data Visualisation 
<img width="1151" alt="Screenshot 2023-05-29 at 12 19 05" src="https://github.com/sashaciocirlan/LSE---DS105L---Envision/assets/12870658/536fea81-4cf9-4b85-aa52-2771df16bc56">



## Data Visualisation:


## Challenges:


## Conclusion:
