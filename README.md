Table of Contents
1.Introduction 
2.Research problems 
3.Data Set
4.Implementation
4.1 Data set
4.2 Plot
4.3 Word cloud
4.4 Data preprocessing
4.5 SVD Model
4.5.1 Top-N Predictions
4.6 KNN
4.6.1 Top-N Predictions
4.7 KNN Baseline
4.7.1Top-N Predictions
5.Conclusion
6.Future Scope


1.Introduction
Recommender system is a subclass of information system which seeks out to predict the user
ratings or preference for any given item that a user would give. A good amount of information is
required for a recommender system to give accurate results. Recommender system has various
application areas like movies, book recommendation, articles, music, product inquiry, social tags,
streaming services also use recommender systems like Netflix, Hulu, Spotify etc. to provide more
user-based results. There are also popular recommender system for specific areas like restaurants
and online dating. Recommender systems have been developed to explore research articles,
collaborators, financial services and life insurance.


2.Research Problem
The objective is to build a recommendation system for Movies; predicting the ratings of the user if whether the user had watched the movie or not. Finding the RMSE and MAE for the
recommendation system for better accuracy by minimizing the difference between the predicted and the actual rating. Recommending top-N number of movies to the user for which the results
would be most promising or accurate. With increase in personal preferences for watching movie, recommending movies have become a big market for entertainment giants like Netflix, IMDb,
Hulu etc. which is an important factor for attracting large amount of viewership across the globe.


3.Data Set
The dataset has been taken from kaggle. It includes links, movies, ratings, tags, credits and keyword files. The dataset has 100k rows of ratings with 1300 tag applications for nearly 9100
movies. On top of this the data was created by 671 users. All selected users have rated at least 20 movies.


4.Implementation
The following are the steps followed in order to implement a recommender system.

4.1 Data set
Importing data set along with the necessary libraries and checking for null values.

4.2 Plot
A bar chart is plotted to observe the number of counts for each rating. From the bar chat below it can be observed that the greatest number of ratings that were given to a movie were 4 followed by
5 and then 3.

4.3 Word cloud
A word cloud is created to visualize the genres which are most rated.

4.4 Data preprocessing
The dataset had values which were in object format, so that it was converted into integer, and subsequently removed the null values from the dataset from all the columns.

4.5 SVD Model
Created an SVD model by using surprise library. Later, calculated evaluation score and then derived the RMSE and MAE values.
After having 4 folds, the mean RMSE and mean MAE values obtained are 0.8905 and 0.6891 respectively.
Predicting the estimate score for the data. Calculating the RMSE and MAE values using SVD model.
The RMSE and MAE value obtained are 0.8964 and 0.6945 respectively.
4.5.1 Top-N Predictions
Predicting the top-n predictions with n value as 10.
The precision obtained was 0.8264 and recall was 0.0693.

4.6 KNN
While implementing KNN, the K value was taken as 10 and the benchmark was set to 3.5 to extract only those ratings which were 3.5 or above. Then finding cosine similarity and RMSE and MAE
value sequentially.
4.6.1 Top-N Predictions
Predicting the top-10 recommendations for ‘An Awfully Big Adventure’ are as follows:

4.7 KNN Baseline
In the KNN baseline, the basic steps were again followed, which were calculating RMSE and MAE values and finding the cosine similarity.
4.7.1Top-N Predictions
Predicting the top-10 recommendation for ‘An Awfullu Big Adventure’ by using KNN Baseline are as follows:
In the top 10 predictions for KNN Baseline, the precision is0.8461 and recall is 0.0801.


5.Conclusion
When considering the RMSE and MAE values, KNN Baseline gave the best results. When
considering Precision KNN gave the best result and for Recall, KNN Baseline gave best results.
Of all metrics compared KNN Baseline performed better than the others.
SVD KNN KNN Baseline
RMSE 0.8963 0.9222 0.8752
MAE 0.6944 0.7131 0.6744
Precision 0.8264 0.8703 0.8461
Recall 0.0693 0.0472 0.0801


6.Future Scope
For the future scope, clustering on the dataset can be performed based on genre. Other recommender techniques can be applied for better accurate results.
