# Module 12 Report Template

## Code is located in Credit_Risk folder(notebook name:credit_risk_classification.ipynb)

## Overview of the Analysis

##

The purpose of this analysis is to develop a machine learning model to assess the credit risk of borrowers based on historical lending data. By training a logistic regression model , our goal is to predict whether a loan will be high-risk (1) or healthy (0).

- **Financial Information:** The dataset consists of past lending activities from a peer-to-peer lending company.
- **Target Variable:** `loan_status`
  - `0` = Healthy loan (low risk of default)
  - `1` = High-risk loan (high probability of default)
- **Features Used for Prediction:**
  - Income
  - Debt-to-income ratio
  - Credit score
  - Loan amount
  - Interest rates, etc.

#### Machine Learning Process:
- **Data Preprocessing:** The dataset was uploaded into a pandas dataframe, the features were separated from the target variable.
- **Data Splitting:** The dataset was split into **training** and **testing** sets.
- **Model Training:** A **Logistic Regression model** was trained using the training data (`X_train` and `y_train`).
- **Model Evaluation:** The model’s performance was evaluated using a **confusion matrix** and **classification report**.

## Results


### **Results:**
- **Accuracy:** **99%**
- **Performance on Healthy Loans (0):**
  - **Precision:** **1.00**
  - **Recall:** **0.99**
  - **F1-score:** **1.00**
  - **Support:** **18,765 loans**
- **Performance on High-Risk Loans (1):**
  - **Precision:** **0.85**
  - **Recall:** **0.95**
  - **F1-score:** **0.89**
  - **Support:** **619 loans**

  ### **Key Takeaways:**
-  **The model accurately predicts most healthy loans (0)** with **perfect precision (1.00)** and **high recall (0.99)**.
-  **It correctly identifies high-risk loans (1) 95% of the time**.
-  **Some healthy loans are misclassified as high-risk** (precision for high-risk = 0.85), which could lead to healthy loans  being misclassified as high risk.

## Summary

The logistic regression model performs well by achieving **99% accuracy**. It successfully predicted **most healthy loans (0)** and detected **high-risk loans (1) with 95% recall**. However, it **misclassified some healthy loans as risky**, which could lead to unnecessary loan rejections.

- **The model performs best at predicting healthy loans (0)** with **perfect precision (1.00)** and **high recall (0.99)**.
- **It effectively detects high-risk loans (1)**, capturing **95% of actual high-risk loans**.
- **It misclassifies some healthy loans as high-risk** (precision for high-risk = 0.85), which could impact lending decisions.

- **If the goal is to avoid high-risk loans**, this model is a **strong choice** due to its **high recall (95%) for high-risk loans**.
- **If reducing false positives  is important**, further **model tuning or alternative models like Random Forest should be explored**.

The model is **recommended for identifying risky loans** since it **correctly detects most high-risk loans**. However, if minimizing **false positives** is a priority, other models need to be considered.
