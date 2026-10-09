# Telco Customer Churn Prediction & Retention Analytics

## Live Tableau Dashboard

[View the Telco Customer Churn & Retention Dashboard on Tableau Public](https://public.tableau.com/app/profile/harika.s3102/viz/TelcoCustomerChurnRetentionDashboard/Dashboard1?publish=yes)

## Project Overview
This project builds an end-to-end customer churn analytics solution using Python, PostgreSQL, machine learning, and Tableau.

The goal is to identify customers at risk of leaving, understand the major churn drivers, and provide an interactive dashboard for retention decision-making.

## Dataset
- 7,043 customers
- 21 original features
- 1,869 churned customers
- Overall churn rate: 26.54%

## Tech Stack
- Python
- Pandas
- PostgreSQL
- SQL
- scikit-learn
- XGBoost
- Tableau Public
- Jupyter Notebook

## Project Workflow

1. Data cleaning and validation
2. PostgreSQL data loading
3. SQL-based churn analysis
4. Feature preprocessing
5. Model training and comparison
6. Threshold tuning
7. Customer risk scoring
8. Tableau dashboard development

## Key Business Insights

- Overall churn rate: 26.54%
- Month-to-month customers had the highest contract-based churn rate
- Electronic check customers had a churn rate of about 45%
- Customers in their first 12 months had a churn rate of about 47%
- Fiber optic customers showed substantially higher churn than DSL customers
- 1,035 customers were classified as High Risk
- Approximately $85K in monthly revenue was associated with High-Risk customers

## Machine Learning

Models evaluated:
- Logistic Regression
- Random Forest
- XGBoost

Logistic Regression was selected as the final model.

### Baseline Logistic Regression
- Accuracy: 80.1%
- Precision: 65.8%
- Recall: 52.4%
- F1 Score: 58.3%
- ROC-AUC: 83.7%

The classification threshold was reduced from 0.50 to 0.30 to improve churn detection.

### Final Threshold Performance
- Precision: 53%
- Recall: 74%
- F1 Score: 62%

This reduced the number of missed churners and better supported the retention use case.

## Risk Segmentation

Customers were grouped into:

- Low Risk: 0–30%
- Medium Risk: 30–60%
- High Risk: 60–100%

## Tableau Dashboard

The Tableau dashboard includes:

- Total Customers
- Churn Rate
- High-Risk Customers
- Monthly Revenue at Risk
- Churn by Contract Type
- Churn by Tenure
- Churn by Payment Method
- Churn by Internet Service
- High-Risk Customer Table
- Interactive Contract filter

## Project Architecture

CSV Data  
↓  
Python / Pandas  
↓  
PostgreSQL  
↓  
SQL Analysis  
↓  
Feature Engineering  
↓  
Machine Learning  
↓  
Churn Probability  
↓  
Risk Segmentation  
↓  
Tableau Dashboard  

## Repository Structure

```text
telco-churn-prediction/
├── data/
├── notebooks/
├── models/
├── sql/
├── requirements.txt
└── README.md