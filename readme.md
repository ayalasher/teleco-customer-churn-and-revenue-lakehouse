# Databricks Telecom Churn Lakehouse Project

## Overview

This project demonstrates how to build an end‑to‑end data engineering and machine learning pipeline using the Lakehouse architecture on Databricks. The goal is to ingest telecom customer data, transform it through a multi‑layer data architecture (Bronze, Silver, and Gold), and train a machine learning model to predict customer churn.

The project simulates a real-world telecom analytics workflow where raw operational data is transformed into analytics-ready datasets and then used for predictive modeling.

---

# Architecture

The project follows the Lakehouse Medallion Architecture:

* **Bronze Layer** – Raw ingested telecom data
* **Silver Layer** – Cleaned and transformed data
* **Gold Layer** – Aggregated datasets optimized for analytics and ML

Pipeline Flow:

Raw Data → Bronze Tables → Silver Transformations → Gold Feature Tables → ML Model Training → Churn Predictions

---

# Project Objectives

* Build an end-to-end **data pipeline using Databricks**
* Implement the **Medallion Lakehouse architecture**
* Perform **data cleaning and feature engineering**
* Train and evaluate a **customer churn prediction model**
* Demonstrate **production-style data engineering practices**

---

# Tech Stack

**Platform**

* Databricks
* Delta Lake

**Languages**

* Python
* SQL

**Libraries**

* PySpark
* Pandas
* Scikit-learn

**Data Engineering Tools**

* Delta Tables
* Databricks Notebooks
* Spark SQL

---

# Dataset

The dataset represents telecom customer data including:

* Customer demographics
* Account information
* Service usage
* Billing details
* Customer churn label

Target Variable:

* `Churn` (Yes / No)

---

# Data Pipeline

## 1. Data Ingestion (Bronze Layer)

Raw telecom data is ingested into Delta tables without modification.

Key tasks:

* Load CSV dataset
* Store raw data in Delta format
* Maintain schema consistency

Output:

* `bronze_customers`

---

## 2. Data Cleaning & Transformation (Silver Layer)

The Silver layer focuses on preparing clean, structured data.

Key tasks:

* Handle missing values
* Normalize categorical fields
* Convert data types
* Remove duplicates

Output:

* `silver_customers_clean`

---

## 3. Feature Engineering (Gold Layer)

The Gold layer creates analytics-ready datasets.

Key tasks:

* Create churn-related behavioral features
* Encode categorical variables
* Create ML-ready feature tables

Output:

* `gold_churn_features`

---

# Machine Learning Pipeline

## Problem

Predict whether a telecom customer will churn.

## Model Used

Logistic Regression

## Steps

1. Feature selection
2. Train-test split
3. Model training
4. Model evaluation

## Evaluation Metrics

* Accuracy
* Precision
* Recall
* F1 Score

---

# Results

The trained model provides churn predictions that can help telecom companies:

* Identify high-risk customers
* Improve retention strategies
* Reduce revenue loss from churn

---

# Repository Structure

```
teleco-churn-lakehouse
│
├── notebooks/
│   ├── 01_bronze
│   ├── 02_silver
│   ├── 03_gold
│   ├── 04_feature_engineering
│   ├── 05_model_training
│   ├── 06_model_evaluation
│   ├── 07_serving predictions
│   └── 08_ml_flow_tracking
│
├── data/
│   └── sample_dataset
│
├── README.md
└── requirements.txt
```

---

# How to Run the Project

1. Import the notebooks into Databricks
2. Upload the dataset to DBFS
3. Run the notebooks in order:

* Data Ingestion
* Data Transformation
* Feature Engineering
* ML Modeling

---

# Key Learnings

* Implementing the Lakehouse Medallion Architecture
* Building scalable data pipelines using Spark
* Managing Delta Lake tables
* Feature engineering for churn prediction
* Training ML models within a data engineering workflow
* Add automated workflows with Databricks Jobs
* Implement MLflow experiment tracking

---

# Future Improvements

* Deploy model as an API
* Add real-time streaming data ingestion

---

# Author

Maxwel Ayal

Data Engineer | Python | SQL | Spark | ETL Pipelines

---
