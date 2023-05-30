---
title: "Tuning Into Your Music"
date: 20 March 2023
date-meta: 20 March 2023
---

# _Leader or Follower_: Exploring the Relationship Between Popular Artists and Music Trends

<p align="middle">
  <img src="https://github.com/sashaciocirlan/LSE---DS105L---Envision/assets/114475296/5be08ffe-45cc-463a-935f-53e407d0f411" width="450" />
  <img src="https://github.com/sashaciocirlan/LSE---DS105L---Envision/assets/114475296/c8eae849-4941-4523-9c07-d54260eed2ee" width="450" /> 
</p>


## 🏠 Team members

<br>
<p align="middle">
  <img src="https://github.com/sashaciocirlan/LSE---DS105L---Envision/assets/114475296/d2018c54-0246-45b8-96dd-dae77aba42cd" width="150" />
  <img src="https://github.com/sashaciocirlan/LSE---DS105L---Envision/assets/114475296/6d371631-3dc2-4b9a-a511-742b96f66719" width="150" /> 
  <img src="https://github.com/sashaciocirlan/LSE---DS105L---Envision/assets/114475296/86581025-4645-4ac9-94c7-9f65cb14a105" width="150" />
  <img src="https://github.com/sashaciocirlan/LSE---DS105L---Envision/assets/114475296/7e459764-9f5c-4b05-942f-cb9dff9c084d" width="150" /> 
  <img src="https://github.com/sashaciocirlan/LSE---DS105L---Envision/assets/114475296/f575137f-2aa2-4ba6-8f05-3114fd3118da" width="150" />
</p>


- [David Bredin](): I'm David, a final-year Politics student at the LSE. I've developed a strong interest in Big Data, and spent time in strategy at a start-up utilising AI to automate MRI annotations. With DS105, I've dug into the technical side of data science and I'm hooked! 

- [HyeongJu Kim](): I'm HyeongJu, a first-year student at LSE, pursuing a degree in Politics and Data Science. The raw emotion and storytelling embedded in rap captivate me, and I believe there is a profound connection between the world of politics and the lyrical power of hip-hop!

- [Jacen Hutagaol](): I'm Jacen, a first-year Politics and Data Science student who secretly wishes there was a degree in Pop Music [with Data Science]. You will rarely find me without my earphones, which have recently been blasting Kylie Minogue and K-Pop stars Le Sserafim.

- [Sasha Ciocirlan](): I'm Sasha, a final-year Politics and Economics student at the LSE. Although I'm not your typical number-cruncher, I've taken a detour into data science and found a new passion, and am bringing a deep love for music to the project.

- [Toni Byfield](): I'm Toni, a second-year economics student. I enjoy coding and love music. I've recently been hooked on the Cults, a favourite is 'Gilded Lily'. Check 'em out!


## 📝 Executive Summary
This project utilised data from streaming platforms' APIs, including Spotify and Billboard, to examine the influence of streaming services on the music industry. The project aimed to understand the evolution of audio features, changes in artist popularity, and potential correlations between audio feature trends and popular music trends.<br>
Through five key steps, the project explored these aspects.
* Analysing the top 10 artists over the past 5 years using the Billboard's Hot 100 chart. 
* Collecting data on the audio features of the top 50 songs per month during this period. 
* Examining the audio features of the top ten artists' songs over the past five years.
* Establishing industry benchmarks by calculating average values and standard deviations or ranges of audio feature categories. This identifies the audio features that experienced the most and least change over time. 
* Comparing the analysis from Step 4 to the audio features of the top ten artists' songs, using visualizations like scatter plots and radar graphs to represent the findings.

The findings hold significance for artists, industry professionals, and streaming platforms. Understanding evolving audio feature preferences and artist popularity informs decision-making for song production, marketing, and playlist curation. Exploring correlations between audio feature trends and popular music trends contributes to predicting future music preferences and shaping the industry's direction.<br>
In conclusion, this project harnessed data from streaming platforms to investigate the impact of streaming services on the music industry. By analyzing audio features and artist popularity, valuable insights were gained into the evolution of music preferences and potential connections with overall trends. These findings offer practical implications for decision-making in the music industry and contribute to its growth and success.

