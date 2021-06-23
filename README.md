# Movie-Rating-Analysis
With this project we will get the analysis of profitable, non profitable movies along with popularity of actors and analysis of movies according to their genre.

We have the data for the 100 top-rated movies from the past decade along with various pieces of information about the movie, its actors, and the voters who have rated these movies online. In this project, we will try to find some interesting insights into these movies and their voters, using Python.

### Task 1: Reading Data
1.1: Read the Movies Data.
Read the movies data file provided and store it in a dataframe movies.

1.2: Inspect the Dataframe
Inspect the dataframe for dimensions, null-values, and summary of different numeric columns.


### Task 2: Data Analysis
Now that we have loaded the dataset and inspected it, we see that most of the data is in place. As of now, no data cleaning is required, so let's start with some data manipulation, analysis, and visualisation to get various insights about the data.

2.1: Reducing Digits
These numbers in the budget and gross are too big, compromising its readability. Let's convert the unit of the budget and gross columns from $ to million $ first.

2.2: Profit
Create a new column called profit which contains the difference of the two columns: gross and budget.
Extract the top ten profiting movies in descending order and store them in a new dataframe - top10.
Plot a scatter or a joint plot between the columns budget and profit and write a few words on what you observed.
Extract the movies with a negative profit and store them in a new dataframe - neg_profit

2.3: The General Audience and the Critics
We might have noticed the column MetaCritic in this dataset. This is a very popular website where an average score is determined through the scores given by the top-rated critics. Second, we also have another column IMDb_rating which tells the IMDb rating of a movie. This rating is determined by taking the average of hundred-thousands of ratings from the general audience.

2.4: Find the Most Popular Trios - I
Find the Most Popular Trios - II
In the previous subtask you found the popular trio based on the total number of facebook likes. Let's add a small condition to it and make sure that all three actors are popular. The condition is none of the three actors' Facebook likes should be less than half of the other two.

2.5: Runtime Analysis
There is a column named Runtime in the dataframe which primarily shows the length of the movie. It might be intersting to see how this variable this distributed. Plot a histogram or distplot of seaborn to find the Runtime range most of the movies fall into.

2.6: R-Rated Movies
Although R rated movies are restricted movies for the under 18 age group, still there are vote counts from that age group.

### Task 3 : Demographic analysis
If we take a look at the last columns in the dataframe, most of these are related to demographics of the voters (in the last subtask. We also have three genre columns indicating the genres of a particular movie. We will extensively use these columns for the third and the final stage of our assignment wherein we will analyse the voters across all demographics and also see how these vary across various genres.

3.1 Combine the Dataframe by Genres
There are 3 columns in the dataframe - genre_1, genre_2, and genre_3. As a part of this subtask, you need to aggregate a few values over these 3 columns.
First create a new dataframe df_by_genre that contains genre_1, genre_2, and genre_3 and all the columns related to CVotes/Votes from the movies data frame. There are 47 columns to be extracted in total.
Now, Add a column called cnt to the dataframe df_by_genre and initialize it to one. We will realise the use of this column by the end of this subtask.
First group the dataframe df_by_genre by genre_1 and find the sum of all the numeric columns such as cnt, columns related to CVotes and Votes columns and store it in a dataframe df_by_g1.
Perform the same operation for genre_2 and genre_3 and store it dataframes df_by_g2 and df_by_g3 respectively.
Now that you have 3 dataframes performed by grouping over genre_1, genre_2, and genre_3 separately, it's time to combine them. For this, add the three dataframes and store it in a new dataframe df_add, so that the corresponding values of Votes/CVotes get added for each genre.There is a function called add() in pandas which lets you do this. The column cnt on aggregation has basically kept the track of the number of occurences of each genre.Subset the genres that have atleast 10 movies into a new dataframe genre_top10 based on the cnt column value.
Now, take the mean of all the numeric columns by dividing them with the column value cnt and store it back to the same dataframe. We will be using this dataframe for further analysis in this task unless it is explicitly mentioned to use the dataframe movies.
Since the number of votes can't be a fraction, type cast all the CVotes related columns to integers. Also, round off all the Votes related columns upto two digits after the decimal point.

3.2: Genre Counts
Now let's derive some insights from this data frame. Make a bar chart plotting different genres vs cnt using seaborn.

# Conclusion :
In this project have the data for the 100 top-rated movies from the past decade along with various pieces of information about the movie, its actors, and the voters who have rated these movies online. With this project, we did analysis on the profitable movies, non-profitable movies and average movies. We got the data of audience and critics, we got the popularity of the actors as per facebook likes, runtime and voting on R-rated movies and we did demographic analysis where we analysed the movies according to the genre and plotted a graph to look into which genre has the highest watch amoung viewers.
