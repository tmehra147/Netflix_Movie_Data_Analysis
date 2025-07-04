# Netflix_Movie_Data_Analysis
Goal
Provide an end‑to‑end exploratory data analysis (EDA) of a Netflix‑focused movie data set, uncovering patterns in genres, popularity, user ratings and release trends, and wrapping up with concise answers to five business‑style questions.
1. Dataset
Aspect	Details
Source	Local CSV (mymoviedb (1).csv)  — a snapshot originally scraped from The Movie Database (TMDb) and filtered to titles available on Netflix.
Rows / columns	~9 k titles × 12 raw features (title, overview, genres, popularity, vote_average, release_date, poster_url, language, etc.).
Time span	Earliest release <1950 → latest 2023‑24 (depending on snapshot).
Licence	TMDb personal/academic use
(add your own compliance note here).
2. Workflow at a Glance
Imports – pandas, numpy, matplotlib.pyplot, seaborn.
Data ingest – pd.read_csv(..., lineterminator='\n').
Initial reconnaissance
df.head(), df.info(), df.describe()
Null check (df.isnull().sum()) → no missing cells.
Duplicate scan → none found.
Cleaning & prep
Date parsing – convert Release_Date to datetime, extract year.
Column pruning – drop low‑signal fields (overview, poster_url, etc.).
Vote banding – custom helper categorize_col() bins vote_average into 4 buckets (not_popular → popular) using quartiles.
Exploratory visuals
sns.catplot() – bar counts for Genre distribution & for the vote‑average buckets.
plt.hist() – release‑year histogram to spot production surges.

# Conclusion
#Q1: What is the most frequent genre in the dataset
# Answer: Drama genre is the most frequent genre in our dataset and has appeared more than 14% of the times 19 others genre.

#Q2: What genres has highest votes
#Answer we have 25.5% of our dataset with popular vote(6520) . Drama again gets the highest
#popularity among fans by being having more than 18.5% of movies popularities

#Q3 What movie got the highest popularity? what's its genre?
#Answer Spider-Man: No way Home has the highest popularity rate in our dataset and it has genres of 
#Action , Adventure , and Sience fiction

#Q4 What movie got the lowest popularity? what's its genre?
#Answer: The united states thread' has the highest lowest rate in our dataset
#and it has genres of music , drama , war , sci-fi and history

#Q5: Which year has the most filmmed movies
#Answer: Year 2020 has the highest filmming rate in our dataset