## 🔋 Motivation
Streaming services have brought about a significant transformation in the music industry, offering users convenient and cost-effective access to a vast catalog of songs. These services play a pivotal role in shaping artist visibility, revenue streams, and listening preferences. Moreover, the publicly available APIs provided by streaming platforms like Spotify, Apple Music, and Amazon Music offer unparalleled insights into various dimensions, including geography, audio features, and time, shedding light on trends among both artists and listeners.<br>
<br>
Throughout our project, we embarked with a set of guiding questions:<br>
* What are the most popular audio features, and how have they evolved over time?<br>
* How has the popularity of artists changed over time?<br>
* Is there a correlation between the evolution of audio features among top artists and the overall trends in popular music?<br>
<br>
While not all of these questions fell strictly within the scope of our analysis, they served as initial guiding points. Ultimately, our collective interest in music propelled us to undertake this project. Specifically, we sought to understand how, if at all, music has evolved over the last five years, and how the most popular artists' own stylistic choices relate to this evolution.

## 👨‍💻 Data Sources
We used two sources of data for our research:<br>
* Billboard (Billboard API) via Python Package (pypi.python.org/pypi/billboard.py) 
* Spotify (Spotify API) (https://developer.spotify.com/documentation/web-api)<br>

## 📊 Exploratory Data Analysis
### Billboard API
In Step 1, our objective was to investigate the top 10 artists of the past 5 years using Billboard’s weekly ‘Billboard Hot 100’ chart. Below is a cropped screenshot of the Billboard chart.<br>
<img width="400" alt="Kim.png" src="https://github.com/sashaciocirlan/LSE---DS105L---Envision/assets/114475296/4d64faaf-1250-4ca2-8e66-3c11a1e69d76">
<br>
Refer to below for our obtained historic trend from Billboard.py<br>
<img width="484" alt="Screenshot 2023-05-29 at 12 32 09" src="https://github.com/sashaciocirlan/LSE---DS105L---Envision/assets/12870658/54f6ef69-a7f6-4d7f-97d0-b0bee2ea9404">

### Spotify API
Similarly, we looked at the Spotify API to investigate the audio features of the top 50 songs per month over the past five years. We used the "Weekly Top Songs Global" chart generated by Spotify every Thursday, which shows the 200 most streamed songs worldwide of the week. Data were collected from 2018/05/24, and we observed a total of 66 charts: every 4 weeks for 5 years. The "Get several tracks' audio features" request in the API allowed us to acquire the audio features of up to 100 tracks.<br>
Below is a screenshot of an example of the Spotify CSV Files from Microsoft Excel, showing the most-streamed songs on the week of 2018/05/24.<br>
<img width="500" alt="Kim.png" src="https://github.com/sashaciocirlan/LSE---DS105L---Envision/assets/114475296/015125f8-9b2e-4e84-a2fc-f9b05bdd5972">
<br>
#### Audio Features
We followed the definition of audio features provided by Spotify: (https://developer.spotify.com/documentation/web-api/reference/get-several-audio-features)<br>
* Danceability - how suitable a track is for dancing (0 is least danceable, 1 is most danceable)
* Energy - perceptual measure of intensity and activity (0 is least energetic, 1 is most energetic)
* Instrumentalness - how much vocals there are in a track (0 is least instrumental (ie. most vocal), 1 is most instrumental (ie. no vocals)
* Liveness - likelihood of audience present (between 0 and 1)
* Loudness - loudness of a track in decibels (dB) (higher values = louder)
* Acousticness - how acoustic a track is (acoustic: no electrical amplification)
* Speechiness - how much spoken word there is in a track (0 is least (only music), 1 is most (no music, only speaking), rap music would fall in between)
* Tempo - tempo of the track in beats per minute (higher means the track is faster)
* Valence - the musical happiness conveyed by the track (0 is saddest, 1 is happiest)
* Duration_ms - the duration of the song in milliseconds



Step 3: 
In Step 3, our objective was to analyze the audio features of the top ten artists' songs from the past five years.


## 💪🏼 Data Collection Challenges
Throughout the data collection section of our investigation our team encountered several challenges. However, through diligent problem-solving and collaboration, our team successfully devised solutions for each of these challenges.<br>

Challenge|Solution|Outcome
:---|:---|:---
One major hurdle was the absence of a direct Billboard API, which was terminated in May 2013. Therefore, we could not retrieve the aggregated data or directly use Billboard's resources for aggregation.|We found a Python package, Billboard.py, on StackOverflow which helped us aggregate the data. With this, we could identify the ten artists with the most entries on the weekly charts over the past five years.|This underlined the value of leveraging existing solutions to overcome data analysis problems and avoid needing to reinvent the wheel. Forums like StackOverflow are particularly helpful for this.
Directly searching for the most popular artists was not possible as the Billboard Hot 100 features popular songs rather than individual artists.|We incorporated an extra step of identifying the artist behind each entry, and then we summed up all artists' songs total number of entries throught 5 years (52 Top 100 charts/year) |We got a strong indicator of the top 10 artists in the past 5 years (e.g. Drake has over 800 total entries in all charts) and we used the Top 10 list we compiled as a baseline for further analysis.
Spotify's weekly charts did not provide easy access to their historical data, making it challenging for us to collect the required information.|After extensive research, we discovered that Spotify's historical data was stored in CSV files (insert photo). Therefore, we manually downloaded the CSV files and imported them into pandas dataframes for analysis.|This process taught us a valuable lesson about the accessibility of data. It served as a reminder that data is often not readily available and may require substantial effort to obtain. Additionally, we recognized the importance of data transformation when working with diverse data sources, as traditional organizations may employ storage formats that are less convenient but contain vital data, that data scientists have to work with while conducting analysis or transitioning an organization to a more modern data storage method. 
We encountered a collaboration issue as there was a misalignment in our variable names and general code style. This lack of coherence in our functions between group members initially prevented us from collecting the data. For instance, one collaborator used the variable name 'Artist' while another used 'Top Ten Artist'.|To resolve this issue, we carefully reviewed and adjusted the variable names to ensure consistency. This enabled us to successfully execute the code.|Although seemingly minor, we argue that this is a common yet deceptively difficult challenge faced by data scientists when collaborating. As a result, we adopted a practice of establishing a baseline 'style' at the beginning of each collaborative coding session, which greatly streamlined the process.


## 📈 Data Analysis

### Determining "Industry Benchmarks"
We have already found the values of each audio feature for each individual song over the past 5 years, but we now want to combine all this data into an "industry benchmark" which could give us an overall picture of what the most popular songs sound like. To do this, we calculated a weighted average for each audio feature. This is done by multiplying each song's value by the number of streams it received that week, adding up all the 50 songs' values and then dividing it by the total number of streams received by these songs that week. Thus, songs that get streamed more will make a bigger contribution to the weighted average than other songs, and the resulting value is more representative of streamers' listening habits.  Consequently, the resulting dataframe will contain both the initial and final sections.
### Comparison
(Rough) First we get the overall average values for the most popular songs (Just get the mean of the values in the above dataframe). We use Sasha’s dataframe with the values for the top 10 artists: for each audio feature, we substract the overall average and the resulting value would be the difference between top artists and the industry benchmark.



## Methodology: 
1. Fetch the audio features for the top songs of the top artists
2. Calculate the average audio features for each top artist
3. Convert the artist data into a DataFrame
<img width="582" alt="Screenshot 2023-05-29 at 12 18 06" src="https://github.com/sashaciocirlan/LSE---DS105L---Envision/assets/12870658/379b34d3-f5bb-4f32-879c-2954c72cf4f0">

### Data Cleaning - Cleaned data frame, sorted artists by rank in charts, renamed columns and made them easier to work with in future visualisations 
<img width="1151" alt="Screenshot 2023-05-29 at 12 18 29" src="https://github.com/sashaciocirlan/LSE---DS105L---Envision/assets/12870658/2603282e-453d-4057-bae9-d6a1086adc2d">

### Data Visualisation 
<img width="1151" alt="Screenshot 2023-05-29 at 12 19 05" src="https://github.com/sashaciocirlan/LSE---DS105L---Envision/assets/12870658/536fea81-4cf9-4b85-aa52-2771df16bc56">



## 📑 Data Visualisation:
The objective of the first visualisation is to see if the most popular artists differ greatly from the most popular songs (in terms of their audio features) over the past 5 years.<br>
In the previous section, we have already calculated the difference between the average audio feature values of the top songs and top artists. In order to visualise this data, a radar chart was created using the plotly package. Because the radar chart required all the different categories (ie. audio features) to be measured on the same scale, the loudness, tempo and duration features were dropped from the data as they did not follow the same measurement scale (loudness was measured in decibels, tempo in beats per minute and duration in milliseconds). All the other features were measured on a scale between 0 and 1.<br>
The resulting radar chart is as follows:<br>
<img width="800" alt="Radar_Chart.png" src="https://github.com/sashaciocirlan/LSE---DS105L---Envision/assets/114475296/2d5ee9d4-9bc4-4ecd-bf66-ac5da49460cb">

On the radar chart, a value of 0 means that the average value of the audio feature for an artist is the same as that of the most popular songs. For example, the danceability of this artist’s songs is at the same level as the most popular songs of the past 5 years. This means that as an artist’s value moves further away from 0, their songs increasingly differ from the most popular songs of the past 5 years.<br>
In general, the plot shows that most of these artists’ values hover around 0 across all audio features, which means that their music closely matches the type of music that has remained popular over the past 5 years. The audio features that appear to have the least deviation across artists include instrumentalness, danceability, and speechiness. For some audio features, there are a few significant outliers that demonstrate their difference from the current music landscape.<br>
The artist that appears to have the most deviation from the most popular songs is Billie Eilish. Her acousticness score is almost 0.6 higher than the most popular songs, and her energy score is about 0.4 lower as well. This means that her music tends to be a lot more acoustic and less energetic than a typical song one would hear on the radio today.<br>
Other artists that appear to have visually significant deviations from the most popular songs include Lil Baby and DaBaby, whose songs have a speechiness score of about 0.2 more than the rest. This makes sense as they are rappers, which explains why there would be more spoken word in their songs. While Drake and Doja Cat, who are also in the top 10 artists list, are also rappers, their most popular songs over the past 5 years have been more pop than rap, as they sing more frequently than rap. That could explain why even though they both have the next-highest speechiness scores, they remain quite close to the overall average set by the most popular songs.



<br>
<br>
<br>



![dance](https://github.com/sashaciocirlan/LSE---DS105L---Envision/assets/127428021/3ac35441-36e8-40d6-af4e-a08be05ed33d)
![energy](https://github.com/sashaciocirlan/LSE---DS105L---Envision/assets/127428021/d1d7d8d2-1007-455b-b4b3-b45bfc53b422)
![key](https://github.com/sashaciocirlan/LSE---DS105L---Envision/assets/127428021/11cf673c-ed6f-421d-a2db-fa95b89b1a36)
![loudness](https://github.com/sashaciocirlan/LSE---DS105L---Envision/assets/127428021/a5d3d0b5-e571-4894-b5cd-80434894f0cc)
![mode](https://github.com/sashaciocirlan/LSE---DS105L---Envision/assets/127428021/60b3f036-7a72-4152-973e-56ee29d88bb4)
![speechiness](https://github.com/sashaciocirlan/LSE---DS105L---Envision/assets/127428021/409686fd-81bf-448f-a2ca-ad0b776c997a)
![avg_parallel](https://github.com/sashaciocirlan/LSE---DS105L---Envision/assets/127428021/29ac8227-b58b-4057-9772-38553d1cc4bf)


## Challenges:


## Conclusion:





## 📊 Data

## 📈 Analysis

## 🖼️ Results

## 🖋️ Conclusions

## 📚 References
