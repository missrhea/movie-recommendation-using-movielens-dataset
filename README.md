# movie-recommendation-using-movielens-dataset

The movielens dataset is used to build the recommendation system. 
The specific dataset can be downloaded using this link: http://files.grouplens.org/datasets/movielens/ml-latest.zip

Description of dataset (taken from the README.txt file in the downloaded dataset):
Summary
=======

This dataset (ml-latest) describes 5-star rating and free-text tagging activity from [MovieLens](http://movielens.org), a movie recommendation service. It contains 27753444 ratings and 1108997 tag applications across 58098 movies. These data were created by 283228 users between January 09, 1995 and September 26, 2018. This dataset was generated on September 26, 2018.

-----------------------------------------

For the purpose of this project, I will be using only these two files:
1.Movies Data File Structure (movies.csv)
---------------------------------------

Movie information is contained in the file `movies.csv`. Each line of this file after the header row represents one movie, and has the following format:

    movieId,title,genres

Movie titles are entered manually or imported from <https://www.themoviedb.org/>, and include the year of release in parentheses. Errors and inconsistencies may exist in these titles.

Genres are a pipe-separated list.

2.Ratings Data File Structure (ratings.csv)
-----------------------------------------

All ratings are contained in the file `ratings.csv`. Each line of this file after the header row represents one rating of one movie by one user, and has the following format:

    userId,movieId,rating,timestamp

The lines within this file are ordered first by userId, then, within user, by movieId.

Ratings are made on a 5-star scale, with half-star increments (0.5 stars - 5.0 stars).

Timestamps represent seconds since midnight Coordinated Universal Time (UTC) of January 1, 1970.

-----------------------------------------

This jupyter notebook includes the following:
1. Loading the data into dataframes/

2. Exploring the data values to gain a better understanding of it. Do this by using statistical measures like the average and with the help of graphs like the histogram to visualize the data.

3. Now build the recommendation system. 
   The (simplistic) problem statement is: Given that user X has watched movie Y and rated it 5 stars,    we recommended a movie Z, such that other users that watched Y and rated it 5 stars also watched      movie Z and rated it 5 stars.  
   
4. To measure the likelihood that movie Z will be recommended, find the correlation between 2 movies    across the user ratings. This will answer the questions, "users who watched movie Y are most          likely to watch movie Z". 
