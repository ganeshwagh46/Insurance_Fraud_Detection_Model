# Insurance_Fraud_Detection_Model

## Project Overview

This repository contains an end-to-end Insurance Fraud Detection project implemented in a reproducible Jupyter notebook. The pipeline covers data cleaning, exploratory data analysis (EDA), feature engineering, model training, evaluation, and comparison. The primary aim is to identify potentially fraudulent insurance claims so that investigators can prioritize cases effectively.

## Dataset

Source: Kaggle.com

Features: Policyholder demographics, policy details, claim amounts, claim types, dates, and a binary fraud indicator.

Data Quality: The notebook documents data issues and outlines steps taken to handle missing values, inconsistent categories, and outliers.

## Problem Statement

Insurance fraud causes significant financial losses. This project builds a supervised binary classification model to flag suspicious claims for further human review.

## Objectives

Perform thorough EDA to understand data patterns.

Engineer meaningful features that capture claimant behavior.

Train and compare multiple models using cross-validation and resampling/class-weighting strategies.

Select the best model and explain the most influential features.

Provide a reproducible workflow with deployment recommendations.

## 🛠 Methodology
Exploratory Data Analysis (EDA)

Checked for duplicate rows, missing values, and class imbalance.

Visualized distributions of numeric features and frequency counts of categorical fields.

Examined correlations and identified outliers.

Cleaning & Preprocessing

Standardized date formats and handled missing values using median/mode or domain-specific rules.

Winsorized extreme outliers in monetary fields.

Created elapsed-time features (e.g., days_since_policy_start) and aggregated historical claim statistics per policyholder.

Feature Engineering

Encoded categorical variables: one-hot encoding for low-cardinality features and target/ordinal encoding for high-cardinality features.

Scaled numeric features within pipelines where required.

Modeling

Baseline Models: Logistic Regression, Decision Tree.

Ensemble Models: Random Forest, XGBoost, LightGBM.

Addressed class imbalance using class weights and SMOTE.

Hyperparameter tuning with stratified cross-validation (GridSearchCV/RandomizedSearchCV).

Evaluation

Primary Metrics: ROC AUC, F1-score.

Secondary Metrics: Precision, Recall, Confusion Matrix, Precision–Recall Curve.

Explainability: Prioritized Recall as the most meaningful metric in fraud detection; feature importance and SHAP used to interpret key drivers.

## 📑 Key Findings

Random Forest achieved the highest performance compared to Logistic Regression and Decision Tree, making it the most effective model for fraud detection.

Fraudulent claims were highly imbalanced in the dataset, requiring class weighting and SMOTE to improve recall for minority (fraud) cases.

Predictive features such as claim_amount, policy_age, and number_of_past_claims were consistently identified as strong indicators of fraudulent behavior.

Random Forest balanced precision and recall better than other models, detecting more fraud cases without generating excessive false positives.

## ✅ Conclusion

Random Forest emerged as the most reliable model for detecting fraudulent insurance claims. Addressing class imbalance significantly improved its ability to capture rare fraud cases. The project emphasizes the importance of feature engineering and ensemble methods in building robust fraud detection systems.
