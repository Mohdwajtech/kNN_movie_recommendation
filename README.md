# kNN_movie_recommendation
kNN  as a kind of prediction for movies

Data Source
movie-train.csv

movie-test.csv

These have been taken (and modified) from: http://kevinmolloy.info/teaching/cs504_2017Fall/

This is a small subset of the original movielens dataset. https://grouplens.org/datasets/movielens/

Objective
To use kNN as a kind of a recommendation/prediction for movies.

Datasets
As discussed in class, you will build your model using the training data. To test your model, you will calculate predictions for each entry in the test set (a userID/movieID pair), and since you know the real rating, you can compute the difference between the two, and determine how well your method performs, as an additional exercise. In this exercise we only consider if a user has seen or not seen -- irrespective of the rating.

In other words if a userId, movieId, rating line exists, then the user has seen that movie.

Description
Consider the problem of recommending movies to users. We have M Users and N Movies. Now, we want to predict whether a given test user  x  will watch movie  y .

User  x  has seen and not seen few movies in the past. We will use  x 's movie watching history as a feature for our recommendation system.

We will use KNN to find the K nearest neighbour users (users with similar taste) to  x , and make predictions based on their entries for movie  y .

A user either had seen the movie (1) or not seen the movie (0). We can represent this as a matrix of size M×N. (M rows and N columns). We have actually used a dictionary with the keys userId and movieId to represent this matrix.

Each element of the matrix is either zero or one. If (u, m) entry in this matrix is 1, then the  uth  user has seen the movie  m .

Training set
M×N binary matrix indicating seen/not-seen.

Test set:
L test cases with  (x,y)  pairs.  x  is N-dimensional binary vector with missing  yth  entry - which we want to predict.

Exercise 1 :: Write a function to compute euclidean distance between two users for all entries except the missing  yth  entry.

We will use KNN to find the K nearest neighbour users (users with similar taste) to  x , and make predictions based on their entries for the movie  y .

We have given the code for Cosine distance, when computing nearest neighbours.


