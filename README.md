# Telco-Customer-Churn-Analysis

### Used Tools: Python, Jupyter Notebook, Pandas, Scikit-Learn, XGBoost, Matplotlib, Seaborn
### Project Type:  Data Cleaning, Exploratory Data Analysis, Data Visualization, Classification
### Type: Stakeholder

## Table of Contents
1. Project Background
2. Executive Summary
3. Dataset Overview
4. Exploratory Data Analysis
5. Modeling Approach
6. Model Evaluation & Comparison
7. Key Insights
8. Recommendations
9. Clarifying Questions & Assumptions

## Project Background
Telecommunications companies often face **customer churn**, where customers leave for competitors.  
Reducing churn improves revenue and reduces customer acquisition costs. 
This project aims to:
- Predict which customers are likely to churn.
- Identify features driving churn.
- Provide actionable recommendations to reduce churn.

## Executive Summary
- **High churn risk:** Customers on month-to-month contracts, using fiber internet, and paying by electronic check.  
- **Retention opportunities:** Customers with longer tenure and multi-year contracts are less likely to churn.  
- **Modeling results:** Random Forest and XGBoost outperform simpler models in accuracy, F1, and ROC-AUC.  
- **Recommendations:** Incentivize longer contracts, improve service bundles, and target high-risk segments proactively.

## Dataset Overview
The dataset has **7,043 customer records** with features like:
- **Customer demographics:** `gender`, `SeniorCitizen`, `Partner`, `Dependents`  
- **Account info:** `tenure`, `Contract`, `PaymentMethod`, `MonthlyCharges`, `TotalCharges`  
- **Services:** `PhoneService`, `InternetService`, `OnlineSecurity`, `MultipleLines`  
- **Target variable:** `Churn` (0 = Stayed, 1 = Left)

  ## Exploratory Data Analysis (EDA)
I visualized the trends in churn, tenure, contract type, and feature correlations.

### 1. Customer Churn Distribution
<img src="Telco_Customer_Churn_Prediction/img1.png" alt="Project Screenshot"/>


