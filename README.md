﻿CS 580L - Machine Learning
Final Project Proposal


A Study On Forecasting Online Shopping Data
By:
Erik Langert, John Montesano, Alexander Marcus


The goal of this project is to study different forecasting techniques to predict online shopping patterns. Our dataset, which is a real world online shopping dataset, contains 100 different products being purchased by 31,490 different customers. The important files in our dataset are as follows:


* A 100 (key products) x 120 (number of days + 1) matrix containing the sale of each product on each day. The first row is the key product ID, whilst the last row is the total sale of the each product for the entire 118-day timespan. This information is located in product_distribution_training_set.txt
* A 1 x 100 (key products) list containing the index numbers for the 100 key products. This information is help in key_production_IDs.txt
* *Note: We are only using a subset of our total data, for the categorization of the data may not be useful for certain predictors. This will allow us to establish a more fair baseline during comparison of algorithms


Our goal is to predict the overall sale of the key products for the next 17 days (up to day 146). We would also like to extend this model to predict the sale of each individual key product for the next 17 days as well.


We will compare and contrast the following techniques: ARIMA, feed-forward neural networks, LSTM recurrent neural networks, and quadratic regression. We intend to leverage open source python libraries such as sci-kit learn, keras, tensorflow, pandas, and numpy, as well as R libraries such as forecast and princomp to implement, training, and evaluate these forecasting techniques. We will modify these algorithms’ parameters and network architecture to minimize our test error and construct a theoretical prediction for the following 17 days as well.




Evaluation:
We will use Root Mean Square Error (RMSE) to evaluate prediction accuracies of our forecasting algorithms.
We will train our models on days 0 - 100 and test on days 101 - 118. We will then take our model, train on all 118 days, and predict the theoretical sales of days 119 - 146.


Research:
- Functional Quadratic Regression (2009) Fang Yao
-An Introductory Study on Time Series Modeling and Forecasting (2001) Ratnadip Adhikari, R. K. Agrawal 
- Deep Learning (2015)  Ian Goodfellow, Yoshua Bengio deeplearningbook.org
- Neural Networks for Time Series Processing (1996) Georg Dorffner
- Recurrent neural networks and robust time series prediction(1994) J.T. Connor


Team Role Breakdown:


Erik Langert – Vanilla & Recurrent Neural Networks
John Montesano - ARIMA, Unit Testing
Alexander Marcus - QDA, Code Format / Cleanliness