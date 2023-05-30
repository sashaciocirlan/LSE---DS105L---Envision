---
title: "Tuning Into Your Music"
date: 20 March 2023
date-meta: 20 March 2023
---

# _Leader or Follower_: Exploring the Relationship Between Popular Artists and Music Trends

<p align="middle">
  <img src="https://github.com/sashaciocirlan/LSE---DS105L---Envision/assets/114475296/5be08ffe-45cc-463a-935f-53e407d0f411" width="450" />
  <img src="https://github.com/sashaciocirlan/LSE---DS105L---Envision/assets/114475296/00b05c11-fd30-4838-a0cc-6da5a4f3ad22" width="365" /> 
</p>


## 🏠 Team Members

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
* Analysing the **top 10 artists** over the past **5 years** using the **Billboard's Hot 100** chart. 
* Collecting data on the **audio features** of the **top 50 songs per month** during this period. 
* Examining the **audio features** of the top ten **artists' songs** over the past five years.
* Establishing **industry benchmarks** by calculating average values and standard deviations or ranges of audio feature categories. This identifies the audio features that experienced the most and least change over time. 
* Comparing the analysis from Step 4 to the audio features of the top ten artists' songs, using **visualisations** like **scatter plots** and **radar graphs** to represent the findings.

▶️ The findings hold significance for artists, industry professionals, and streaming platforms. Understanding evolving audio feature preferences and artist popularity informs decision-making for song production, marketing, and playlist curation. Exploring correlations between audio feature trends and popular music trends contributes to predicting future music preferences and shaping the industry's direction.

