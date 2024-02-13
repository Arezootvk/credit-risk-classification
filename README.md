# credit-risk-classification


Welcome to the credit risk classification project! This repository is dedicated to predicting the creditworthiness of borrowers for a peer-to-peer lending services company. Our goal is to develop models that effectively identify whether a loan is at high risk of default or is healthy. This analysis is crucial for financial institutions to minimize losses due to bad loans and assess the risk associated with lending activities.

## Overview of the Analysis

### Dataset and Features
We utilized a dataset containing financial attributes of borrowers and their loans, including credit history, loan amounts, interest rates, income levels, and more. The primary focus was on the `loan_status` column, categorizing loans into healthy (0) or high default risk (1).

### Machine Learning Process
1. **Data Preparation:** Loaded and organized lending data, separating the target outcome and other data.
2. **Data Splitting:** Divided the data into training and testing groups to evaluate the model on new data.
3. **Model Training:** Employed logistic regression, a powerful model for yes/no predictions, trained with the provided data.
4. **Prediction and Evaluation:** Assessed model performance using various metrics, including precision, recall, F1-scores, and a confusion matrix.

## Results

### Model 1
The logistic regression model showcased remarkable performance:

- **Healthy Loans (0):**
  - Precision: 1.00 - Extremely accurate with minimal false positives.
  - Recall: 0.99 - Successfully identified 99% of healthy loans.
- **High-Risk Loans (1):**
  - Precision: 0.85 - Correct 85% of the time when predicting high-risk loans.
  - Recall: 0.91 - Identified 91% of actual high-risk loans.
- **Balanced Accuracy Score:** 0.952 - Strong performance across both classes despite significant class imbalance.
- **F1-Scores:** 1.00 for healthy loans and 0.88 for high-risk loans.
- **Overall Accuracy:** 0.99 - 99% of all model predictions are correct.

### Model 2
The oversampling model demonstrated high effectiveness, especially in identifying high-risk loans:

- **Balanced Accuracy Score:** 0.9937 - Excellent overall performance.
- **Confusion Matrix:**
  - Healthy Loans (0): 18649 correctly identified, 116 misclassified as high risk.
  - High-Risk Loans (1): 615 correctly identified, 4 misclassified as healthy.
- **Precision:** Class 0 (healthy loans) nearly perfect, Class 1 (high-risk loans) at 0.84.
- **Recall:** Class 0 nearly perfect, Class 1 at 0.99.
- **F1-Scores:** Perfect score of 1.00 for healthy loans and 0.91 for high-risk loans.
- **Overall Accuracy:** 0.99 - Highly effective in identifying both healthy and high-risk loans.

## Summary

Both models performed exceptionally well in predicting loan risks, each with its strengths:

- **Model 1:** Highly accurate in identifying both safe and risky loans, achieving almost perfect scores and 99% overall accuracy.
- **Model 2:** Slightly better at dealing with the challenge of imbalanced classes, especially effective at identifying risky loans with a 99% accuracy.

## Recommendation

Choose **Model 2** if pinpointing risky loans is the top priority. It excels at catching these without missing many, making it more suitable for reducing bad loans and managing risk effectively.
