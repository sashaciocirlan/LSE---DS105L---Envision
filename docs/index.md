---
title: "Tuning Into Your Music"
date: 20 March 2023
date-meta: 20 March 2023
---

# "Tuning into your tastes": Exploring popular song features and trends

**Team members:** 

- [Sasha Ciocirlan](): I'm Sasha, a final-year Politics and Economics student at the LSE. Although I'm not your typical number-cruncher, I've taken a detour into data science and found a new passion, and am bringing a deep love for music to the project.


- [Jacen](): I'm Jacen, a first-year Politics and Data Science student who secretly wishes there was a degree in Pop Music [with Data Science]. You will rarely find me without my earphones, which have recently been blasting Kylie Minogue and K-Pop stars Le Sserafim.
- [Toni Byfield](): I'm Toni, a second-year economics student. I enjoy coding and love music. I've recently been hooked on the Cults, a favourite is 'Gilded Lily'. Check 'em out!
- [David Bredin](): I'm David, a final-year Politics student at the LSE. I've developed a strong interest in Big Data, and spent time in strategy at a start-up utilising AI to automate MRI annotations. With DS105, I've dug into the technical side of data science and I'm hooked! 

- [HyeongJu Kim](): I'm HyeongJu, a first year student at LSE, pursuing a degree in Politics and Data Science. The raw emotion and storytelling embedded in rap captivate me, and I believe there is a profound connection between the world of politics and the lyrical power of hip-hop!
<img width="100" alt="Kim.png" src="https://github.com/sashaciocirlan/LSE---DS105L---Envision/assets/114475296/b887141d-88df-4521-8b82-837a49c9a346">

## 📝 Project Description
This project utilized data from streaming platforms' APIs, including Spotify and Billboard, to examine the influence of streaming services on the music industry. The project aimed to understand the evolution of audio features, changes in artist popularity, and potential correlations between audio feature trends and popular music trends.<br>
Through five key steps, the project explored these aspects. Step 1 involved analyzing the top 10 artists over the past 5 years using Billboard's Hot 100 chart. Step 2 focused on collecting data on the audio features of the top 50 songs per month during this period. Step 3 examined the audio features of the top ten artists' songs over the past five years.In Step 4, industry benchmarks were established by calculating average values and standard deviations or ranges of audio feature categories. This identified the audio features that experienced the most and least change over time. Finally, in Step 5, the analysis from Step 4 was compared to the audio features of the top ten artists' songs, using visualizations like scatter plots and radar graphs to represent the findings.<br>
The findings hold significance for artists, industry professionals, and streaming platforms. Understanding evolving audio feature preferences and artist popularity informs decision-making for song production, marketing, and playlist curation. Exploring correlations between audio feature trends and popular music trends contributes to predicting future music preferences and shaping the industry's direction.<br>
In conclusion, this project harnessed data from streaming platforms to investigate the impact of streaming services on the music industry. By analyzing audio features and artist popularity, valuable insights were gained into the evolution of music preferences and potential connections with overall trends. These findings offer practical implications for decision-making in the music industry and contribute to its growth and success.


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

#### Step 1
In Step 1, our objective was to investigate the top 10 artists of the past 5 years using Billboard’s weekly ‘Billboard Hot 100’ chart. Below is a cropped screenshot of the Billboard chart.<br>
<img src="./Billboard Chart.png" style="height:45%;width:65%">

Challenge|Solution|Outcome
:---|:---|:---
A major hurdle we faced was the absence of a direct Billboard API to access the required data. In fact, the Billboard API was officially terminated in May 2013. As a result, we couldn't retrieve the aggregated data or directly aggregate it through Billboard's resources.<br>Our direct search for the most popular artists proved unsuccessful since the Billboard Hot 100 primarily features popular songs rather than individual artists.|Fortunately, we discovered a Python package called Billboard.py that proved instrumental in creating code to aggregate the data. This enabled us to identify the artists with the most entries on the weekly charts over the past five years.<br>However, we identified a strong correlation between the number of songs an artist had entered and their popularity. For example, Drake had 800 songs entered over the five-year period.|This challenge provided valuable insight into the importance of seeking out existing solutions to overcome problems in data analysis.<br>This challenge deepened our understanding of the nature of imperfect data and the necessity to make justifiable statistical leaps when drawing conclusions, a common task for data scientists.

Refer to below for our obtained historic trend from Billboard.py<br>
<img width="484" alt="Screenshot 2023-05-29 at 12 32 09" src="https://github.com/sashaciocirlan/LSE---DS105L---Envision/assets/12870658/54f6ef69-a7f6-4d7f-97d0-b0bee2ea9404">


#### Step 2
In Step 2, our objective was to investigate the audio features of the top 50 songs per month over the past five years.

Challenge|Solution|Outcome
:---|:---|:---
Spotify's weekly charts did not provide easy access to their historical data, making it challenging for us to collect the required information.|After extensive research, we discovered that Spotify's historical data was stored in CSV files (insert photo). Therefore, we manually downloaded the CSV files and imported them into pandas dataframes for analysis.|This process taught us a valuable lesson about the accessibility of data. It served as a reminder that data is often not readily available and may require substantial effort to obtain. Additionally, we recognized the importance of data transformation when working with diverse data sources, as traditional organizations may employ storage formats that are less convenient but contain vital data, that data scientists have to work with while conducting analysis or transitioning an organization to a more modern data storage method. 

Below is a screenshot of our Spotify CSV File from Microsoft Excel.<br>
<img src="./CSV File.png" style="height:65%;width:65%">



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





## 📊 Data

## 📈 Analysis

## 🖼️ Results

## 🖋️ Conclusions

## 📚 References
