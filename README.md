# Netflix Customer Churn Analysis

## Project Overview

This project analyzes customer churn behavior in a subscription-based streaming platform using data mining techniques. The objective is to identify customers at risk of leaving the service and discover the main factors associated with churn.

The project was developed using RapidMiner and includes data cleaning, exploratory data analysis, churn prediction, and customer segmentation.

---

## Problem Statement

Customer retention is a major challenge for subscription-based companies. When customers churn, the company loses recurring revenue and must spend more resources acquiring new customers.

This project uses the `churned` attribute to identify customer attrition and analyze the behavioral and demographic factors that contribute to customer loss.

---

## Dataset

The dataset contains customer-level information such as:

- customer_id
- age
- gender
- churned
- number_of_profiles
- avg_watch_time_per_day
- favorite_genre
- watch_hours
- monthly_fee
- subscription_type
- last_login_days
- region
- device
- payment_method

---

## Project Workflow

### 1. Data Understanding and Cleaning
The dataset was analyzed to identify attribute types, descriptive statistics, missing values, and outliers.

Cleaning steps included:
- handling missing values in age, gender, watch_hours, and monthly_fee
- detecting unrealistic outliers such as age = 200 and last_login_days = 500
- replacing outliers using RapidMiner operators

### 2. Exploratory Data Analysis
EDA was performed to understand customer behavior patterns and their relationship with churn.

Main findings include:
- churned users tend to have lower watch hours
- churned users tend to have higher last_login_days
- low engagement is strongly associated with churn

### 3. Churn Prediction
Decision tree models were used to predict churn and compare different splitting criteria.

### 4. Customer Segmentation
Clustering was applied to identify customer groups with different engagement patterns and possible outlier behavior.

---

## Key Findings

- `last_login_days` showed the strongest positive relationship with churn
- `watch_hours` showed a strong negative relationship with churn
- `avg_watch_time_per_day` also had a negative relationship with churn
- `monthly_fee` and `number_of_profiles` had weak relationships with churn

These findings suggest that inactivity and reduced engagement are the strongest indicators of customer churn.

---

## Tools Used

- RapidMiner
- Excel
- PDF reporting
- Presentation slides

---

## Repository Structure

```text
netflix-customer-churn-analysis/
│
├── README.md
├── data/
│   └── CleanedData.xlsx
├── rapidminer/
│   └── PROJECT DT.rmp
├── docs/
│   ├── Report.pdf
│   └── Netflix churn Presentation (1).pdf
└── images/
    └── churn_pipeline.png
