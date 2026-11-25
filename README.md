# Predicting Customer Term Deposit Subscription Using Classification Models
## Project Overview
This project aims to develop and compare machine learning classification models to predict the likelihood of a bank customer subscribing to a term deposit and figure out the best performing-model. The output of the models will be a subscription probability score for each customer in the test dataset, along with a binary prediction (Yes/No).

## 1. Business Objective
A Portuguese banking institution launched a direct marketing campaign to promote its term deposit product. The marketing team aims to identify customers who are most likely to subscribe to the product, so the team can prioritize potential customers, optimize campaign targeting, and improve marketing strategy. To address this objective, this project will develop and compare machine learning classification models to predict the likelihood of a customer subscribing to a term deposit and figure out the best performing-model. The output of the models will be a subscription probability score, and a binary prediction (Yes/No) on each customer in the test dataset.

## **2. Data Understanding**
The data is related with direct marketing campaigns of a Portuguese banking institution. The marketing campaigns were based on phone calls. Often, more than one contact to the same client was required, in order to access if the product (bank term deposit) would be `yes` or `no` subscribed. The dataset consists of 41188 observations and 20 inputs, ordered by date from May 2008 to November 2010.

## **3. Data Loading & Wrangling**
Before loading and processing the dataset, first import all the libraries needed for data manipulation, preprocessing, visualization, and machine learning model development. This project will compare three classification models:
- **Logistic Regression** as the baseline model.
- **Random Forest with class weight balanced** for class imbalance.
- **Random Forest with random oversampling** to increase proportion of the minority class in the training data.



These models will be trained and evaluated to compare their performance in predicting whet
her a customer will subscribe to a term deposit.
