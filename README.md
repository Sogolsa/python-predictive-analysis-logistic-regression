# Predictive Analysis — Logistic Regression

This project applies logistic regression to a marketing dataset to predict customer subscription behavior. The analysis was conducted in Python using pandas, scikit‑learn, and visualization libraries, with the workflow documented in a Jupyter Notebook.

## Project Overview

- **Objective**: Predict whether a customer subscribes to a term deposit based on demographic and campaign features.
- **Dataset**: Bank marketing dataset (`bank.csv`) with 4,521 records and 17 features.
- **Approach**:
  - Data cleaning and preprocessing (encoding categorical variables, handling unknowns).
  - Exploratory data analysis (EDA) with summary statistics and visualizations.
  - Feature engineering with dummy variables.
  - Logistic regression modeling with recursive feature elimination (RFE).
  - Model evaluation using accuracy, confusion matrix, and odds ratios.

## Key Insights

- **Class imbalance**: ~88% of customers did not subscribe, ~12% did.
- **Strong predictors**:
  - **Job title** and **education** showed clear influence on subscription likelihood.
  - **Month of contact** (e.g., March, October, December) significantly impacted outcomes.
  - **Previous campaign outcome (poutcome)** was highly predictive.
- **Model performance**:
  - Accuracy: ~89.5% on test data.
  - Confusion matrix showed good classification of non‑subscribers, with some false negatives for subscribers.
- **Odds ratios**:
  - Customers with a successful previous outcome had **4.18× higher odds** of subscribing.
  - Being retired increased odds by ~92%.
  - Certain months (March, October, December) were associated with higher subscription likelihood.
  - Having a loan or being married reduced subscription odds.

## Methodology

1. **Data Exploration**  
   - Summary statistics and distributions.  
   - Visualizations: histograms, bar charts, stacked bars for categorical predictors.

2. **Preprocessing**  
   - Converted categorical variables to dummy variables.  
   - Encoded target variable (`y`) as binary (0 = no, 1 = yes).  

3. **Modeling**  
   - Logistic regression with scikit‑learn.  
   - Recursive Feature Elimination (RFE) to select top 15 predictors.  

4. **Evaluation**  
   - Accuracy score and confusion matrix.  
   - Interpretation of coefficients as log‑odds and odds ratios.  



