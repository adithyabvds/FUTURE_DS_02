# Customer Retention & Churn Analysis

## Project Overview

This project focuses on analyzing customer interaction data from an e‑commerce platform to better understand user behavior, identify churn patterns, and predict which customers are likely to stop using the platform.

Customer churn analysis is an important task for many online businesses, including e‑commerce platforms and SaaS companies. Retaining existing customers is often far more cost‑effective than acquiring new ones. By analyzing customer activity and engagement patterns, businesses can take proactive steps to improve retention and customer lifetime value.

The goal of this project is to convert raw user interaction data into meaningful insights and build a machine learning model capable of identifying customers who are at risk of churning.

---

## Objectives

The primary objectives of this project include:

* Understanding customer engagement patterns
* Identifying behavioral signals that indicate churn
* Performing time‑based activity analysis
* Building a machine learning model to predict churn
* Providing business recommendations to improve retention

---

## Dataset

Dataset Source:
[https://www.kaggle.com/datasets/dexterplayzx/customer-churn-dataset-for-retention-analysis](https://www.kaggle.com/datasets/dexterplayzx/customer-churn-dataset-for-retention-analysis)

The dataset contains event‑level records of user interactions on an e‑commerce platform. Each row represents a customer action such as viewing a product, adding an item to the cart, or completing a purchase.

### Key Attributes

| Column     | Description                                |
| ---------- | ------------------------------------------ |
| Event Time | Timestamp of user activity                 |
| Event Type | Type of interaction (view, cart, purchase) |
| Product ID | Unique identifier for a product            |
| Category   | Product category                           |
| Brand      | Product brand                              |
| Price      | Price of the product                       |
| User ID    | Unique identifier for the user             |

These attributes allow us to track user engagement and purchasing behavior over time.

---

## Data Formats Used

Two data formats were used during the project depending on the stage of analysis.

### CSV Format (Power BI Dashboard)

The processed dataset was exported in CSV format to build Power BI dashboards. CSV files are widely compatible with visualization tools and allow seamless integration with Power BI.

CSV files were mainly used for:

* Customer analytics dashboards
* Churn visualization
* Revenue insights
* Interactive business intelligence reports

---

### Parquet Format (Python Analysis)

During the Python analysis phase, the dataset was stored in Parquet format. Parquet is a column‑based storage format that is optimized for large datasets and provides faster read performance compared to traditional CSV files.

Parquet was used for:

* Data preprocessing
* Feature engineering
* Machine learning model training
* Large‑scale analysis using Pandas

Using Parquet significantly improved data loading speed and storage efficiency.

---

## Data Processing & Feature Engineering

The original dataset contained event‑level data. To better represent customer behavior, this data was aggregated into user‑level features.

### Features Created

| Feature         | Description                               |
| --------------- | ----------------------------------------- |
| Total Events    | Total number of user interactions         |
| Total Purchases | Number of purchases made by the user      |
| Total Spend     | Total amount spent by the user            |
| Unique Products | Number of unique products interacted with |
| First Activity  | First recorded interaction time           |
| Last Activity   | Most recent interaction time              |
| Lifetime Days   | Time between first and last activity      |
| Recency Days    | Days since last user interaction          |

These features help capture the engagement and purchasing behavior of each customer.

---

## Churn Definition

A customer was considered **churned** if they had no activity on the platform for more than **30 days**.

| Label | Meaning          |
| ----- | ---------------- |
| 0     | Active Customer  |
| 1     | Churned Customer |

---

## Machine Learning Model

A **Random Forest Classifier** was used to predict customer churn using the engineered behavioral features.

### Model Features

* Total Events
* Total Purchases
* Total Spend
* Unique Products
* Lifetime Days

---

## Model Performance

| Metric    | Score |
| --------- | ----- |
| Accuracy  | 53%   |
| Precision | 0.39  |
| Recall    | 0.78  |
| F1 Score  | 0.52  |

### Interpretation

The model identifies **78% of churned customers**, which allows businesses to detect at‑risk users early and implement retention strategies.

Although precision is relatively lower, the model is optimized to minimize missed churn cases, which is often more valuable in churn prediction scenarios.

---

## Key Insights

* Customers with **low engagement levels** are more likely to churn
* Users who make **multiple purchases** show stronger retention
* Higher **customer lifetime duration** correlates with better engagement
* Customer activity varies over time, suggesting seasonal or promotional influences

---

## Business Recommendations

Based on the findings, several strategies can help reduce customer churn:

1. Launch targeted retention campaigns for inactive users
2. Introduce loyalty programs to reward repeat customers
3. Implement personalized product recommendations
4. Improve onboarding and early user experience for new customers

---

## Power BI Dashboard

An interactive Power BI dashboard was created to visualize churn patterns, customer retention trends, and revenue insights.

Dashboard Link:
[https://app.powerbi.com/groups/me/reports/22ebf85a-286d-4c6c-8039-2ee9e19b0e84/25daa5b51309a806a070?experience=power-bi](https://app.powerbi.com/groups/me/reports/22ebf85a-286d-4c6c-8039-2ee9e19b0e84/25daa5b51309a806a070?experience=power-bi)

---

## Tools & Technologies

* Python
* Pandas
* NumPy
* Scikit‑learn
* Matplotlib
* Seaborn
* Jupyter Notebook
* Power BI

---

## Project Structure

```
FUTURE_DS_02

│
├── Data_Merging_Cleaning_Feature_Engineering.ipynb
├── Analysis_and_Conclusion.ipynb
├── Analysis_and_Conclusion.html
├── Final_Report.pdf
├── Customer Retention and Churn Analysis Dashboard.pdf
└── README.md
```

*Note: Large datasets are hosted on Kaggle due to GitHub file size limitations.*

---

## Conclusion

This project demonstrates how customer interaction data can be analyzed to uncover churn patterns and predict customer behavior. By combining exploratory data analysis with machine learning techniques, businesses can gain valuable insights into customer engagement and develop strategies to improve long‑term retention.

---

## Author

Adithya BV
B.Sc Data Science & Analytics
M.S. Ramaiah University of Applied Sciences

GitHub:
[https://github.com/adithyabvds](https://github.com/adithyabvds)
