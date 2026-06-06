# California Housing Price Prediction

## Project Overview

This project focuses on predicting California housing prices using machine learning techniques on the California Housing Prices dataset from Kaggle.

The objective is to build an accurate regression model that can estimate the median house value of a district based on demographic, geographic, and economic features.

Unlike a simple model-building exercise, this project includes a complete machine learning workflow consisting of:

* Data cleaning
* Missing value treatment
* Exploratory Data Analysis (EDA)
* Feature Engineering
* Model Development
* Model Comparison
* Performance Evaluation

---

## Dataset

Dataset Source:

California Housing Prices Dataset (Kaggle)

The dataset contains housing information collected from the 1990 California census, including:

* Longitude
* Latitude
* Housing Median Age
* Total Rooms
* Total Bedrooms
* Population
* Households
* Median Income
* Median House Value

Target Variable:

**median_house_value**

---

## Problem Statement

The goal is to predict the median house value of a district using various demographic and housing-related attributes.

This is a supervised machine learning regression problem.

---

## Data Cleaning & Preprocessing

### Missing Value Handling

The dataset contained missing values in the `total_bedrooms` column.

Instead of using simple mean or median imputation, a machine learning-based approach was used:

* Correlation analysis was performed.
* `households` showed strong correlation with `total_bedrooms`.
* A Linear Regression model using SGDRegressor was trained.
* Predicted values were used to fill missing entries.

This approach preserves relationships within the dataset better than traditional imputation methods.

---

## Exploratory Data Analysis (EDA)

Several analyses were performed:

* Correlation Matrix
* Scatter Plot Analysis
* Feature Relationship Investigation
* Geographic Distribution Analysis

EDA helped identify the most influential variables affecting housing prices.

Key observations:

* Median Income has strong influence on house prices.
* Geographic location plays a major role.
* Household-based metrics provide more meaningful information than raw counts.

---

## Feature Engineering

To improve model performance, new features were created:

### Household-Based Features

* rooms_per_household
* bedrooms_per_household
* population_per_household

### Geographic Features

Latitude and longitude were divided into geographic regions to capture location-based pricing patterns.

These engineered features improved the model's ability to learn housing price behavior.

---

## Machine Learning Models Tested

Multiple regression algorithms were trained and compared.

### Linear Regression (SGDRegressor)

Used as a baseline model.

### XGBoost Regressor

Gradient boosting model capable of handling non-linear relationships.

### LightGBM Regressor

Fast and efficient gradient boosting framework.

### Random Forest Regressor

Ensemble tree-based regression model.

---

## Model Evaluation

The models were evaluated using:

* Mean Squared Error (MSE)
* Root Mean Squared Error (RMSE)
* R² Score

The comparison allowed objective selection of the best-performing model.

### Best Performing Model

🏆 LightGBM Regressor

LightGBM achieved the lowest prediction error and delivered the strongest overall performance on the test data.

---

## Technologies Used

### Programming Language

* Python

### Data Analysis

* Pandas
* NumPy

### Visualization

* Matplotlib
* Seaborn

### Machine Learning

* Scikit-Learn
* XGBoost
* LightGBM

### EDA

* ydata-profiling

---

## Project Workflow

1. Data Collection
2. Data Cleaning
3. Missing Value Prediction
4. Exploratory Data Analysis
5. Feature Engineering
6. Model Training
7. Model Evaluation
8. Model Comparison
9. Best Model Selection

---

## Results

Key achievements of the project:

✅ Machine Learning-based missing value imputation

✅ Feature engineering using domain knowledge

✅ Geographic segmentation analysis

✅ Comparison of multiple regression algorithms

✅ Identification of the best-performing model

✅ End-to-end machine learning pipeline

---

## Notebook

The complete implementation, analysis, and model comparison can be found in:

`California_ML.ipynb`

---

## Author

### Nidhi Devrani

Aspiring Data Analyst passionate about data analytics, machine learning, and transforming data into actionable insights.

LinkedIn:
[www.linkedin.com/in/nidhi-devrani-b79159349](http://www.linkedin.com/in/nidhi-devrani-b79159349)

