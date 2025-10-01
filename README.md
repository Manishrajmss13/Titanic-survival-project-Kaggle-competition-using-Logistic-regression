# Titanic Survival Prediction (Kaggle Competition)

This repository contains my submission for the legendary Kaggle "Titanic: Machine Learning from Disaster" competition. The goal of this project was to build a predictive model to determine whether a passenger would have survived the sinking of the RMS Titanic.

This notebook represents a complete data science workflow, starting from initial data exploration and cleaning, moving through feature engineering, and finally to model training and prediction.

# Choosen Approach:
My strategy for this challenge was to use a Logistic Regression model, focusing heavily on thoughtful data preparation to ensure the model had the best possible information to learn from.

## 1. Data Exploration & Cleaning

The first step was a deep dive into the train.csv dataset. I used visualizations to understand the characteristics of the passengers and how certain attributes like Class, Sex, and Port of Embarkation correlated with survival.

This initial analysis revealed a few key challenges:

* Missing Data: The Age and Cabin columns had a significant number of null values.

* Irrelevant Features: Columns like Name and Ticket number, in their raw form, didn't seem immediately useful for prediction.

To address this, I imputed the missing Age values using the median for that column and dropped the Cabin column due to the high volume of missing data.

## 2. Feature Engineering
With a clean dataset, I engineered the features to be suitable for a machine learning model:

* Categorical Encoding: I converted key categorical features like Sex and Embarked into a numerical format using one-hot encoding.

* Feature Dropping: To simplify the model and avoid noise, I removed the Name, Ticket, and Cabin columns.

## 3. Model Training & Prediction
* Algorithm: I chose Logistic Regression for its strong baseline performance and high degree of interpretability.

* Training: The model was trained on the cleaned and engineered feature set derived from the train.csv file.

* Prediction: The trained model was then used to predict the survival outcomes for the 418 passengers in the test.csv dataset, generating the final My prediction.csv submission file.
