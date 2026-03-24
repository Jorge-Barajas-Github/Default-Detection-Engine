# \# Default Detection Engine

# 

# This project develops and evaluates supervised machine learning models to predict whether a credit card client will default on their next payment. The objective is to build classification models that can effectively identify high-risk clients and evaluate performance using appropriate metrics for imbalanced data.

# 

# \---

# 

# \## Problem Overview

# 

# Credit default prediction is a critical task in financial risk management. Financial institutions rely on accurate models to identify clients who are likely to default in order to mitigate losses and improve decision-making.

# 

# This project applies supervised learning techniques to predict default behavior using historical credit and payment data, with a focus on handling class imbalance and evaluating model performance beyond simple accuracy.

# 

# \---

# 

# \## Dataset

# 

# \- Source: Kaggle (UCI Default of Credit Card Clients Dataset)

# \- Records: 30,000 clients

# \- Features: 24 explanatory variables

# \- Target: `default.payment.next.month` (Binary)

# 

# The dataset contains demographic information, credit limits, repayment history, and billing/payment amounts.

# 

# Note: The dataset is not included in this repository due to file size.

# 

# \---

# 

# \## Approach

# 

# The full workflow is implemented in a single notebook and includes:

# 

# \### 1. Data Preparation

# 

# \- Data cleaning (handling invalid category values)

# \- Feature selection and transformation

# \- Train / validation / test split using stratification

# \- Feature scaling using StandardScaler

# \- One-hot encoding for categorical variables

# 

# \### 2. Exploratory Data Analysis

# 

# \- Summary statistics and distribution analysis

# \- Correlation heatmap to identify relationships with default behavior

# \- Pairwise feature visualization

# 

# \### 3. Model Development

# 

# Three supervised learning models were trained and tuned:

# 

# \- Logistic Regression (baseline with class weighting)

# \- Decision Tree (depth and leaf tuning)

# \- Random Forest (ensemble model with hyperparameter tuning)

# 

# GridSearchCV was used to identify optimal hyperparameters for each model.

# 

# \### 4. Evaluation

# 

# Models were evaluated using:

# 

# \- F1-score (primary metric for class imbalance)

# \- ROC-AUC score

# \- Confusion matrix

# \- Classification report

# 

# \---

# 

# \## Results

# 

# The Random Forest model achieved the best performance:

# 

# \- \*\*F1 Score:\*\* 0.53  

# \- \*\*ROC-AUC:\*\* 0.767  

# 

# Comparison:

# 

# \- Logistic Regression: F1 = 0.467, AUC = 0.705  

# \- Decision Tree: F1 = 0.502, AUC = 0.738  

# 

# \### Key Observations

# 

# \- Random Forest provided the best balance between precision and recall

# \- Logistic Regression was more interpretable but underperformed in detecting defaulters

# \- Repayment history features (PAY\_0, PAY\_2, PAY\_3) were the most important predictors

# \- Demographic variables had significantly lower predictive power

# 

# \---

# 

# \## Repository Structure

# 

# ```text

# Default-Detection-Engine/

# │

# ├── data/

# │   └── README.md

# ├── notebooks/

# │   └── Default\_Detection\_Engine.ipynb

# ├── src/

# │   └── utils.py

# ├── requirements.txt

# └── .gitignore

