# Movie Viewership Forecast and Major Sports Event Prediction

## Introduction
Solace Stream is a leading streaming media company that offers a vast library of movies, TV shows, documentaries, and original content catering to a global audience. 
Solace Stream is having a decline in viewership of their content on the first day of release and aims to develop a predictive model that can accurately forecast 
viewership levels and also determine the presence of major sports events that may impact viewership.

## Objective
- Identify key variables that drive viewership
- Implementation of regression module to forecast movie viewership
- Implementation of a classification model to predict major sports events on movie release day

## Task
- Use Python to explore datasets, create a regression model to forecast content viewership, and predict the occurrence of major sports event on release day
- Generate insights from the analysis
- Make recommendations based on the analysis

## 1.1 Import of Python Libraries
![Library](https://github.com/RandyAikins/Python_Movie_Viewership_MSE_Prediction/assets/128720674/2c922e22-0ad9-4fdd-a4d5-d1d5d22e0331)


## 1.2 Data Description and Import
- visitors: Average number of visitors, in millions, to the platform in the past week
- ad_impressions: Number of ad impressions, in millions, across all ad campaigns for the content (running and completed)
- major_sports_event: Any major sports event on the day
- genre: Genre of the content
- dayofweek: Day of the release of the content
- season: Season of the release of the content
- views_trailer: Number of views, in millions, of the content trailer
- views_content: Number of first-day views, in millions, of the content

![](https://github.com/RandyAikins/Python_Movie_Viewership_MSE_Prediction/assets/128720674/7e4948f6-4251-4312-a7b7-ce6846b55306)

## 1.3 Data Assessment
The dataset is assessed for shape, information, statistical description of features, duplicated and null values

![](https://github.com/RandyAikins/Python_Movie_Viewership_MSE_Prediction/assets/128720674/48671f60-6466-46a5-b953-af0395955be8)

## 2.0 Exploratory Data Analysis (EDA)
Univariate, Bivariate, and Multivariate Analysis is performed to uncover patterns and identify relationships among features

![](https://github.com/RandyAikins/Python_Movie_Viewership_MSE_Prediction/assets/128720674/012c4b7a-11d3-4585-bd7c-f6436c80232c)

![](https://github.com/RandyAikins/Python_Movie_Viewership_MSE_Prediction/assets/128720674/9dc3b9ad-3a6a-4604-a92f-880494e0a24c)

![](https://github.com/RandyAikins/Python_Movie_Viewership_MSE_Prediction/assets/128720674/33b19092-d182-4c17-a61d-cf6d54ebc163)

## 3.0 Regression Task

## 3.1 Data Pre-processing
The pre-processing involved:
- dropping some features
- encoding categorical labels into numerical labels using Label Encoder from Scikit-learn
- segmenting the dataset into predictor variables (x) and target variables (y)
- scaling x variables using Standard Scaler
- splitting the data into training and testing sets

![](https://github.com/RandyAikins/Python_Movie_Viewership_MSE_Prediction/assets/128720674/83cda192-6b33-44a7-8c08-31afa65ccc01)

## 3.2 Model Building
The regression model for forecasting content viewership is built using 3 machine-learning algorithms:
- Linear Regression
- Randon Forest Regressor
- XGBoost Regressor

This is done by:
* instantiating the algorithm 
* Training the algorithm using the training sets
* Viewership prediction using the testing set

![](https://github.com/RandyAikins/Python_Movie_Viewership_MSE_Prediction/assets/128720674/59703684-6815-4887-ac0b-87c699bc98d3)

## 3.3 Model Evaluation
The 3 regression models built are evaluated using:
- r-squared (r2)
- mean squared error (MSE)
- mean absolute error (MAE)

Using these metrics to measure the performance of the models, Linear Regression was the best on all 3 evaluation metrics

![](https://github.com/RandyAikins/Python_Movie_Viewership_MSE_Prediction/assets/128720674/6233edb4-a9b2-4212-bd73-87b94308f612)




