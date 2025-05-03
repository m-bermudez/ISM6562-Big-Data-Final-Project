# ISM6562-Big-Data-Final-Project
# 📊 Big Data Final Project: Communities and Crime Analysis

## 📝 Project Overview

This project explores the [UCI Communities and Crime dataset](https://archive.ics.uci.edu/dataset/183/communities+and+crime), which integrates socio-economic indicators with FBI crime data to understand factors influencing violent crime rates in U.S. communities.

We leverage Apache Spark within the Databricks Community Edition environment to:
- Clean and preprocess a high-dimensional dataset
- Query and analyze patterns using SparkSQL
- Build and evaluate predictive models using Spark MLlib
- Visualize insights and feature relationships

---

## 📁 Dataset Summary

- **Source**: [UCI ML Repository - Communities and Crime](https://archive.ics.uci.edu/dataset/183/communities+and+crime)
- **Instances**: 1,994
- **Attributes**: 128
- **Target Variable**: `ViolentCrimesPerPop` — the rate of violent crimes per 100K people in a community

### Key Data Categories
- Demographics (race, income, education)
- Housing and employment data
- Police resource allocation
- Community characteristics

---

## 🔄 Data Preparation

Steps included:

1. **Loading into Spark**
   - Used UCIML Repo then conversion into Spark Dataframe for ingestion with inferred schema and header mapping.

2. **Removing Non-Predictive Fields**
   - Dropped columns like `state`, `community`, `communityname`, and `fold`.

3. **Cleaning Anomalies**
   - Replaced "?" entries with nulls, then imputed or removed affected rows.

4. **Feature Engineering**
   - Normalized features where appropriate.
   - Combined or transformed variables to improve model inputs.

5. **Final Schema Validation**
   - Ensured all columns were numerical and usable for ML modeling.

---

## 🔍 Exploratory Data Analysis (EDA)

- Summary statistics and distribution plots of key features
- Correlation heatmap to explore feature relationships
- Visual comparisons of `ViolentCrimesPerPop` against education, income, and police funding

---

## 🛠 SparkSQL Implementation

Used SparkSQL for:
- Computing mean and max crime rates per region
- Filtering communities with extreme values
- Aggregating education and poverty indicators vs. crime rate
- Demonstrating joins and grouping for insights

---

## 🤖 Machine Learning Models

Implemented the following regression models using Spark MLlib:

1. **Linear Regression**
2. **Decision Tree Regressor**
3. **Random Forest Regressor**
4. **Gradient-Boosted Trees Regressor**

### Tools Used
- `VectorAssembler` for feature transformation
- `Pipeline` for structuring ML stages
- `RegressionEvaluator` using RMSE as the primary metric

---

## 💡 Advanced SparkML Features

- Use of ML Pipelines for consistent preprocessing and modeling
- Optional: Cross-validation and hyperparameter tuning
- Feature importance extraction for interpretation

---

## 📊 Visualizations

- Heatmap of feature correlations
- Distribution plots of violent crime rates
- Actual vs. predicted plots from models
- Feature importance bar charts

---
