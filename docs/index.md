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


## 🏠 TEAM MEMBERS

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
This project utilised data from streaming platforms' APIs, including **Spotify** and **Billboard**, to examine the influence of streaming services on the music industry. The project aimed to understand the evolution of audio features, changes in artist popularity, and potential correlations between audio feature trends and popular music trends.<br>
Through **five key steps**, the project explored these aspects.
* Analysing the **top 10 artists** over the past **5 years** using the Billboard's Hot 100 chart. 
* Collecting data on the **audio features** of the **top 50 songs per month** during this period. 
* Examining the **audio features** of the top ten **artists' songs** over the past five years.
* Establishing **industry benchmarks** by calculating average values and standard deviations or ranges of audio feature categories. This identifies the audio features that experienced the most and least change over time. 
* Comparing the analysis from Step 4 to the audio features of the top ten artists' songs, using **visualisations** like **scatter plots** and **radar graphs** to represent the findings.

The findings hold significance for artists, industry professionals, and streaming platforms. Understanding evolving audio feature preferences and artist popularity informs decision-making for song production, marketing, and playlist curation. Exploring correlations between audio feature trends and popular music trends contributes to predicting future music preferences and shaping the industry's direction.<br>
In conclusion, this project harnessed data from streaming platforms to investigate the impact of streaming services on the music industry. By analysing audio features and artist popularity, valuable insights were gained into the evolution of music preferences and potential connections with overall trends. These findings offer practical implications for decision-making in the music industry and contribute to its growth and success.

## 🔋 Motivation
Streaming services have brought about a significant transformation in the music industry, offering users convenient and cost-effective access to a vast catalog of songs. These services play a pivotal role in shaping artist visibility, revenue streams, and listening preferences. Moreover, the publicly available APIs provided by streaming platforms like Spotify, Apple Music, and Amazon Music offer unparalleled insights into various dimensions, including geography, audio features, and time, shedding light on trends among both artists and listeners.<br>
<br>
Throughout our project, we embarked with a set of guiding questions:<br>
* What are the most popular audio features, and how have they evolved over time?<br>
* How has the popularity of artists changed over time?<br>
* Is there a correlation between the evolution of audio features among top artists and the overall trends in popular music?<br>
While not all of these questions fell strictly within the scope of our analysis, they served as initial guiding points. Ultimately, our collective interest in music propelled us to undertake this project. Specifically, we sought to understand how, if at all, music has evolved over the last five years, and how the most popular artists' own stylistic choices relate to this evolution.

