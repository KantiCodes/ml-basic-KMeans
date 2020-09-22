# ml-KMeans-usage

# Pre-face
Hoping that my work might help beginners better understand what machine learning is and what can we do with it I decided to put a small explanantion of ML techniques types before some of my machine learning projects.  
I hope that after reading following definition it will be easier to understand what is it that I'm trying to show and how it's done.

***Machine learning problems can be approached using 3 different methods.***
* Supervised learning - when dealing with labeled data such that having input data ***_X_*** and some output data ***_Y_***, we want to find parameters ***_θ_*** of the function ***_f_*** such that ***_X_ *  _θ_ ≈ _f_***  
***Example:*** could be the famous titanic survival classification or house price prediction, where based on some features such as location of the house and its size we predict the price.  

* Unsupervised learning - when dealing with unlabeled data and looking for similarities/patterns between certain samples, e.g. clusters of the data with similar features.  
***Example:*** could be song recommendation based on liked/favorite songs. The system could find other users that share with you favorite list(people from same cluster) and recommend you some of their songs

* Reinforcement learning - when dealing with rewards systems such as video games, traffic problems, trying to teach the agent (entity beeing able to modify the enviroment) how to take actions in order to maximize the reward.

**PS:**
_Feel free to merge request better definition_.

# Introduction
This repository presents step by step usage of [KMeans](https://scikit-learn.org/stable/modules/generated/sklearn.cluster.KMeans.html#sklearn.cluster.KMeans) algorithm from [sklearn](https://scikit-learn.org/stable/) library. I am going to first show how to cluster the data assuming the number of cluster on a guess and then present [***Elbow Technique***](https://en.wikipedia.org/wiki/Elbow_method_(clustering)#:~:text=In%20cluster%20analysis%2C%20the%20elbow,number%20of%20clusters%20to%20use) used to determine right number of clusters.

# KMeans intuition / naive KMeans
Is an unsupervised clustering method that clusters the data based on the smiliarity between the samples. 
It requires from the user to provide it with number of clusters - ***K*** and then finds ***K*** centroids such that the centroid of specific cluster is the closest representation of all of the samples belonging to that cluster.  
The most common similarity metric is squared eucledian distance.

The iterative naive KMeans (slow version but, giving good intuition beheind the algorithm):  
***Step one*** for all of the _samples_ assign them to the cluster which squared eucledian distance is the lowest  
***Step two*** for all clusters, assign it to mean of samples belonging to that cluster  

<img src="https://upload.wikimedia.org/wikipedia/commons/e/ea/K-means_convergence.gif" width="400" height="400"/>

[source](https://commons.wikimedia.org/wiki/File:K-means_convergence.gif)
