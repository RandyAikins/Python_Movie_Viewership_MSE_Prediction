# SERVICE VIEWERSHIP PREDICTION AND MAJOR SPORTS EVENT DAY CLASSIFICATION

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

![](https://github.com/RandyAikins/Captsone-Project/assets/128720674/d233c4df-dd3f-4469-b8f6-b922a994880c)

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


# 1.3 Data Assessment
The dataset is assessed for shape, information, statistical description of features, duplicated and null values

![](https://github.com/RandyAikins/Python_Movie_Viewership_MSE_Prediction/assets/128720674/48671f60-6466-46a5-b953-af0395955be8)


# 2.0 Exploratory Data Analysis (EDA)
Univariate, Bivariate, and Multivariate Analysis is performed to uncover patterns and identify relationships among features

![](https://github.com/RandyAikins/Python_Movie_Viewership_MSE_Prediction/assets/128720674/012c4b7a-11d3-4585-bd7c-f6436c80232c)
![](https://github.com/RandyAikins/Python_Movie_Viewership_MSE_Prediction/assets/128720674/9dc3b9ad-3a6a-4604-a92f-880494e0a24c)
![](https://github.com/RandyAikins/Python_Movie_Viewership_MSE_Prediction/assets/128720674/33b19092-d182-4c17-a61d-cf6d54ebc163)


# 3.0 Regression Task
The task is to build a machine-learning model to predict the amount of viewership for Solace Stream services 

## 3.1 Data Pre-processing
The data pre-processing involved:
- dropping some features
- encoding categorical labels into numerical labels using Label Encoder from Scikit-learn
- segmenting the dataset into predictor variables (x) and target variables (y)
- scaling x variables using Standard Scaler
- splitting the data into training and testing sets

![](https://github.com/RandyAikins/Python_Movie_Viewership_MSE_Prediction/assets/128720674/83cda192-6b33-44a7-8c08-31afa65ccc01)

## 3.2 Model Building
The regression model for predicting content viewership is built using 3 machine-learning algorithms:
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


# 4.0 Classification Task
The task is to classify data points into major sport event and non-major sports event 

## 4.1 Data Preprocessing
- segmenting the dataset into predictor variables (x) and target variables (y)
- scaling x variables using Standard Scaler
- splitting the data into training and testing sets

![](https://github.com/RandyAikins/Python_Movie_Viewership_MSE_Prediction/assets/128720674/7b523709-d25c-4d2d-91a7-edc98bdcb2c5)

## 4.2 Model Building
The classification model for classifying data points into major sports event and non-major sports event is built using 3 machine-learning algorithms:
- Gaussian Naive Bayes
- Decision Tree Classifier

This is done by:
* instantiating the algorithm 
* Training the algorithm using the training sets
* Predicting major sport event using the testing set

![](https://github.com/RandyAikins/Python_Movie_Viewership_MSE_Prediction/assets/128720674/3e403bd8-f2ac-4474-9e1c-dd6d0405a634)

## 4.3 Model Evaluation
The 2 classification models built are evaluated using:
- accuracy score
- precision score
- recall score
- f1 score
- confusion matrix

Using these metrics to measure the performance of the models, Gaussian Naive Bayes suits the better as it has a higher accuracy score

![](https://github.com/RandyAikins/Python_Movie_Viewership_MSE_Prediction/assets/128720674/e4e2d96d-ea9c-4fc8-8fea-26bb9b076e6e)
![](https://github.com/RandyAikins/Python_Movie_Viewership_MSE_Prediction/assets/128720674/c2c522e8-b3c1-4cc2-975f-3396c63891d5)


# Insights:
- There is low viewership for most trailers which has a positive relationship with content viewership.
- 40% of content release day coincide with major sport event which negatively affects content viewership.
- Sci-Fi, Comedy, and Thriller are preferred genres with Drama and Horror the least preferred genres.
- Most of the movies released belong to the Others genre (25.5%) which has low viewership.
- Movies released on Wednesdays have the most viewership with Monday and Thursday-released movies bringing the least content views.

# Recommendations:
- Solace Stream should use the classification models to guide movie release days to reduce coincidence with major sports event which negatively affect content viewership.
- Use regression model to optimize features in boosting future content viewership. For example, trailer views that have a positive relationship with content viewership should be boosted. 