## 👨‍💻 Data Sources
We used two sources of data for our research:<br>
* Billboard (Billboard API) via Python Package (pypi.python.org/pypi/billboard.py) 
* Spotify (Spotify API) (https://developer.spotify.com/documentation/web-api)<br>

## 📊 Exploratory Data Analysis
### Billboard API
We looked at Billboard’s weekly “Billboard Hot 100” chart, a weekly music chart that ranks the 100 most popular songs in the United States on various factors, to investigate the top 10 artists of the past 5 years cumulative. Due to reasons that will be specified below, we obtained data from a Python Package called Billboard.py. Data were collected from 2018/05/24, and we observed weekly for 5 years. 
<br>
Refer to below for our obtained historic trend from Billboard.py<br>
<p align="middle">
  <img width="484" alt="Screenshot 2023-05-29 at 12 32 09" src="https://github.com/sashaciocirlan/LSE---DS105L---Envision/assets/12870658/54f6ef69-a7f6-4d7f-97d0-b0bee2ea9404">
</p>

### Spotify API
Similarly, we looked at the Spotify API to investigate the audio features of the top 50 songs per month over the past five years. We used the "Weekly Top Songs Global" chart generated by Spotify every Thursday, which shows the 200 most streamed songs worldwide of the week. Data were also collected from 2018/05/24, and we observed a total of 66 charts: every 4 weeks for 5 years. The "Get several tracks' audio features" request in the API allowed us to acquire the audio features of up to 100 tracks.<br>
Below is a screenshot of an example of the Spotify CSV Files from Microsoft Excel, showing the most-streamed songs on the week of 2018/05/24.<br>
<p align="middle">
  <img width="500" alt="Kim.png" src="https://github.com/sashaciocirlan/LSE---DS105L---Envision/assets/114475296/015125f8-9b2e-4e84-a2fc-f9b05bdd5972">
</p>
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
Spotify's weekly charts did not provide easy access to their historical data, making it challenging for us to collect the required information.|After extensive research, we discovered that Spotify's historical data was stored in CSV files. Therefore, we manually downloaded the CSV files and imported them into pandas dataframes for analysis.|This process taught us a valuable lesson about the accessibility of data. It served as a reminder that data is often not readily available and may require substantial effort to obtain. Additionally, we recognized the importance of data transformation when working with diverse data sources, as traditional organisations may employ storage formats that are less convenient but contain vital data, that data scientists have to work with while conducting analysis or transitioning an organisation to a more modern data storage method. 
We encountered a collaboration issue as there was a misalignment in our variable names and general code style. This lack of coherence in our functions between group members initially prevented us from collecting the data. For instance, one collaborator used the variable name 'Artist' while another used 'Top Ten Artist'.|To resolve this issue, we carefully reviewed and adjusted the variable names to ensure consistency. This enabled us to successfully execute the code.|Although seemingly minor, we argue that this is a common yet deceptively difficult challenge faced by data scientists when collaborating. As a result, we adopted a practice of establishing a baseline 'style' at the beginning of each collaborative coding session, which greatly streamlined the process.


## 📈 Data Analysis

### Determining "Industry Benchmarks"
We have already found the values of each audio feature for each individual song over the past 5 years, but we now want to combine all this data into an "industry benchmark" which could give us an overall picture of what the most popular songs sound like. To do this, we calculated a weighted average for each audio feature. This is done by multiplying each song's value by the number of streams it received that week, adding up all the 50 songs' values and then dividing it by the total number of streams received by these songs that week. Thus, songs that get streamed more will make a bigger contribution to the weighted average than other songs, and the resulting value is more representative of streamers' listening habits.  Consequently, the resulting dataframe will contain both the initial and final sections.
### Comparison
(Rough) First we get the overall average values for the most popular songs (Just get the mean of the values in the above dataframe). We use Sasha’s dataframe with the values for the top 10 artists: for each audio feature, we substract the overall average and the resulting value would be the difference between top artists and the industry benchmark.


## 📑 Data Visualisation
### Plotting into Dataframe
The primary goal of the initial visualization is to examine whether there are substantial differences between the audio features of the most popular artists and the most popular songs over the past five years. <br>
In the preceding section, we had already computed the variance in average audio feature values between the top songs and top artists. To present this data visually, we created a radar chart using the plotly Python package. However, since the radar chart necessitated uniform measurement scales for all categories (i.e., audio features), we excluded loudness, tempo, and duration from the data due to their disparate measurement units (loudness in decibels, tempo in beats per minute, and duration in milliseconds). All other features were scaled between 0 and 1 for consistency. <br>
The resulting radar chart is as follows: <br>
<img width="800" alt="Radar_Chart.png" src="https://github.com/sashaciocirlan/LSE---DS105L---Envision/assets/114475296/2d5ee9d4-9bc4-4ecd-bf66-ac5da49460cb">

On the radar chart, a value of 0 means that the average value of the audio feature for an artist is the same as that of the most popular songs. For example, the danceability of this artist’s songs is at the same level as the most popular songs of the past 5 years. This means that as an artist’s value moves further away from 0, their songs increasingly differ from the most popular songs of the past 5 years.<br>
In general, the plot shows that most of these artists’ values hover around 0 across all audio features, which means that their music closely matches the type of music that has remained popular over the past 5 years. The audio features that appear to have the least deviation across artists include instrumentalness, danceability, and speechiness. For some audio features, there are a few significant outliers that demonstrate their difference from the current music landscape.<br>
The artist that appears to have the most deviation from the most popular songs is Billie Eilish. Her acousticness score is almost 0.6 higher than the most popular songs, and her energy score is about 0.4 lower as well. This means that her music tends to be a lot more acoustic and less energetic than a typical song one would hear on the radio today.<br>
Other artists that appear to have visually significant deviations from the most popular songs include Lil Baby and DaBaby, whose songs have a speechiness score of about 0.2 more than the rest. This makes sense as they are rappers, which explains why there would be more spoken word in their songs. While Drake and Doja Cat, who are also in the top 10 artists list, are also rappers, their most popular songs over the past 5 years have been more pop than rap, as they sing more frequently than rap. That could explain why even though they both have the next-highest speechiness scores, they remain quite close to the overall average set by the most popular songs.

### Scatterplots
To visualise how the audio features of the most popular songs have changed over time, or lack thereof, scatter plots with trend lines were created using the plotnine package. Each scatter plot shows all the values of one audio feature for all of the songs that have been analysed (i.e. top 50 songs every 4 weeks for 5 years). <br>

1. Danceability
<p align="center">
  <img width="450" alt="Danceability.png" src="https://github.com/sashaciocirlan/LSE---DS105L---Envision/assets/114475296/ce25d581-ea4e-4c4f-8db2-c5bc99e55b5b">
</p>

   - The danceability scatter plot shows that most of the top songs have a value of more than 0.5, which indicates that popular songs tend to be danceable.
   - However, the trendline in red is slightly decreasing. Even though it might indicate that songs are becoming less danceable, the small gradient of the slope does not necessarily show a significant trend.

2. Energy
<p align="center">
  <img width="450" alt="Energy.png" src="https://github.com/sashaciocirlan/LSE---DS105L---Envision/assets/114475296/3e86c41f-645b-4249-9cc9-4e95bc11f943">
</p>

   - Similarly, most popular songs tend to be energetic, with most songs having energy scores of above 0.5. 
   - Here, the trend line is increasing but only slightly, so we cannot say for sure that songs are getting more energetic over time. 

3. Speechiness
<p align="center">
  <img width="450" alt="Speechiness.png" src="https://github.com/sashaciocirlan/LSE---DS105L---Envision/assets/114475296/72cfa4f2-cf6d-421f-b456-6bf05613c4d8">
</p>

   - Almost all of the songs have speechiness scores of below 0.5, with only 3 points on the scatter plot being above 0.5. This indicates a very strong likelihood that a popular song would definitely have more music and singing than spoken word.
   - The trendline is going down slightly, and visually there are fewer songs with scores above 0.3 as time passes. This could indicate that such songs (like rap songs) could be getting less popular over time but only marginally.

4. Acousticness
<p align="center">
  <img width="450" alt="Acousticness.png" src="https://github.com/sashaciocirlan/LSE---DS105L---Envision/assets/114475296/49722bff-4be9-41d9-a226-ea4f0ca754be">
</p>

   - Most songs have acousticness scores of below 0.5, which means that the most popular songs tend to have electronic production. However, there are still a significant proportion of popular songs that have acousticness scores of above 0.5, which means that acoustic songs have some popularity as well.
   - The trendline is increasing but only very slightly, which means we cannot make any meaningful conclusions about the trend of songs becoming more acoustic.

5. Instrumentalness
<p align="center">
  <img width="450" alt="Instrumentalness.png" src="https://github.com/sashaciocirlan/LSE---DS105L---Envision/assets/114475296/57443fa0-fd49-4433-bc24-63a567e072aa">
</p>

   - The vast majority of popular songs are not instrumental at all, which means that there will almost always be vocals over the music in popular songs. This makes sense as this is the standard for pop music.
   - The trendline virtually remains unchanged at close to zero, which indicates that popular songs have consistently remained non-instrumental.

6. Loudness
<p align="center">
  <img width="450" alt="Loudness.png" src="https://github.com/sashaciocirlan/LSE---DS105L---Envision/assets/114475296/1f57c240-0153-4d66-81a2-32c5f128774b">
</p>

   - Most songs are between -8 and -4 decibels which is relatively loud.
   - Trendline is slightly decreasing which means that are getting softer, but the small gradient means that we cannot say for sure if there really is such a trend.

7. Valence
<p align="center">
  <img width="450" alt="Valence.png" src="https://github.com/sashaciocirlan/LSE---DS105L---Envision/assets/114475296/63934284-3d55-4cab-b634-1050b0b00f3a">
</p>

   - Valence has the most spread amongst all of the audio features. In general, equal numbers of happy and sad songs have become popular.
   - Trendline is slightly increasing but it is just straddling 0.5. Since that is basically the average value, no real trend can be inferred regarding valence.

8. Tempo
<p align="center">
  <img width="450" alt="Tempo.png" src="https://github.com/sashaciocirlan/LSE---DS105L---Envision/assets/114475296/621ecd4d-9c2b-4bd5-8f1f-9ab8aa2bda5f">
</p>

   - The tempo of most songs tend to be relatively upbeat between 100-150 bpm (for reference, normal resting heart rate is around 60-100 bpm).
   - The trend line is slightly increasing, which could mean that popular songs are getting faster but only slightly.

9. Duration
<p align="center">
  <img width="450" alt="Duration.png" src="https://github.com/sashaciocirlan/LSE---DS105L---Envision/assets/114475296/66d176f0-f304-4fa3-9de5-b2358470a934">
</p>

   - Most of the popular songs last between 100000 and 250000 ms long (between 1:40 mins and 4:00 mins). 
   - Trendline is only slightly decreasing, but the average has still remained around 200000 ms (about 3:20 mins) over the years. The decreasing trendline aligns with the trend nowadays in pop music of songs getting shorter because of the growing popularity of streaming. This is because shorter songs are able to be streamed more times, leading to more revenue earned for artists and record companies.


<br>
<br>
<br>



![dance](https://github.com/sashaciocirlan/LSE---DS105L---Envision/assets/127428021/3ac35441-36e8-40d6-af4e-a08be05ed33d)
![energy](https://github.com/sashaciocirlan/LSE---DS105L---Envision/assets/127428021/d1d7d8d2-1007-455b-b4b3-b45bfc53b422)
![speechiness](https://github.com/sashaciocirlan/LSE---DS105L---Envision/assets/127428021/409686fd-81bf-448f-a2ca-ad0b776c997a)
![Parallelplot](https://github.com/sashaciocirlan/LSE---DS105L---Envision/assets/127428021/64f854ea-8fb2-4d94-b92a-fe5fc1d1a308)


## Challenges:


## Conclusion:
## Work Distribution
Our project was collaborative, and therefore required all of our participation and contributions in order to succeed. Although we divided group responsibilities by strengths, and therefore most efficiently, we also challenged ourselves to take on tasks that were outside of our comfort zone and provided opportunity to learn the technical, organisational and design skills required for this project.<br>

### Kim 
Kim leveraged his creative lens to design the overall aesthetic and visual appearance of the web-page. This included, but was not limited to, transposing text onto the webpage, adjusting formatting and ensuring our colour schemes and overall visual appearance was clear and accessible. Notably, we opted for a colour scheme that was blue, orange and red as this is a colour blind friendly-palette. 

### David 
David was responsible for overall direction and strategy of the project, including managing workflow, adjusting the scope, setting deadlines and ensuring the webpage told a coherent story that was in-line with our objectives and previous feedback. David also wrote portions of the web-page, including the executive summary, motivations, conclusion and next steps. 

### Toni
Toni utilised her growing expertise in coding to, in tandem with Sasha, collect, analyse and visualise data from the Billboard.Py package. Specifically, Toni drafted functions to retrieve, parse and clean the data. This ensured Sasha and Jacen could also manipulate and analyse the data. Moreover, Toni used Plotnin to visualise the data across scatterplots and parallel coordinate planes. In particular, Toni was responsible for identifying the audio features of the top ten artists' songs, per year, and comparing these audio features to the wider industry benchmarks. 

### Sasha
Sasha played an integral role in bridging the web-pages overall strategy to its technical contents. On the technical side, Sasha utilises Pandas to filter, merge and pivot the raw data to prepare it for analysis. Sasha used this technical knowledge to inform the project's scope and set realistic technical goals within the context of our group's overall motivations. Sasha also was responsible for cleaning the repository. 

### Jacen:
Jacen anchored the web-pages analysis by establishing industry benchmarks. In particular, Jacen utilised the Spotify API to investigate the audio features of the top 50 songs, per month, for the last five years. This acted as a reference point for the latter half of our investigation, in which we compared this 'benchmark' to the top ten most popular artists. Moreover, Jacen provided an excellent visual representation of this relationship in his usage of Plotnine to create a radar graph.



