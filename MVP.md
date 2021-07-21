# MVP (and updated project proposal)

Having tried in vain to find a Netflix dataset suitable for my purposes (that wouldn't require a week of web scraping), I've decided to switch gears and do a project with Spotify data instead, which has a much friendlier API.   

For my project, I am analyzing the components that characterize hit songs on Spotify, as measured by streaming popularity.  The idea is to explore which factors differentiate ultra-successful songs (many days spent among the daily top 10-20 streamed) from the merely successful (occasional appearances in the daily top 200 most streamed).  The results contained in this analysis could help successful, already established artists get over the hump from star status to superstar status.

To do this, I used an extensive dataset from kaggle which contains a list of all the songs in the Daily Top 200 Streamed over a period of 3 years:   https://www.kaggle.com/pepepython/spotify-huge-database-daily-charts-over-3-years?select=Database+to+calculate+popularity.csv

I used pandas to clean and combine the multiple tables into one.  For each song that made at least one appearance in the USA Daily Top 200,  I combined many potentially helpful Spotify metrics (genre, danceability, energy, valence, etc.) with my own calculations of popularity (number of days spent in the top 20, peak daily streaming position achieved, etc.).   I ended up with a tidy dataset with ~7000 rows and ~20 columns.

Since planning, cleaning and combining took such a long time, I have not yet had much of a chance to crunch the data, plot graphs, or draw meaningful insights, but that is all coming (as soon as I get some sleep)!  You can find my excel spreadsheet at myspotify.xslx in this directory.

