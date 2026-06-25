📊 Telco Customer Churn Prediction and Customer Segmentation
Project Overview

Customer churn is one of the biggest challenges in the telecom industry. Losing existing customers directly impacts revenue and business growth.

The goal of this project is to:

Analyze customer behavior and identify factors affecting churn
Build a machine learning model to predict customer churn
Improve model performance using multiple approaches
Help businesses take proactive retention actions

In addition, customer segmentation is performed using clustering techniques to group customers based on behavior, spending patterns, tenure, and churn probability. These segments help in designing targeted marketing and retention strategies.

Dataset Description

The dataset used in this project is the IBM Telco Customer Churn dataset, which contains customer demographics, subscription details, billing information, service usage, and churn status.

Key Features:
Tenure Months
Monthly Charges
Total Charges
Contract Type
Internet Service
Payment Method
Technical Support
Customer Lifetime Value (CLTV)
Churn Label (Target Variable)
Project Objectives
Perform exploratory data analysis (EDA)
Identify key factors affecting customer churn
Build a machine learning model for prediction
Improve model using different techniques
Compare multiple modeling approaches
Perform customer segmentation using clustering
Generate business insights for decision-making
Tools & Libraries Used
Python
Pandas
NumPy
Matplotlib
Seaborn
Scikit-learn
OpenPyXL
Exploratory Data Analysis (EDA)
Steps performed:
Studied numerical features (Tenure, Monthly Charges, Total Charges)
Analyzed categorical features (Contract Type, Internet Service, Payment Method, Technical Support)
Compared churned vs non-churned customers using visualizations
Used histograms, boxplots, and countplots
Key Insights:
Customers with low tenure are more likely to churn
Month-to-month contracts show highest churn rate
Higher monthly charges increase churn risk
Customers with technical support are more stable
Data Preprocessing
Converted Total Charges into numeric format
Handled missing values
Removed irrelevant / leakage columns
Applied One-Hot Encoding
Split dataset into training and testing sets
Churn Prediction Model
Model Used:

Random Forest Classifier

Techniques Applied:
Class imbalance handling (class_weight='balanced')
Hyperparameter tuning (n_estimators=300, max_depth=10)
Feature importance analysis
Cross-validation
Model Comparison (All Approaches)
Approach	Description	Accuracy	Precision (Class 1)	Recall (Class 1)	F1-score
Base Model	Default Random Forest	0.79	0.66	0.51	0.58
Approach 1	Class imbalance handling	0.79	0.67	0.52	0.59
Approach 2	Hyperparameter tuning	0.78	0.59	0.75	0.66
Approach 3	Feature importance analysis	0.78	0.60	0.74	0.66
Final Model	RF (n_estimators=300, max_depth=10)	0.78	0.60	0.74	0.66
📈 Cross Validation Results
Accuracy Mean: 0.779
Recall Mean: 0.733

This confirms that the model is stable and generalizes well.

📉 ROC-AUC Analysis
ROC-AUC curve used to evaluate classification performance
Measures ability of model to distinguish:
Class 0 → Non-Churn
Class 1 → Churn

Higher AUC = better model performance
Final model shows strong separation ability across thresholds

Evaluation Metrics Explanation
Class Definition:
Class 0 → Non-Churn Customers (Stay)
Class 1 → Churn Customers (Leave)
Metric Meaning:
Precision (Class 1): Out of predicted churn customers, how many actually churned
Recall (Class 1): Out of actual churn customers, how many were correctly identified

In this project, Recall for Class 1 is more important because missing a churn customer leads to business loss.

Feature Importance

Most important factors affecting churn:

Tenure Months 
Monthly Charges
Contract Type
Total Charges
Internet Service

Insight:
Customers with low tenure + high monthly charges are most likely to churn.

Customer Segmentation

After predicting churn probability, K-Means clustering was applied.

Steps:
Feature selection: Tenure, Monthly Charges, Total Charges, Churn Probability
StandardScaler normalization
Elbow method for optimal clusters
K-Means clustering
Customer Segments
🟢 Budget Loyal Customers
Low monthly charges
Low churn probability
Stable long-term customers
🔴 High Risk New Customers
Low tenure
High churn probability
Need immediate retention actions
🟡 Loyal Premium Customers
High value customers
Low churn probability
Long-term profitable users
Key Business Insights
Month-to-month contracts have highest churn
High charges increase churn risk
Technical support improves retention
Long-tenure customers are more stable
Segmentation helps targeted marketing
Future Improvements
Use advanced models like XGBoost / LightGBM
Deploy using Streamlit web app
Build interactive dashboard
Add real-time churn prediction system

This project demonstrates an end-to-end machine learning pipeline including data analysis, multiple modeling approaches, model evaluation, cross-validation, ROC-AUC analysis, and customer segmentation for real-world business decision-making.