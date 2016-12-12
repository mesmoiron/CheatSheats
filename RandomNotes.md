# Cheat sheet of practical remarks found elsewhere
ML = machine learning, DS = data science, ST = statistics

* Generally we expect the accuracy to increase on adding variables. (ML)
  * Feature Engineering: dereive new information and try to predict those.
  * Better modeling techniques. Let’s explore this next.

### Regression
Regression is to build a function of __independent variables__ (also known as predictors) to predict a __dependent variable__ (also called __response__)

### Logistic Regression
Logistic regression is used to predict the probability of occurrence of an event by fitting data to a logistic curve.

### Generalized Linear Regression
The generalized linear model (GLM) generalizes linear regression by allowing the linear model to be related to the response variable via a link function and allowing the magnitude of the variance of each measurement to be a function of its predicted value.

It unifies various other statistical models, including linear regression, logistic regression and Poisson regression

### Non-linear Regression
Fit a curve through data.

## Clustering
* k-means is similar to k-medoids
* k-means cluster is represented with its center in the k-means algorithm
* k-mean tends to find clusters with sphere shape and with similar sizes
* k-medoids cluster is represented with the object closest to the center of the cluster
* k-medoids is more robust than k-means in presence of outliers

* PAM(Partioning Around Medoids) is inefficient for large datasets
* CLARA algorithm can be used instead
* DBSCAN Density-based clustering for numeric data is to group objects into one cluster if they are connected to one another by densely populated area

* Dense point = number of points of point alpha is no less than minimum number of points
* All the points in its neighborhood are __density-reachable__ from alpha and are put into the same cluser as alpha

* Density-based clustering can discover clusters with various shapes and size and is insentive to noise

### Interpreting results
* Depends on the target problem
* Domain knowledge
* Experience

## plots
* 2 dimensional clusplots where lines show the distance between clusters
* silhouette plots
  * large s (almost 1) suggests that the corresponding observations are very well clustered
  * small s (around 0) means that the observation lies between two clusters
  * negative s observations are probably in the wrong cluster

## Outlier detection
* Univariate outlier detection
* Multivariate outlier detection
* LOF (Local Outlier Factor)
* Outlier detection by clustering
* Outlier detection from time series

### Univariate
* Use boxplot(function)

### Multivariate
* make data frame of the data
* detect outliers for the columns/find the index of outliers
* take the outliers that belong to both the columns as data
* plot data
* color and mark the outliers

* Outliers in both columns-> intersection
* Outliers in either of -> union

* More than 2 variables make a final list of variables produced by majority voting or other weighing procedure.

#### LOF
* is Density-based
* works on numerical data only

* show outliers with diplot
* show outliers with pairs plot

* k = number of neighbors
* compute outlier scores
* select the top ones as outliers
* plot the outliers

### Clustering
* Group data into clusters
* Data not assigned to any cluster are taken as outliers(DBSCAN)
* k-means outliers: data assigned to k groups by assigning them to the closest cluster center
  * calculate distance/dissimilarity between each object and its cluster center.
  * pick those with largest distances

* remove class category
* generate kmeans result
* cluster the centers
* cluster the IDs
* calculate distances between objects and cluster centers
* pick top 5 largest distances
* who are the outliers (print them)

### Time series
* decompose time series data with robust regression
* identify outliers
* google: introduction to STL (Seasonal-trend-decomposition based on Loess)

## Time series Decomposition
Time Series Decomposition is to decompose a time series into trend, seasonal, cyclical and irregular components.
* Trend: long term trend
* Seasonal: seasonal variation
* Cyclical: repeated but non-periodic fluctuations
* Residual: irregular component

### Time Series Forecasting
* Autoregressive moving average ARMA-model
* Autoregressive integrated moving average ARIMA-model

### Time Series Clustering
Times series clustering is to partition time series data into groups based on similarity or distance, so that time series in the same cluster are similar to each other.
Measures:
* Euclidean distance
* Manhattan distance
* Maximum norm
* Hamming distance
* Angle between two vectors (inner product)
* Dynamic Time Warping (DTW) distance#

##### Sources
* RDataming