▶️ In conclusion, this project harnessed data from streaming platforms to investigate the impact of streaming services on the music industry. By analysing audio features and artist popularity, valuable insights were gained into the evolution of music preferences and potential connections with overall trends. These findings offer practical implications for decision-making in the music industry and contribute to its growth and success.

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
* Billboard via [Python Package](https://pypi.org/project/billboard.py/) 
* Spotify via [Spotify API](https://developer.spotify.com/documentation/web-api) 

## 📊 Exploratory Data Analysis
### Billboard Python Package
🔝 We conducted an analysis of Billboard's "Billboard Hot 100" chart, which is a weekly music chart that ranks the 100 most popular songs in the United States based on multiple factors. Our objective was to investigate the Top 10 artists over the past cumulative 5 years. <br>

▶️ To gather the necessary data, we utilised a Python Package called Billboard.py. The data collection process spanned from May 24, 2018, and continued on a weekly basis for a period of 5 years. We used songs instead of entire albums as songs were more accessible and heterogeneous in terms of coverage (happy, sad, danceable, energetic, etc.)
<br>
Please refer below to see the historical Top 10 artists we obtained using the Billboard.py package - it will be essential in the analysis <br>
<p align="middle">
  <img width="484" alt="Screenshot 2023-05-29 at 12 32 09" src="https://github.com/sashaciocirlan/LSE---DS105L---Envision/assets/12870658/54f6ef69-a7f6-4d7f-97d0-b0bee2ea9404">
</p>

### Data Cleaning and Visualisation

#### Billboard package
Below shows a cleaned data frame, sorted artists by rank in charts, renamed columns, which made them easier to work with in future visualisations.<br>
<p align="middle">
 	<img width="650" alt="Billboard Data Visualisation.png" src="https://github.com/sashaciocirlan/LSE---DS105L---Envision/assets/114475296/be9c08c7-d2e4-4b7b-8125-df422bdfc3d5">
	<img width="650" alt="Billboard Data Cleaning.png" src="https://github.com/sashaciocirlan/LSE---DS105L---Envision/assets/114475296/cee5feaf-02f7-4a76-9e24-333772712425">
  
</p>



### Spotify API
In a similar vein, we utilised the Spotify API to analyze the audio features of the top 50 songs per month over the past five years. Specifically, we focused on the "Weekly Top Songs Global" chart, which Spotify generates every Thursday and showcases the 200 most streamed songs worldwide for that week. Our data collection process also commenced on May 24, 2018, and we observed a total of 66 charts, corresponding to a frequency of one chart every four weeks over a span of five years. To obtain the necessary audio features, we leveraged the "Get several tracks' audio features" request within the Spotify API. This enabled us to acquire the audio features of up to 100 tracks at a time. As a result, we were able to gather comprehensive information about the audio characteristics of the top songs.
Below, you will find a screenshot from Microsoft Excel showcasing an example of the Spotify CSV Files, displaying the most-streamed songs during the week of May 24, 2018.
<br>
<p align="middle">
  <img src="https://github.com/sashaciocirlan/LSE---DS105L---Envision/assets/114475296/6c226c5d-d392-4b7c-8f4f-ec104415ed68" width="1300"/>
</p>
<br>

📇 Here is a function that will find an artist’s Spotify ID using Spotify API. To get data about artists (like the audio features of their songs) you first need to get their artist ID. Rather than searching for this manually, this function does get the ID when the artist’s name is entered.  <br>
<img width="423" alt="image" src="https://github.com/sashaciocirlan/LSE---DS105L---Envision/assets/127428021/30ed24db-fc78-4826-ab99-5e33280506bf">

📇 Here is a function that gathers the artist’s songs, albums, and release dates and outputs them.  All that needs to be entered is the artist’s Spotify ID, then the function proceeds to get the information. The variable “trim_name” is used to make sure there are no duplicate albums being outputted.<br> 
<img width="452" alt="image" src="https://github.com/sashaciocirlan/LSE---DS105L---Envision/assets/127428021/9c66b91e-4054-4498-a4d7-53de3025e6ff">


When we calculated the average audio features for each artist the data came back messy. Each audio feature had results that had a variety of different decimal places. To make the data presentable and easy to read, each result was rounded to 3 decimal places.<br>
<img width="452" alt="image" src="https://github.com/sashaciocirlan/LSE---DS105L---Envision/assets/127428021/936bb3af-aad8-4501-ba9d-e6885b87b7b4">



#### Audio Features
We followed the definition of audio features provided by [Spotify Developer Documentation](https://developer.spotify.com/documentation/web-api/reference/get-several-audio-features): <br>


🕺 **Danceability**: How suitable a track is for dancing based on a combination of musical elements including tempo, rhythm stability, beat strength and overall regularity. 

	number[float] 

⚡️ **Energy**: A perceptual measure of intensity and activity. Typically, energetic tracks feel fast, loud and noisy. Perceptual features contributing to this attribute include dynamic range, perceived loudness, timbre, onset rate, and general entropy. 

	number[float] 

🎼 **Instrumentalness**: This predicts whether a track contains no vocals. ‘Ooh’ and ‘aah’ sounds are treated as instrumental in this context. Rap or spoken words are clearly ‘vocal’. Values above 0.5 are intended to represent instrumental tracks but confidence is higher as the value approaches 1.0 

	number[float] 

🖖 **Liveness**: Detects the presence of an audience in the recording. A value above 0.8 provides strong likelihood that the track is live. 

	number[float] 

📢 **Loudness**: The overall loudness of the track in decibels (dB). Loudness values are averaged across the entire track. Loudness is the quality of a sound that is the primary psychological correlate of physical strength (amplitude). Values range between -60 and 0 dB. 

👂 **Acousticness**: A confidence measure from 0.0 to 1.0 of whether the track is acoustic. 

	number[float] 

💬 **Speechiness**: Detects the presence of spoken words in a track. Values above 0.66 describe tracks that are probably made entirely of spoken words. Values between 0.33 and 0.66 describe tracks that may contain both music and speech, either in sections or layered, including such cases as rap music. 

	number[float] 

💨 **Tempo**: The overall estimated tempo of a track in beats per minute (BPM). In musical terminology, tempo is the speed or pace of a given piece and derives directly from the average beat duration. 

	number[float] 

😹 **Valence**: The musical positiveness conveyed by a track. Tracks with high valence sound more positive (e.g. happy, cheerful and euphoric), while tracks with low valence sound more negative (e.g. sad, depressed, angry). 

	number[float] 

⏳ **Duration**: The duration of the track in milliseconds. 

	Integer 

All features, barring **Duration** and **Loudness**, utilise a scale of 0 to 1, with 0 being least (e.g. lowest possible speechiness) and 1 being most (e.g. highest possible speechiness). 



## 💪🏼 Data Collection Challenges
Throughout the data collection section of our investigation our team encountered several challenges. However, through diligent problem-solving and collaboration, our team successfully devised solutions for each of these challenges.<br>

😰 Challenge|✅ Solution|📈 Outcome
:---|:---|:---
One major hurdle was the absence of a direct Billboard API, which was terminated in May 2013. Therefore, we could not retrieve the aggregated data or directly use Billboard's resources for aggregation.|We found a Python package, Billboard.py, on StackOverflow which helped us aggregate the data. With this, we could identify the ten artists with the most entries on the weekly charts over the past five years.|This underlined the value of leveraging existing solutions to overcome data analysis problems and avoid needing to reinvent the wheel. Forums like StackOverflow are particularly helpful for this.
Directly searching for the most popular artists was not possible as the Billboard Hot 100 features popular songs rather than individual artists.|We incorporated an extra step of identifying the artist behind each entry, and then we summed up all artists' songs total number of entries throught 5 years (52 Top 100 charts/year) |We got a strong indicator of the top 10 artists in the past 5 years (e.g. Drake has over 800 total entries in all charts) and we used the Top 10 list we compiled as a baseline for further analysis.
Spotify's weekly charts did not provide easy access to their historical data, making it challenging for us to collect the required information.|After extensive research, we discovered that Spotify's historical data was stored in CSV files. Therefore, we manually downloaded the CSV files and imported them into pandas dataframes for analysis.|This process taught us a valuable lesson about the accessibility of data. It served as a reminder that data is often not readily available and may require substantial effort to obtain. Additionally, we recognized the importance of data transformation when working with diverse data sources, as traditional organisations may employ storage formats that are less convenient but contain vital data, that data scientists have to work with while conducting analysis or transitioning an organisation to a more modern data storage method. 
We encountered a collaboration issue as there was a misalignment in our variable names and general code style. This lack of coherence in our functions between group members initially prevented us from collecting the data. For instance, one collaborator used the variable name 'Artist' while another used 'Top Ten Artist'.|To resolve this issue, we carefully reviewed and adjusted the variable names to ensure consistency. This enabled us to successfully execute the code.|Although seemingly minor, we argue that this is a common yet deceptively difficult challenge faced by data scientists when collaborating. As a result, we adopted a practice of establishing a baseline 'style' at the beginning of each collaborative coding session, which greatly streamlined the process.


## 🧐 Data Analysis

### Determining Industry Benchmarks
We have successfully gathered data on the audio features of individual songs spanning the past 5 years. Our aim now is to consolidate this information into an **Industry Benchmark** that offers a comprehensive view of the sound characteristics prevalent in the most popular songs. To accomplish this, we have computed weighted averages for each audio feature.

The calculation process entails multiplying the value of each song's audio feature by the number of streams it received within a specific week. Subsequently, we aggregate the feature values for the top 50 songs and divide the sum by the total number of streams accumulated by those songs in that particular week. This methodology ensures that songs with higher streaming figures exert a more significant influence on the weighted average, resulting in a value that better reflects the listening habits of the audience.

Consequently, the final dataframe encompasses both the initial sections of data and the consolidated industry benchmark. Below, you will find a preview of the resulting dataframe, displaying its heads and tails.
<p align="middle">
  <img src="https://github.com/sashaciocirlan/LSE---DS105L---Envision/assets/114475296/925fb4be-424f-4919-8796-406679c29430" width="500" />
</p>

### Comparison
After calculating weighted averages for each chart, we aim to obtain an overall understanding of the entire 5-year period by calculating the mean of all 66 values for each audio feature. This aggregated data is the aforementioned **Industry Benchmark** or the overall weighted average.

Next, utilising the previously computed average values for the audio features of each artist, we proceed to subtract each artist's values from the overall weighted average of the most popular songs. This process allows us to gauge the divergence of each artist from the general music industry. A value of 0 indicates that the artist aligns with the industry benchmark established by the most popular songs. Conversely, the further a value deviates from 0, the more distinct the artist is from the most popular songs.

Below is the dataframe displaying these values: 
<p align="middle">
  <img src="https://github.com/sashaciocirlan/LSE---DS105L---Envision/assets/114475296/6b20dafd-7089-4b5d-b3d0-e308b9371117" width="500" />
</p>

## 📑 Data Visualisation

![dance](https://github.com/sashaciocirlan/LSE---DS105L---Envision/assets/127428021/3ac35441-36e8-40d6-af4e-a08be05ed33d)
Scatterplot which depicts the average danceability of the top 10 artists’ songs. Their scores are quite varied suggesting there is not a common trend in danceability for successful artists. However, the majority are above 0.5 which suggests danceable music is more popular.

![energy](https://github.com/sashaciocirlan/LSE---DS105L---Envision/assets/127428021/d1d7d8d2-1007-455b-b4b3-b45bfc53b422)
Scatterplot which depicts the range of top artists average energy in their songs.  There’s more of a correlation than danceability, which suggests an energy score at around 0.6 correlate to a song being more popular. Also shows popular artists tend to have more energetic music as everyone apart from Billie Eilish has an average greater than 0.5.

![speechiness](https://github.com/sashaciocirlan/LSE---DS105L---Envision/assets/127428021/409686fd-81bf-448f-a2ca-ad0b776c997a)
The results are very varied on the graph, inidicating there's a big difference in the speechinesss of the top artist's songs. However, all of the results are below 0.3, signifying that listeners do not enjoy wordy songd.


<br>
<br>
<br>

### Plotting into Dataframe

To visualise how the audio features of the most popular songs have changed over time, or lack thereof, scatter plots with trend lines were created using the plotnine package. Each scatter plot shows all the values of one audio feature for all of the songs that have been analysed (i.e. top 50 songs every 4 weeks for 5 years). <br>

1. Danceability
<p align="center">
  <img width="450" alt="Danceability.png" src="https://github.com/sashaciocirlan/LSE---DS105L---Envision/assets/114475296/ce25d581-ea4e-4c4f-8db2-c5bc99e55b5b">
</p>

   - The danceability scatter plot shows that most of the top songs have a value of more than 0.5, which indicates that popular songs tend to be danceable.
   - However, the trendline in red is slightly decreasing. The gradient shows that songs are becoming slighlty less danceable.

2. Energy
<p align="center">
  <img width="450" alt="Energy.png" src="https://github.com/sashaciocirlan/LSE---DS105L---Envision/assets/114475296/3e86c41f-645b-4249-9cc9-4e95bc11f943">
</p>

   - Similarly, most popular songs tend to be energetic, with most songs having energy scores of above 0.5. 
   - Here, the trend line is increasing so we can cautiously observe that songs are becoming more energetic over time.  

3. Speechiness
<p align="center">
  <img width="450" alt="Speechiness.png" src="https://github.com/sashaciocirlan/LSE---DS105L---Envision/assets/114475296/72cfa4f2-cf6d-421f-b456-6bf05613c4d8">
</p>

   - Almost all of the songs have speechiness scores of below 0.5, with only 3 points on the scatter plot being above 0.5. This indicates a very strong likelihood that a popular song would definitely have more music and singing than spoken word.
   - The trendline is going down slightly, and visually there are fewer songs with scores above 0.3 as time passes. This indicates that such songs (like rap songs) could be getting less popular over time.

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
   - The trend line is slightly increasing, which could mean that popular songs are getting faster.

9. Duration
<p align="center">
  <img width="450" alt="Duration.png" src="https://github.com/sashaciocirlan/LSE---DS105L---Envision/assets/114475296/66d176f0-f304-4fa3-9de5-b2358470a934">
</p>

   - Most of the popular songs last between 100000 and 250000 ms long (between 1:40 mins and 4:00 mins). 
   - Trendline is only slightly decreasing, but the average has still remained around 200000 ms (about 3:20 mins) over the years. The decreasing trendline aligns with the trend nowadays in pop music of songs getting shorter because of the growing popularity of streaming. This is because shorter songs are able to be streamed more times, leading to more revenue earned for artists and record companies.

📊 To present this data visually, we created a radar chart using the _plotly_ Python package. However, since the radar chart necessitated uniform measurement scales for all categories (i.e., audio features), we excluded loudness, tempo, and duration from the data due to their disparate measurement units (loudness in decibels, tempo in beats per minute, and duration in milliseconds). All other features were scaled between 0 and 1 for consistency. <br> 

The resulting radar chart is as follows: <br>
<img width="800" alt="Radar_Chart.png" src="https://github.com/sashaciocirlan/LSE---DS105L---Envision/assets/114475296/2d5ee9d4-9bc4-4ecd-bf66-ac5da49460cb">

On the radar chart, a value of 0 means that the average value of the audio feature for an artist is the same as that of the most popular songs. For example, the danceability of this artist’s songs is at the same level as the most popular songs of the past 5 years. This means that as an artist’s value moves further away from 0, their songs increasingly differ from the most popular songs of the past 5 years.<br>

👉 In general, the plot shows that most of these artists’ values hover around 0 across all audio features, which means that their music closely matches the type of music that has remained popular over the past 5 years. The audio features that appear to have the least deviation across artists include instrumentalness, danceability, and speechiness. For some audio features, there are a few significant outliers that demonstrate their difference from the current music landscape.<br>

👉 The artist that appears to have the most deviation from the most popular songs is Billie Eilish. Her acousticness score is almost 0.6 higher than the most popular songs, and her energy score is about 0.4 lower as well. This means that her music tends to be a lot more acoustic and less energetic than a typical song one would hear on the radio today.<br>

👉 Other artists that appear to have visually significant deviations from the most popular songs include Lil Baby and DaBaby, whose songs have a speechiness score of about 0.2 more than the rest. This makes sense as they are rappers, which explains why there would be more spoken word in their songs. While Drake and Doja Cat, who are also in the top 10 artists list, are also rappers, their most popular songs over the past 5 years have been more pop than rap, as they sing more frequently than rap. That could explain why even though they both have the next-highest speechiness scores, they remain quite close to the overall average set by the most popular songs.

## 🕛 Conclusions: 

Successful artists, while following certain industry benchmarks, also introduce their own unique elements that have the potential to influence future music trends.

#### Acoustic & Instrumental Trends:
Interestingly, our investigation discovered a distinct anomaly - Billie Eilish's music showcases a significantly higher degree of acousticness and instrumentalness compared to industry norms. Eilish's innovative blend of acoustic textures and experimental instrumentals might be indicative of a renaissance of these elements in popular music. Although the industry currently leans towards electronic production, Eilish's success could inspire other artists to revisit and redefine the role of acoustic and instrumental elements in their music, leading to a gradual resurgence of these features.

#### Speechiness Trends:
DaBaby and Lil Baby, scored unusually high in terms of speechiness, suggesting a higher degree of spoken words in their songs compared to typical popular music. This divergence might signal an ongoing evolution of the genre, as artists increasingly blend musical and spoken elements to engage listeners in new ways. Looking forward, this could mean an expansion of the stylistic boundaries of popular music, with the increased integration of spoken word elements, particularly in genres like hip-hop and rap.

#### Danceability & Tempo Trends:
With the rising trends of danceability and tempo across the industry, it's evident that artists like Doja Cat, Drake, and Post Malone, who already align with these benchmarks, are effectively tapping into listeners' preferences for energetic and upbeat music. This suggests that the emphasis on creating music that is rhythmically engaging and uplifting will continue to grow, shaping the future sound of popular music.

#### Valence Trends:
Taylor Swift's consistent success with high-valence songs, those provoking feelings of positivity, underscores listeners' ongoing affinity for music that stimulates uplifting emotions. This could lead to an increasing number of artists incorporating more optimistic themes into their music, fueling the trend towards higher valence scores.

#### Duration Trends: 
The shrinking duration of songs shows that brevity is the new norm in the music industry. As streaming platforms dominate, artists are looking to maximize streams and revenue by delivering shorter songs that pack a punch.

#### The Future of Music:
In essence, this in-depth study suggests that the future of popular music is set to be an exciting blend of innovation and adaptation. It's likely that artists will continue to experiment with their music by pushing genre boundaries, revisiting traditional elements, and amplifying the emotional resonance of their songs.

However, they will also have to strike a balance with prevailing industry trends, aligning their music with the evolving preferences of listeners. As we continue to move forward, the artists who can best navigate this delicate balance of tradition and innovation will shape the future landscape of popular music, leaving their unique imprint on the evolving rhythm of the industry.

### ❔ Limitations:
Our study was insightful, but it also had some inherent statistical limitations.

1. Sampling Bias: The choice to focus on the top 10 artists from the Billboard Hot 100 is a convenience sampling method, which is prone to bias. These artists are not necessarily representative of all artists in the music industry. Future analyses could benefit from a random sampling approach across a wider range of artists.

2. Temporal Scope: Our data covers a span of several years, yet this might not be enough to detect long-term trends. The music industry is greatly influenced by broader cultural shifts that can take decades to manifest.

3. Variable Selection: We only considered several audio features in our analysis. Other potential predictors of song popularity were not included in the study due to data constraints, such as lyrics, promotional activities, collaborations, and the artist's public image.

4. Statistical Significance: While we identified some trends and made comparisons between the top 10 artists and industry benchmarks, we did not perform statistical tests to confirm the significance of these differences. Thus, the observed differences might be due to random variation rather than a true difference.

5. Causality: Our study is observational in nature. Even though we can identify associations between the top artists' songs and their alignment with the industry benchmarks, we can't establish causality. For instance, we can't definitively say whether the songs are popular because they align with industry trends or whether the artists' success causes those trends.

6. Addressing these limitations in future research would involve expanding the scope of data collection, employing more robust statistical techniques, and adopting a more comprehensive research design to control for potential confounding variables. Such improvements would bolster the robustness of our findings and offer a deeper understanding of the forces shaping trends in the music industry.

## 🌟 Next Steps: 

We know that our analysis only scratches the surfaces of an ever-changing and fascinating industry that we all love - music. As we move forward we aim to continue to develop our skills acquired in DS105 and leverage them to learn new insights about music and maybe achieve our initial ambitious goals to create a ML model =) 

What could we do in the future? 

1. Investigate artist influence on industry trends: We could perform a more in-depth analysis on our top 10 artists and determine if their music has had a noticeable impact on the industry benchmarks. Do these artists inspire a change in the music scene, or are they successful because they closely align with the benchmarks? Identifying songs and artists that deviated from the norm before it became popular could help answer these questions.

2. Understand trends in less successful artists: We could also examine the characteristics of lower-rated artists. Are they following the trends set by the industry, or are they trying to innovate in different ways? Comparing their music features with those of successful artists could reveal interesting patterns and insights.

3. Temporal analysis of artist adaptation: Another interesting angle could be to track the evolution of artists over time. Do artists adapt their music to fit the evolving industry benchmarks, or do they maintain a consistent style regardless of the industry's trends?

4. Predictive modelling: Based on our current findings and further explorations, we could attempt to build a model that predicts the success of a song based on its audio features. This would be a significant step forward in understanding what makes a song popular.

The overarching aim would be to delve deeper into the dynamics between individual artist success and industry-wide trends. Is it the case of the industry shaping the artist, or the artist shaping the industry, or perhaps a bit of both? The intriguing interplay between the individual and the collective presents a rich seam of exploration for our next steps in this research project.

To be continued...

## 🏀 Work Distribution
Our project was collaborative, and therefore required all of our participation and contributions in order to succeed. Although we divided group responsibilities by strengths, and therefore most efficiently, we also challenged ourselves to take on tasks that were outside of our comfort zone and provided opportunity to learn the technical, organisational and design skills required for this project.<br>

### Kim 
Kim leveraged his creative lens to design the overall aesthetic and visual appearance of the web-page. This included, but was not limited to, transposing text onto the webpage, adjusting formatting and ensuring our colour schemes and overall visual appearance was clear and accessible. Notably, we opted for a colour scheme that was blue, orange and red as this is a colour blind friendly-palette. 

### David 
David was responsible for overall direction and strategy of the project, including managing workflow, adjusting the scope, setting deadlines and ensuring the webpage told a coherent story that was in-line with our objectives and previous feedback. David also wrote portions of the web-page, including the executive summary, motivations, conclusion and next steps. 

### Toni
Toni utilised her growing expertise in coding to, in tandem with Sasha, collect, analyse and visualise data from the Billboard.Py package. Specifically, Toni drafted functions to retrieve, parse and clean the data. This ensured Sasha and Jacen could also manipulate and analyse the data. Moreover, Toni used Plotnine to visualise the data across scatterplots and parallel coordinate planes. In particular, Toni was responsible for identifying the audio features of the top ten artists' songs, per year, and comparing these audio features to the wider industry benchmarks. 

### Sasha
Sasha played an integral role in bridging the web-pages overall strategy to its technical contents. On the technical side, Sasha utilises Pandas to obtain, filter, merge and pivot the raw data to prepare it for analysis. Sasha used this technical knowledge to inform the project's scope and set realistic technical goals within the context of our group's overall motivations. Sasha also was responsible for cleaning the repository and the website. 

### Jacen
Jacen anchored the web-pages analysis by establishing industry benchmarks. In particular, Jacen utilised the Spotify API to investigate the audio features of the top 50 songs, per month, for the last five years. This acted as a reference point for the latter half of our investigation, in which we compared this 'benchmark' to the top ten most popular artists. Moreover, Jacen provided an excellent visual representation of this relationship in his usage of ggplot to create a radar graph.


