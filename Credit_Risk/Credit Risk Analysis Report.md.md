# Credit Risk Analysis Report

## Overview of the Analysis

### Introduction

Lending companies extend loans or credit to borrowers with the expectation of either asset return or repayment. Credit risk arises when a borrower fails to fulfill this obligation, potentially leading to financial losses for the lender. In this analysis, we employ machine learning to assess the creditworthiness of borrowers by analyzing historical lending data from a peer-to-peer lending service.

### Methodology

We utilize a logistic regression algorithm, widely recognized for predicting the probability of a target variable in classification tasks, to identify healthy (low-risk) and non-healthy (high-risk) loans based on provided loan status.

### Model Development

After analyzing the dataset provided by the lending company, a logistic regression model was trained, achieving an impressive accuracy score of 95%. However, it's worth noting that the model demonstrated a higher recall value (0.99) for healthy loans compared to non-healthy loans (0.91), indicating a slight imbalance in the dataset.

### Data Imbalance

Upon examining the loan status distribution, it's evident that the dataset exhibits significant class imbalance:

- Healthy Loans (Class 0): 75,036 instances
- Non-Healthy Loans (Class 1): 2,500 instances

### Model Performance - Imbalanced Data

- True Positives (Healthy Loans): 18,663
- False Positives (Healthy Loans predicted as Non-Healthy): 102
- True Negatives (Non-Healthy Loans): 563
- False Negatives (Non-Healthy Loans predicted as Healthy): 56

### Oversampling for Balance

To rectify this imbalance, we employed the RandomOverSampler module from the imbalanced-learn library. This approach effectively augmented the minority class, resulting in a balanced dataset with 56,271 instances for each class.

### Model Performance - Balanced Data

- True Positives (Healthy Loans): 18,649
- False Positives (Healthy Loans predicted as Non-Healthy): 116
- True Negatives (Non-Healthy Loans): 615
- False Negatives (Non-Healthy Loans predicted as Healthy): 4

## Results

### Machine Learning Model 1 (Logistic Regression Model Fitted with Imbalanced Data)

The model accurately predicted healthy loans 100% of the time. However, it predicted non-healthy loans with 85% accuracy.

While the model performed well, there are potential areas for improvement:

- 1% of healthy loans were misclassified as non-healthy (high-risk).
- 9% of non-healthy loans were misclassified as healthy (low-risk).

This indicates a higher likelihood of misclassifying non-healthy loans, which could lead to potential financial losses for the lending company. The model demonstrated a 1% error rate for healthy loans and a 9% error rate for non-healthy loans based on recall scores.

![Model 1](https://github.com/GabrelleaNorman/credit-risk-classification/assets/130908954/860fc070-22db-4568-b679-88320244d92f)

### Machine Learning Model 2 (Logistic Regression Model Fitted with Oversampled Data)

The model accurately predicted healthy loans 100% of the time. It predicted non-healthy loans with 84% accuracy.

With the balanced (oversampled) data, the model exhibits a significantly reduced likelihood of making critical misclassifications:

- Only 1% of healthy loans are misclassified as non-healthy (high-risk).
- Likewise, only 1% of non-healthy loans are misclassified as healthy (low-risk).

These results demonstrate a marked improvement in the model's ability to accurately classify loans, particularly non-healthy ones, significantly reducing the risk of potential financial losses for the lending company.

![Model 2](https://github.com/GabrelleaNorman/credit-risk-classification/assets/130908954/efc5b74e-3bc7-4ba0-a34f-32bb5e8c0111)

### Summary

The logistic regression model fitted with the balanced (oversampled) dataset exhibited outstanding performance, achieving an accuracy score of 99%. This model is especially proficient at correctly classifying non-healthy loans, which is crucial for minimizing potential financial losses.

In conclusion, a lending company should prioritize a model that accurately identifies healthy and non-healthy loans. The logistic regression model fitted with the balanced dataset is recommended due to its superior accuracy, balanced classification performance, and reduced risk of misclassifying non-healthy loans.

