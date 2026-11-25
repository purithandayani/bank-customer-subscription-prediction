# Predicting Customer Term Deposit Subscription Using Classification Models
## Project Overview
This project aims to develop and compare machine learning classification models to predict the likelihood of a bank customer subscribing to a term deposit and figure out the best performing-model. The output of the models will be a subscription probability score for each customer in the test dataset, along with a binary prediction (Yes/No).

##**Business Objective**
A Portuguese banking institution launched a direct marketing campaign to promote its term deposit product. The marketing team aims to identify customers who are most likely to subscribe to the product, so the team can prioritize potential customers, optimize campaign targeting, and improve marketing strategy. To address this objective, this project will develop and compare machine learning classification models to predict the likelihood of a customer subscribing to a term deposit and figure out the best performing-model. The output of the models will be a subscription probability score, and a binary prediction (Yes/No) on each customer in the test dataset.

## **Data Understanding**
The data is related with direct marketing campaigns of a Portuguese banking institution. The marketing campaigns were based on phone calls. Often, more than one contact to the same client was required, in order to access if the product (bank term deposit) would be `yes` or `no` subscribed. The dataset consists of 41188 observations and 20 inputs, ordered by date from May 2008 to November 2010.
**Target Variable:**
1 – Customer subscribed to a term deposit.
0 – Customer did not subscribe.
**Class Distribution:**
No subscription: 88.73%
Yes subscription: 11.27%

**Methodology**
1. Data Understanding & Exploratory Data Analysis
- Dataset overview and descriptive statistics.
- Target class distribution analysis.
- Categorical and numerical feature exploration.
- Correlation analysis.
- Feature–target relationship analysis.

2. Data Preprocessing
- Duplicate record removal.
- Exclusion of duration to prevent data leakage, since call duration is only known after a customer interaction.
- One-Hot Encoding for categorical features.
- Min-Max Scaling for numerical features in Logistic Regression.
- Stratified train/validation/test splitting.

3. Model Development
- **Logistic Regression** as the baseline model.
- **Random Forest with class weight balanced** for class imbalance.
- **Random Forest with random oversampling** to increase proportion of the minority class in the training data.
These models will be trained and evaluated to compare their performance in predicting whether a customer will subscribe to a term deposit.

4. Model Evaluation
Model performance is evaluated using:
- Precision
- Recall
- F1-score
- ROC-AUC
- Confusion Matrix
A classification threshold of 0.5 is applied to generate binary predictions.

## **Model Results**
Based on validation performance, the selected model is Random Forest with RandomOverSampler
The model achieved the highest recall (38.3%) and F1-score (42.2%) among the evaluated models, making it the most promising approach for identifying potential subscribers.

Confusion Matrix Interpretation
- True Positive: 356
- False Positive: 376
- False Negative: 572
- True Negative: 6,932
The model successfully identifies 356 actual subscribers, while 572 potential subscribers remain unidentified.

## **Prediction Output**
The selected model generates two main outputs for each customer:
1. subscription_probability: Estimated probability of subscribing to a term deposit.
2. predicted_subscription: Binary prediction (Yes/No) using a 0.5 threshold.
These outputs can help the bank prioritize potential subscribers for targeted marketing campaigns.

## **Business Recommendations**
- Prioritize potential subscribers: Use predicted subscription probabilities to identify and prioritize customers for marketing outreach.
- Improve campaign targeting: Focus marketing efforts on customer segments with higher observed subscription rates.
- Reduce missed opportunities: Further improve model recall to identify more potential subscribers.
- Monitor model performance: Evaluate prediction performance regularly and refine the model as new campaign data becomes available.
