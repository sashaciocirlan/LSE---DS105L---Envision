---
title: "Tuning Into Your Music"
date: 20 March 2023
date-meta: 20 March 2023
---

# _Leader or Follower_: Exploring the Relationship Between Popular Artists and Music Trends


## Motivation:
Streaming services have brought about a significant transformation in the music industry, offering users convenient and cost-effective access to a vast catalog of songs. These services play a pivotal role in shaping artist visibility, revenue streams, and listening preferences. Moreover, the publicly available APIs provided by streaming platforms like Spotify, Apple Music, and Amazon Music offer unparalleled insights into various dimensions, including geography, audio features, and time, shedding light on trends among both artists and listeners.<br>
<br>
Throughout our project, we embarked with a set of guiding questions:<br>
* What are the most popular audio features, and how have they evolved over time?<br>
* How has the popularity of artists changed over time?<br>
* Is there a correlation between the evolution of audio features among top artists and the overall trends in popular music?<br>
<br>
While not all of these questions fell strictly within the scope of our analysis, they served as initial guiding points. Ultimately, our collective interest in music propelled us to undertake this project. Specifically, we sought to understand how, if at all, music has evolved over the last five years, and how the most popular artists' own stylistic choices relate to this evolution.

## Data Sources:
We used two sources of data for our research:<br>
* Billboard (Billboard API) via Python Package (pypi.python.org/pypi/billboard.py) 
* Spotify (Spotify API) (https://developer.spotify.com/documentation/web-api)<br>

### Data Collection Challenges:
Throughout the data collection section of our investigation our team encountered several challenges.<br>

#### Step 1
In Step 1, our objective was to investigate the top 10 artists of the past 5 years using Billboard’s weekly ‘Billboard Hot 100’ chart. Below is a cropped screenshot of the Billboard chart.<br>
<img width="400" alt="Kim.png" src="https://github.com/sashaciocirlan/LSE---DS105L---Envision/assets/114475296/4d64faaf-1250-4ca2-8e66-3c11a1e69d76">

Challenge|Solution|Outcome
:---|:---|:---
One major hurdle was the absence of a direct Billboard API, which was terminated in May 2013. Therefore, we could not retrieve the aggregated data or directly use Billboard's resources for aggregation.|We found a Python package, Billboard.py, on StackOverflow which helped us aggregate the data. With this, we could identify the ten artists with the most entries on the weekly charts over the past five years.|This underlined the value of leveraging existing solutions to overcome data analysis problems and avoid needing to reinvent the wheel. Forums like StackOverflow are particularly helpful for this.
Directly searching for the most popular artists was not possible as the Billboard Hot 100 features popular songs rather than individual artists.|We had to incorporate an extra step of identifying the artist behind each entry.|Waiting.

Refer to below for our obtained historic trend from Billboard.py<br>
<img width="484" alt="Screenshot 2023-05-29 at 12 32 09" src="https://github.com/sashaciocirlan/LSE---DS105L---Envision/assets/12870658/54f6ef69-a7f6-4d7f-97d0-b0bee2ea9404">


#### Step 2
In Step 2, our objective was to investigate the audio features of the top 50 songs per month over the past five years.

Challenge|Solution|Outcome
:---|:---|:---
Spotify's weekly charts did not provide easy access to their historical data, making it challenging for us to collect the required information.|After extensive research, we discovered that Spotify's historical data was stored in CSV files (insert photo). Therefore, we manually downloaded the CSV files and imported them into pandas dataframes for analysis.|This process taught us a valuable lesson about the accessibility of data. It served as a reminder that data is often not readily available and may require substantial effort to obtain. Additionally, we recognized the importance of data transformation when working with diverse data sources, as traditional organizations may employ storage formats that are less convenient but contain vital data, that data scientists have to work with while conducting analysis or transitioning an organization to a more modern data storage method. 

<br>

(Rough)Part 1: finding trends in the most popular music of the past 5 years
Data set used: ‘Weekly Top Songs Global’ by Spotify
Chart of the 200 most-streamed songs worldwide of the week released every Thursday
Historical charts provided in the form of CSV files
Data will be collected from the chart of 2018-05-24
We will look at the charts every 4 weeks for the next 5 years
Total of 66 charts



Below is a screenshot of our Spotify CSV File from Microsoft Excel.<br>
<img width="500" alt="Kim.png" src="https://github.com/sashaciocirlan/LSE---DS105L---Envision/assets/114475296/015125f8-9b2e-4e84-a2fc-f9b05bdd5972">

(Rough)<br>
What are audio features according to Spotify?
Documentation: https://developer.spotify.com/documentation/web-api/reference/get-several-audio-features
Audio features are as follows:
Danceability - how suitable a track is for dancing (0 is least danceable, 1 is most danceable)
Energy - perceptual measure of intensity and activity (0 is least energetic, 1 is most energetic)
Instrumentalness - how much vocals there are in a track (0 is least instrumental (ie. most vocal), 1 is most instrumental (ie. no vocals)
Liveness - likelihood of audience present (between 0 and 1)
Loudness - loudness of a track in decibels (dB) (higher values = louder)
Acousticness - how acoustic a track is (acoustic = no electrical amplification)
Speechiness - how much spoken word there is in a track (0 is least (only music), 1 is most (no music, only speaking), rap music would fall in between)
Tempo - tempo of the track in beats per minute (higher means the track is faster)
Valence - the musical happiness conveyed by the track (0 is saddest, 1 is happiest)
Duration_ms - the duration of the song in milliseconds

Using the Spotify API
The Spotify API ‘Get several tracks’ audio features’ request allows us to get the audio features of up to 100 songs
So we will do this for the top 50 songs every 4 weeks for the past 5 years
Below is an example dataframe showing the audio features of the songs from 2018-05-24

#### Step 3
In Step 3, our objective was to analyze the audio features of the top ten artists' songs from the past five years.

Challenge|Solution|Outcome
:---|:---|:---
We encountered a collaboration issue as there was a misalignment in our variable names and general code style. This lack of coherence in our functions between group members initially prevented us from collecting the data. For instance, one collaborator used the variable name 'Artist' while another used 'Top Ten Artist'.|To resolve this issue, we carefully reviewed and adjusted the variable names to ensure consistency. This enabled us to successfully execute the code.|Although seemingly minor, we argue that this is a common yet deceptively difficult challenge faced by data scientists when collaborating. As a result, we adopted a practice of establishing a baseline 'style' at the beginning of each collaborative coding session, which greatly streamlined the process.


#### Step 5 - We compare the Top Songs of the 10 most featured artists on the Billboard charts, in the past 5 years


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
![avg_audio_features](https://github.com/sashaciocirlan/LSE---DS105L---Envision/assets/127428021/b063594f-9fc3-4111-a2ce-4b930d36fcac)
![danceability](https://github.com/sashaciocirlan/LSE---DS105L---Envision/assets/127428021/6dd6e42b-3e5d-4340-8f9a-93ccbdb5087c)
![energy](https://github.com/sashaciocirlan/LSE---DS105L---Envision/assets/127428021/a5c72a68-013d-4d35-80c6-c04f2fa9e8ab)
![key](https://github.com/sashaciocirlan/LSE---DS105L---Envision/assets/127428021/703565c2-e072-4e9d-8665-6bb8a2b6f114)
![loudness](https://github.com/sashaciocirlan/LSE---DS105L---Envision/assets/127428021/e96e682f-7fa4-4fcb-a9c6-cddb864fe43d)
![mode](https://github.com/sashaciocirlan/LSE---DS105L---Envision/assets/127428021/279db048-d5e8-4676-9ca0-586833026fc5)
![speechiness](https://github.com/sashaciocirlan/LSE---DS105L---Envision/assets/127428021/23df194c-7588-4f6c-a74d-affa3bfa2658)


## Challenges:


## Conclusion:





## 📊 Data

## 📈 Analysis

## 🖼️ Results

## 🖋️ Conclusions

## 📚 References
