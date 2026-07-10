# customer-churn-analysis-and-prediction
End-to-end customer churn analysis and predictive modeling using Python and scikit-learn.

# SaaS Customer Churn Analysis

| Category           | Details                                                  |
| ------------------ | -------------------------------------------------------- |
| Project Type       | Data Analysis + Machine Learning                         |
| Domain             | SaaS Customer Retention                                  |
| Dataset            | Customer Subscription, Usage & Churn Data                |
| Tools              | Python, Pandas, NumPy, Matplotlib, Seaborn, Scikit-learn |
| Notebook           | `CODE/customer-churn-analysis-and-prediction.ipynb`      |
| Models Used        | Logistic Regression, Decision Tree, Random Forest        |
| Best Model         | Random Forest                                            |
| Evaluation Metrics | Accuracy, Classification Report, ROC-AUC                 |

---

# Project Overview

This project analyzes customer subscription and behavioral data to identify patterns that influence SaaS customer churn.

The objective is to understand why customers leave, identify important churn indicators, and build machine learning models to predict customers who are likely to churn.

The project covers:

* Data cleaning and preprocessing
* Exploratory Data Analysis (EDA)
* Customer churn pattern analysis
* Business insights and recommendations
* Machine learning model development
* Model evaluation and feature importance analysis

---

# Project Structure

```text
customer-churn-analysis/
│
├── DATA/
│   ├── customer_subscription_churn_usage_patterns.csv
│   └── cleaned_customer_churn.csv
│
├── CODE/
│   └── customer-churn-analysis-and-prediction.ipynb
│
└── README.md
```

---

# Dataset Description

The dataset contains customer subscription, usage, and engagement information.

| Feature                | Description                    |
| ---------------------- | ------------------------------ |
| user_id                | Unique customer identifier     |
| signup_date            | Customer registration date     |
| plan_type              | Subscription plan category     |
| monthly_fee            | Monthly subscription cost      |
| avg_weekly_usage_hours | Average weekly product usage   |
| support_tickets        | Number of support requests     |
| payment_failures       | Number of payment failures     |
| tenure_months          | Customer relationship duration |
| last_login_days_ago    | Days since last login          |
| churn                  | Customer churn status          |

### Dataset Size

* Original records: 2,810 customers
* Duplicate records removed: 10
* Final dataset size: 2,800 customers

---

# Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-learn
* Jupyter Notebook

---

# Data Cleaning

The dataset was checked for:

* Missing values
* Duplicate records
* Duplicate customer profiles

### Missing Values

No missing values were found.

### Duplicate Records

10 exact duplicate records were removed.

Duplicate profiles were also checked while ignoring the unique `user_id` column. No repeated customer profiles were identified.

---

# Exploratory Data Analysis

## Customer Churn Distribution

The dataset contains:

* Churned customers: 1,605
* Retained customers: 1,195

Overall churn rate:

**57.32%**

This indicates that customer retention is a major challenge.

---

# Key Analysis Insights

## Subscription Plan Analysis

Churn was analyzed across:

* Basic
* Standard
* Premium

### Insight

Churn distribution was similar across all subscription plans.

This indicates that subscription type alone is not a strong churn driver. Customer behavior and engagement metrics have a greater influence.

---

## Usage Behavior Analysis

Feature analyzed:

`avg_weekly_usage_hours`

### Insight

Customers who churned showed lower minimum usage levels compared to retained customers.

Lower product engagement may increase churn risk.

---

## Login Activity Analysis

Feature analyzed:

`last_login_days_ago`

### Insight

Churned customers generally had longer periods of inactivity.

Customer inactivity is an important indicator of possible churn risk.

---

## Payment Failure Analysis

Feature analyzed:

`payment_failures`

### Insight

Payment failures showed overlap between churned and retained customers.

Payment issues alone are not enough to explain churn but may contribute when combined with other customer behavior factors.

---

## Support Ticket Analysis

Feature analyzed:

`support_tickets`

### Insight

Support ticket patterns were similar between churned and retained customers.

A combination of multiple customer signals is more useful than a single metric.

---

## Tenure Analysis

Feature analyzed:

`tenure_months`

### Insight

Average tenure was similar between churned and retained customers.

Customer lifetime alone is not a strong churn indicator in this dataset.

---

# Machine Learning Model Development

Machine learning models were developed to predict customer churn.

## Workflow

1. Feature selection
2. Data encoding
3. Train-test split
4. Feature scaling
5. Model training
6. Model evaluation

---

# Models Used

## Logistic Regression

A baseline classification model for binary churn prediction.

Performance:

* Accuracy: **66.79%**
* ROC-AUC Score: **0.701**

---

## Decision Tree Classifier

A non-linear model that learns decision rules from customer data.

Performance:

* Accuracy: **60.89%**

---

## Random Forest Classifier

An ensemble model combining multiple decision trees to improve prediction performance.

Performance:

* Accuracy: **66.96%**

---

# Model Comparison

| Model               | Accuracy |
| ------------------- | -------: |
| Random Forest       |   66.96% |
| Logistic Regression |   66.79% |
| Decision Tree       |   60.89% |

### Best Performing Model

**Random Forest Classifier**

Random Forest achieved the highest accuracy among the tested models.

---

# Feature Importance

Feature importance analysis identified the factors contributing most to churn prediction.

Important factors include:

* Customer engagement
* Usage behavior
* Login activity
* Payment issues
* Support interactions
* Subscription-related factors

---

# Business Recommendations

Based on the analysis:

* Improve customer onboarding and product education.
* Identify inactive users early and create re-engagement campaigns.
* Monitor usage patterns to detect churn risk.
* Combine multiple customer behavior factors for better predictions.
* Provide proactive support for customers experiencing payment issues.

---

# Conclusion

This project analyzed SaaS customer churn using exploratory data analysis and machine learning techniques.

Three classification models were developed:

* Logistic Regression
* Decision Tree
* Random Forest

Among these models, Random Forest achieved the best performance.

The analysis shows that customer engagement and activity patterns play an important role in churn prediction. Predictive analytics can help SaaS businesses identify at-risk customers early and develop effective retention strategies.

