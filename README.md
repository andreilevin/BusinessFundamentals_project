# A Spotify Streaming Analysis

In this project for the Metis "Business Fundamentals" module, I performed exploratory data analysis on Spotify music streaming data in order to extract actionable insights regarding which key features differentiate ultra-popular songs ("superheroes") from the merely popular ("heroes").  Such a data-driven approach to generating insights could help musical artists and content creators looking to  increase their streaming numbers and make the figurative leap from gold to platinum. 

### Project Presentation [Slides](https://github.com/andreilevin/BF_project/blob/main/AndreiPresentation.pdf): 

[![AndreiPresentation.pdf:](https://raw.githubusercontent.com/andreilevin/BF_project/main/cover_screenshot.jpg)](https://github.com/andreilevin/BF_project/blob/main/AndreiPresentation.pdf)

## Project Design

I began my analysis with two tables from [Kaggle](https://www.kaggle.com/pepepython/spotify-huge-database-daily-charts-over-3-years?select=Database+to+calculate+popularity.csv).  The first (enormous) table contains the titles, artists, and unique ids for every song in the Spotify daily Top 200 most streamed, both globally and in each of 35 different countries, for every day between Jan 1, 2017 and Nov 5, 2020.   The second table contains a collection of multiple interesting features for each unique song in the first dataset. 

I combined the two tables into one, keeping a list of all unique songs in the USA Daily Top 200 over this time period, along with multiple interesting features for each song (including some engineered by me).  These extra engineered features include song popularity metrics such as the number of appearances in the Daily Top 200 over this time period and the peak daily position achieved.  In order to level the playing field somewhat between songs with earlier and later release dates, I removed all songs subject to the following two filters:

- Songs with a release date prior to Jan 1, 2017.   Since pre-2017 streaming data was not available in this dataset, it is likely that our calculated "peak daily position achieved" value is less than the true all-time value for these songs.

- Songs with a release date after Jun 1, 2020.   Reasoning along similar lines as the first point above, I wanted to give all songs at least several months (through Nov 5, 2020) a chance to achieve their peak daily position, in order to avoid systematically underestimating this important target feature.  This decision (to keep songs released in the first 6 months of 2020) has the added bonus that any by-year aggregation data for 2020 can just be doubled if we wish to compare it to the other three years in an apples-to-apples way.

## Tools 

* Pandas for data aggregation, some feature engineeering, and rudimentary cleaning
* Google Sheets for cleaning and pivot tables (see the [workbook](https://github.com/andreilevin/BF_project/blob/main/myspotify.xlsx) in this repository), 
* Tableau for data visualization
