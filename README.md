# Credit Card Fraud Analysis

## Overview

This project uses python to analyze a dataset containing transactions made by credit cards in September 2013 by European cardholders.

Due to confidentiality issues,  the original features and more background information about the data have not been provided. Features V1 to V28 are the principal components obtained with PCA, the only features which have not been transformed with PCA are 'Time' and 'Amount'. Feature 'Time' contains the seconds elapsed between each transaction and the first transaction in the dataset. The feature 'Amount' is the transaction amount. Feature 'Class' is the response variable and it takes value 1 in case of fraud and 0 otherwise.


## Tools and Technologies Used

Programming Language: Python

Software: Jupyter Notebook


## Data Source

Download transactions dataset from [here](https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud?resource=download)


## Exploratory Data Analysis (EDA)


### Class Distribution

![image](https://github.com/sumaiyamahmud/credit_card_fraud_analysis/assets/113713705/f476c661-e047-45eb-befa-1e0b2727242b)

The Class dustributions show that only a few transactions are fraudulent.


### Correlation Matrix

![image](https://github.com/sumaiyamahmud/credit_card_fraud_analysis/assets/113713705/645eb005-9b78-4478-bec0-5de395350778)


### Distribution of Time and Amount

![image](https://github.com/sumaiyamahmud/credit_card_fraud_analysis/assets/113713705/c26ba13a-807b-43a5-a62a-2660f2e1e63f)


## Data Pre-processing

The *Time* and *Amount* features were standardized using StandardScaler before using them to predict values. They were then split into features (X) and target (y) variable. Then, the dataset was split into training and testing sets.


## Data Modeling

*LogisticRegression*, *RandomForestClassifier*, *DecisionTreeClassifier* and *Support Vector Machine* were used to model the data. The models were then fit to the training dataset and then used to predict the results for the test set.


## Model Evaluation

The models were evaluated in terms of *accuracy*, *precision*, *recall*, and *f1_score*. 


![image](https://github.com/sumaiyamahmud/credit_card_fraud_analysis/assets/113713705/c5fb0788-2137-4c82-a71e-ec90eb944c20)


RandomForestClassifier performed the best overall compared to the rest of the models.

## Confusion matrix for Random Forest Regression model

![image](https://github.com/sumaiyamahmud/credit_card_fraud_analysis/assets/113713705/2861f6d3-0627-49b6-9101-c3eb097c881d)

The matrix above shows that the model predicted:

True Positive (TP): 98
True Negative (TN): 8.5e+04 (85,000)
False Positive (FP): 5
False Negative (FN): 36

Incorrect predictions are quite low as shown by very low values of false positive and false negative.


## References

https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud?resource=download 

https://www.w3schools.com/ 
