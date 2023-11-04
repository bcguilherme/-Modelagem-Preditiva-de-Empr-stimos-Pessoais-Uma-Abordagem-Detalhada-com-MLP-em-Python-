# Redes-Neurais-neural-networks-

# Bank Personal Loan Modeling

This repository contains a Python script for modeling a dataset related to personal loan acceptance using the Pandas library and the MLPClassifier from Scikit-Learn.

## Table of Contents

- [Overview](#overview)
- [Dataset Description](#dataset-description)
- [Data Preprocessing](#data-preprocessing)
- [Modeling](#modeling)

## Overview

This project focuses on building a predictive model to determine whether a customer will accept a personal loan offer. The dataset used for this analysis is "Bank_Personal_Loan_Modelling.xlsx."

## Dataset Description

The dataset consists of various features, including categorical, continuous, and ordinal variables:

### Categorical Variables:
- Personal Loan: Whether the customer accepted the personal loan offer (target variable).
- Securities Account: Whether the customer has a securities account.
- CD Account: Whether the customer has a certificate of deposit (CD) account.
- Online: Whether the customer uses online banking services.
- Credit Card: Whether the customer uses a credit card issued by UniversalBank.

### Continuous Variables:
- Age: Customer's age.
- Experience: Years of experience.
- Income: Annual income in dollars.
- CCAvg: Average credit card spending.
- Mortgage: Mortgage value.

### Ordinal Variables:
- Family: Family size.
- Education: Customer's education level.

The "ID" variable doesn't provide valuable information, and the "Zip code" variable may not be useful for modeling.

## Data Preprocessing

We perform the following data preprocessing steps:

1. Remove the "ID" variable from the dataset.
2. Display basic statistics of the variables using `df.describe().transpose()`.
3. Check the distribution of the target variable using `df["Personal_Loan"].value_counts()`.
4. To address the class imbalance, we create a balanced dataset with a sample of class 0 and all instances of class 1.

## Modeling

1. Split the dataset into predictors (X) and the target variable (Y).
2. Split the data into training and testing sets using `train_test_split`.
3. Normalize the variables using `StandardScaler`.
4. Train a Multi-Layer Perceptron (MLP) classifier with hidden layer sizes of (100, 50, 20) and activation function 'logistic'.
5. Evaluate the model's accuracy on the test set.

The model's accuracy is printed as a percentage. The repository provides a simple example of how to preprocess data and build a predictive model for personal loan acceptance.

Feel free to explore and adapt this code for your specific needs.
