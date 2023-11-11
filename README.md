# CUSTOMER CHURN PREDICTION

## Overview
This repository contains code for predicting customer churn using machine learning techniques. The dataset includes various features such as credit score, geography, gender, age, and more. The goal is to build a predictive model to identify customers who are likely to churn.

## Data Exploration and Preprocessing
The initial exploration of the dataset reveals 10,000 rows and 14 columns, including features like credit score, tenure, balance, and the target variable 'Exited' indicating whether a customer churned or not. Key statistics and visualizations are used to understand the data distribution and relationships.

### Exploratory Data Analysis (EDA)
EDA includes a correlation heatmap, count plots for gender and geography, and bar charts showing correlations of numeric features with the 'Exited' column. Noteworthy findings include positive correlation of 'Age' and 'Balance' with customer churn, while 'IsActiveMember' shows a negative correlation.

## Data Preprocessing
Data preprocessing involves handling missing values (none found), dropping irrelevant columns ('Surname', 'CustomerId', 'RowNumber'), and converting numerical features into categorical ranges ('Tenure' and 'Age'). One-hot encoding is applied to categorical variables, and numerical features are scaled.

## Model Training
Three models are trained and evaluated: Random Forest Classifier, XGBoost Classifier, and a Neural Network. The Random Forest and XGBoost models undergo hyperparameter optimization using RandomizedSearchCV.

### Random Forest Classifier
Achieved an accuracy of 85.1% on the validation set. Best hyperparameters: {'n_estimators': 110, 'max_depth': 14}.

### XGBoost Classifier
Achieved an accuracy of 86.0% on the validation set. Best hyperparameters: {'subsample': 1, 'max_depth': 3, 'learning_rate': 0.1}.

### Neural Network
A neural network is implemented with hyperparameters optimized using RandomizedSearchCV. The best configuration includes 16 neurons, 1 hidden layer, SGD optimizer, learning rate of 0.01, 15 epochs, and a batch size of 16. The model achieved an accuracy of 84.5% on the validation set.

## Model Selection
After training and evaluating three models, the Neural Network emerges as the final choice due to its strong performance on relevant metrics. While achieving an overall accuracy of 85.3% on the validation set, the Neural Network excels in recall, particularly for churn instances. The model demonstrates an 87% recall for non-churn cases and a 46% recall for churn cases.

## Model Selection
The Neural Network despite having a slightly lower accuracy compared to the XGBoost model, its superior performance in identifying churn instances makes it the preferred choice.

## Conclusion
The selected Neural Network model showcases a nuanced understanding of customer churn, providing valuable insights and accurate predictions. Further exploration and fine-tuning of hyperparameters could potentially enhance its performance even more.


