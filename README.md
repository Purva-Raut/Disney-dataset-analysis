# Disney-dataset-analysis

Disney+ is one of the most popular media and video streaming platforms.
This tabular dataset consists of listings of all the movies and tv shows available on Disney+, along with details such as - cast, directors, ratings, release year,
duration, etc.Dataset link: https://www.kaggle.com/datasets/shivamb/disney-movies-and-tv-shows.
I have anlysed this dataset and answered some of the interesting questions like :'Is there any relationship between the duration of the movies/TV shows and the year 
of release?','Top countries that produce content for Disney+' etc.
I have used pandas, matplotlib, seaborn libraries learned in the Jovian course-Data Analysis with Python: Zero to Pandas for this analysis.

Steps:
#Data Preparation and Cleaning

1.Import the dataset and convert it into a dataframe using pandas. #pd.read_csv

2.Check how the dataframe looks like. #df.head()

3.Check how many rows and columns in the dataframe. #df.shape

4.Check non-null values and datatypes of of the columns in the dataframe. #df.info()

5.Check statistical information of the columns in the dataframe. #df.describe

6.Check null values count. #df.isna().sum()

7.Data wrangling- converting columns to correct datatype. eg: pd.to_datetime(df['date_added'])

8.Treating the missing values-dropna, fillna 

9.Checking and treating duplicate entries.

#Exploratory Analysis and Visualization
Use matplotlib and seaborn libraries

Histogram- for release_year
Scatterplot- To check relationship between 'duration' and 'release_year' columns

#Answered some interesting questions:
1.Find out which release_year has max no. of movies+tv shows.Then find out of them how many are movies and tv shows.
#sort_values
plotted count_plot

2.Classify movies into 4 buckets and plot them <30 min(Short), Between 30 and 60 mins(Medium), Between 60 and 120 mins(Normal),>120(Long) movies and draw inference.
Divided into buckets using operations.
plotted bar_plot

3.Extract movies listed in 'Family' genre for duration 45 to 60 mins to recommend to secondary school entertainment period. 
Make sure that the Rating is not 16+ and above and release year is 1990 and above.
split and explode
barplot

4.Find the top 10 countries with the most content on disney+
split,explode,strip
The split() method splits a string into a list.
The explode() method converts each element of the specified column(s) into a row.
The strip() method removes the whitespaces

5.Is there any relation between the no. of seasons for the TV shows and the release_year? eg: Latest release year has more or less shows comparatively?
scatterplot

#Inferences and Conclusion

In our dataset of disney+ the earliest release year is 1928 and the latest is 2021.

Most the content on the disney+ ott is after release year 2000.

Movies are from year 1940 and above whereas TV shows are from year 1980 and further.

There is no correlation between the release year and the duration of the movies or TV shows.

Between years 1950 to 1985 movies were of longer duration.

The data that we worked on had content added from OCT 2019 to NOV 2021.

Year 2021 has the maximum content of 125 out of which 70 were movies and 55 TV Shows.

Maximum movies uploaded are 1 to 2 hours long followed by short duration movies of less than 30 mins which are less than half of the normal duration movies uploaded.

30 to 60 mins and more than 120 minutes seems like a bit odd for the movie duration so these movies are less.

United States country has the maximum content on disney+ followed by other countries like UNited Kingdom, Canada etc.

It is observed that majority of the TV shows have seasons less than 5.

'The Simpsons' TV show released in year 1989 has 32 seasons.

