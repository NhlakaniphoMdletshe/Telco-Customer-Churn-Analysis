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
![Project Screenshot](https://github.com/NhlakaniphoMdletshe/Telco-Customer-Churn-Analysis/blob/main/images/img1.png)
Most customers remained, but a significant portion of them churned. This imbalance may affect model performance.

### 2. Tenure Distribution by Churn
![Project Screenshot](https://github.com/NhlakaniphoMdletshe/Telco-Customer-Churn-Analysis/blob/main/images/img2.png)
Customers who churn generally have shorter tenure, highlighting the importance of early retention strategies.

### 3. Contract Type vs Churn
![Project Screenshot](https://github.com/NhlakaniphoMdletshe/Telco-Customer-Churn-Analysis/blob/main/images/img3.png)
Month-to-month contract holders are at the highest risk of churn, whereas 1-year and 2-year contracts show lower churn.

### 4. Feature Correlation Heatmap
![Project Screenshot](https://github.com/NhlakaniphoMdletshe/Telco-Customer-Churn-Analysis/blob/main/images/img4.png)
- Positive correlation between `MonthlyCharges` and churn suggests high charges may influence leaving.  
- Strong correlation between `tenure` and `TotalCharges` is expected; longer tenure equals higher total charges.

## Modeling Approach
I trained four models:
- Logistic Regression
- Decision Tree
- Random Forest
- XGBoost

### Metrics for evaluation:
- Accuracy
- Precision
- Recall
- F1 Score
- ROC-AUC
- Confusion Matrix

## Model Evaluation & Comparison
### Performance Table
![Project Screenshot](https://github.com/NhlakaniphoMdletshe/Telco-Customer-Churn-Analysis/blob/main/images/img5.png)

### Metrics Visualization
![Project Screenshot](https://github.com/NhlakaniphoMdletshe/Telco-Customer-Churn-Analysis/blob/main/images/img6.png)
- Random Forest and XGBoost provide the best balance of F1 and ROC-AUC.  
- Logistic Regression is strong in interpretability but slightly lower in predictive power.

### Confusion Matrix Example (Random Forest)
![Project Screenshot](https://github.com/NhlakaniphoMdletshe/Telco-Customer-Churn-Analysis/blob/main/images/img7.png)
The model correctly identifies most churned customers while keeping false positives low. This is important for targeting retention campaigns efficiently.

## Key Insights
- Month-to-month contract holders churn more frequently.  
- Fiber optic internet users have higher churn than DSL.  
- Customers within the first year are at the highest churn risk.  
- Electronic check payment users show higher churn.  
- Longer tenure and multi-year contracts reduce churn probability.

## Recommendations
- **Incentivize long-term contracts:** Offer discounts or benefits for 1-year and 2-year plans.  
- **Bundle services:** Combine internet and security services to increase stickiness.  
- **Target high-risk segments:** Early intervention campaigns for new customers, fiber users, and electronic check payers.  
- **Monitor metrics:** Continuously track churn rates and model performance to adapt strategies.

## Clarifying Questions & Assumptions
**Questions for Stakeholders:**  
- How is churn defined? Temporary suspensions or permanent departures?  
- How often should the model be retrained?

**Assumptions & Caveats:**  
- Missing `TotalCharges` filled with median.  
- Models trained on historical data; future trends may differ.  
- Correlations indicate trends but not causation.





