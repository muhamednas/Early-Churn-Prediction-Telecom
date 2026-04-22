# 📞 Early Churn Prediction in Telecom

![Python](https://img.shields.io/badge/python-3.12-blue.svg)
![Scikit-Learn](https://img.shields.io/badge/scikit--learn-latest-orange.svg)
![XGBoost](https://img.shields.io/badge/xgboost-3.0.2-green.svg)
![Pandas](https://img.shields.io/badge/pandas-data%20analysis-red.svg)

Predicting customer churn is critical for telecommunications companies to maintain market share. This project utilizes machine learning to identify at-risk customers by analyzing demographics, account details, and service usage patterns.

## 🚀 Project Overview
The objective is to build a robust classification pipeline that predicts the likelihood of a customer leaving (churning) based on historical data. This enables the business to implement proactive retention strategies, such as targeted discounts or personalized service upgrades.

## 📊 Dataset Highlights
The analysis is based on the Telco Customer Churn dataset, covering:
* **Demographics:** Gender, senior citizen status, partners, and dependents.
* **Services:** Phone, multiple lines, internet (DSL/Fiber optic), online security, tech support, and streaming.
* **Account Info:** Tenure, contract type, payment method, paperless billing, monthly charges, and total charges.

## 🛠️ Workflow & Implementation

### 1. Data Cleaning & Preprocessing
* **Numeric Conversion:** Converted `TotalCharges` to numeric, handling missing values by dropping rows with null entries.
* **Label Encoding:** Transformed binary categories (e.g., "Yes"/"No") into numeric (1/0).
* **One-Hot Encoding:** Applied to multi-class categorical features using `pd.get_dummies`.

### 2. Feature Engineering
* **Tenure Grouping:** Created a `tenure_group` feature to categorize customers into segments (e.g., 0-1 year, 1-2 years, 5+ years) to better capture loyalty patterns.
* **Scaling:** Standardized features using `StandardScaler` to ensure optimal performance for distance-based models.

### 3. Exploratory Data Analysis (EDA)
* Visualized churn distribution via count plots.
* Analyzed the relationship between churn and numeric variables (Tenure and Monthly Charges) using boxplots.

### 4. Model Benchmarking
We compared multiple models to find the best balance between precision and recall:

| Model | Accuracy | Key Insight |
| :--- | :--- | :--- |
| **Random Forest** | **78.82%** | Highest overall accuracy. |
| **Logistic Regression**| **78.60%** | Excellent baseline and interpretability. |
| **XGBoost** | **77.54%** | Strong performance in capturing complex patterns. |
| **Decision Tree** | **75.26%** | Useful for visual understanding of splits. |

## 📈 Key Findings
* Customers with **shorter tenure** are significantly more likely to churn.
* **Monthly charges** play a visible role in decision-making for churned customers.
* The Logistic Regression model demonstrated the highest **recall** for non-churned customers (96%), while Random Forest provided a balanced performance across both classes.

## 💻 Installation
1. Clone the repository:
   ```bash
   git clone [https://github.com/yourusername/Early-Churn-Prediction-Telecom.git](https://github.com/yourusername/Early-Churn-Prediction-Telecom.git)
