# From Hero to Superhero: A Spotify Streaming Analysis

In this project, we performed exploratory data analysis on Spotify music streaming data in order to extract actionable insights regarding which key features differentiate ultra-popular songs from the merely popular.

## Design and Data

We begin our analysis with two tables from [Kaggle](https://www.kaggle.com/pepepython/spotify-huge-database-daily-charts-over-3-years?select=Database+to+calculate+popularity.csv).  The first (enormous) table contains the titles, artists, and unique ids for every song in the Spotify daily Top 200 most streamed, both globally and in each of 35 different countries, for every day between Jan 1, 2017 and Nov 5, 2020.   The second table contains a collection of multiple interesting features for each unique song in the first dataset. 

We used Pandas to combine the two tables into one, keeping a list of all unique songs in the USA Daily Top 200 over this time period, along with multiple interesting features (some engineered by us).  These extra engineered features include popularity metrics for each song, such as (a) the number of appearances in the Daily Top 200 and (b) the peak daily position achieved over this time period.  In order to level the playing field somewhat among songs with earlier and later release dates, we removed all songs subject to the following two filters:

- Songs with a release date prior to Jan 1, 2017.   Since pre-2017 streaming data was not available in this dataset, it is likely that our calculated "peak daily position achieved" value is less than the true all-time value for these songs.

- Songs with a release date after Jun 1, 2020.   Reasoning along similar lines as the first point above, we wanted to give all songs at least several months (through Nov 5, 2020) to achieve their peak daily position, in order to avoid systematically underestimating this important target feature.

## Tools and Algorithms

We used Pandas for data aggregation, some feature engineeering, and rudimentary [cleaning](https://github.com/andreilevin/BF_project/blob/main/spotifypandasclean.ipynb).  The bulk of the data cleaning (and some pivot table plots) were performed in Google Sheets (see the [workbook](https://github.com/andreilevin/BF_project/blob/main/myspotify.xlsx) in this repository), and the remaining data visualizations were done in Tableau (dashboard available [here]( https://public.tableau.com/app/profile/andrei.levin/viz/AndreiSpotify/Dashboard1)).  

## Communication

Our exploratory data analysis yielded several interesting takeaways, best viewed in the slide deck [here](https://github.com/andreilevin/BF_project/blob/main/AndreiPresentation.pdf).  Based on our initial analysis, we believe an machine-learning-driven extension of this initial approach could be fruitful in delivering actionable insights to musical artists and content creators looking to  increase their streaming numbers and make the figurative leap from gold to platinum.

