# MovieLenks-100k Recommender System

In this notebook I make the Exploratory Data Analysis of *MovieLens-100k Dataset* and create recommending systems using kNN and SVD.

## Dataset Description

ML-100k Dataset describes 5-star rating and free-text tagging activity from MovieLens, a movie recommendation service. It is split into *u.data*, *u.item* and *u.user* files, which store data about ratings, movies and users respectively. There are 943 unique users, 1682 unique movies and 100000 ratings.

## Interesting Findings In Data Analysis

* The dataset has a small number of missing data, except for a whole column named **video release date** in *u.item*
* The dataset only has movies released at 1998 and earlier
* Star Wars is the most frequently rated movie
* Users mostly rate movies average or above average(3 and 4 respectively)

## Using kNN To Recommend Movies

We decided to use *collaborative filtering* for the dataset, since it was robust and easier to implement.

After we applied the filter to the dataset, it was not hard to train kNN and find k similar movies for our movie of interest.

The result look like a basic assumption on the person's interests.

![knn](https://imgur.com/OAaTczL.jpg)

## Matrix Factorization

To make our predictions better, we can use *Matrix factorization* some latent(hidden) features, which help us get the compact representations of user tastes and item descriptions.

We had to introduce mapping for our movies to interpret the results, since Matrix factorization reduces the number of features.

The results looked a bit more interesting

![svd](https://imgur.com/XdAlyof.jpg)