# Airline Flight Fare Prediction

Implementing an END-to-END regression problem and trying our different approaches to reduce prediction error.


## Table of Contents

* [Motivation](#motivation)
* [About the Data](#about-the-data)
* [Challenges](#challenges)
* [Results](#results)
* [Required Packages](#required-packages)
* [Acknowledgements](#acknowledgements)
* [Future Scope](#future-scope)


## Motivation

Flight ticket prices can be something tricky to guess, today we might see a price, check out the price of the same flight tommorow and it's a different story.
trying to build a model to accurately predict these prices would be really satisfying.

## About the Data:

The dataset can be downloaded from here : https://www.kaggle.com/datasets/nikhilmittal/flight-fare-prediction-mh

Our Features: 

* Airline : The name of the airline
* Date_of_Journey: the date of flight
* Source : The city where the flight took from
* Destination: The city where the plane landed
* Dep_Time: The time when the plane takes off from Source
* Arrival_Time: The time when the plane lands at destination
* Duration : The total time in hours and minutes to go from Source to Destination
* Total_Stops: The number of cities the plane stopped at between Source and Destination
* Additional_Info: Additional_Information about the flight(contains meal or not, baggage check-in or not, etc.)


## Challenges

* Data Cleaning
* Data Preprocessing
* Outliers Detection
* Feature Engineering
* Tuning our model

## Results

* Started with baseline model (linear regression) with R2 score of 0.95 on training set and 0.79 on testing set.
* trained a baseline randomforest model and got a better R2 score of 0.812
* removed some outlier record and imputed other and it enhanced our R2 score to 0.835
* Did hyperparameters tuning on randomforest model and got an R2 score of 0.842
* then decided to try a more powerful regressor like gradientboosting and got an R2 score of 0.852 with hyperparameter tuning
* Final result is that we build a model with RMSE of 1847.3 INR and Normalized RMSE = 0.052.
This means that on average, the standard deviation from ground truth price values is 1847 INR which is not bad at all.

## Required Packages

* Python3
* Numpy
* Pandas
* Matplotlib
* Seaborn
* Sklearn


## Acknowledgements

This project is my implementation of  a KAGGLE competition. 

## Future Scope

* Do further feature engineering
* Enhancing our R2 score to 0.9 or above and reduce RMSE to about 500 INR.
* Model Deployment
