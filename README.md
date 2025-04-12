# 📉 Customer Churn Prediction

Predicting customer churn is crucial for telecom companies to retain users and reduce losses. This project uses a machine learning pipeline to predict whether a customer is likely to churn based on their service usage and demographic attributes.

---

## 📌 Project Overview

This project focuses on analyzing the Telco Customer Churn dataset to build a binary classification model that predicts customer churn (Yes/No). It involves extensive preprocessing, feature engineering, and the evaluation of multiple machine learning algorithms to determine which one provides the best performance.

---

## 📂 Dataset

- **Source**: Telco Customer Churn dataset
- **Size**: ~7,000 rows, ~20 features
- **Target column**: `Churn` (Yes/No)

---

## ⚙️ Features

The dataset includes:
- Demographic info: `gender`, `SeniorCitizen`, `Partner`, `Dependents`
- Account info: `tenure`, `Contract`, `PaymentMethod`
- Services signed up for: `InternetService`, `OnlineSecurity`, `TechSupport`, etc.
- Charges: `MonthlyCharges`, `TotalCharges`

Some features like `HaveDog`, `FeelsLonely`, and `UseTiktok` were dropped as irrelevant.

---

## 🧹 Preprocessing Steps

- Dropped irrelevant columns (`customerID`, `FeelsLonely`, etc.)
- Handled missing values using:
  - **Mean imputation** for numerical (`TotalCharges`)
  - **Most frequent value** for categorical (`StreamingTV`)
- Dropped rows with critical missing data
- Encoded categorical variables using `OrdinalEncoder`
- Scaled numeric values using `MinMaxScaler`
- Removed duplicate rows

---

## 🧠 Models Used

We trained and tested the following machine learning models:

| Model                 | Accuracy (%) |
|----------------------|--------------|
| Decision Tree         | ✅ Computed |
| Random Forest         | ✅ Computed |
| Logistic Regression   | ✅ Computed |
| Gaussian Naive Bayes  | ✅ Computed |

Each model was trained using a 70-30 train-test split and evaluated using accuracy score.

---

## 📈 Results

The accuracies of the models are visualized in a bar chart. Here's a quick summary:

- ✅ **Random Forest** generally performs best with good generalization.
- 🧠 **Logistic Regression** is fast and surprisingly strong for this kind of binary task.
- 🌲 **Decision Tree** can overfit if not tuned.
- 🐦 **Naive Bayes** performs reasonably well but makes simplifying assumptions.

*Exact accuracy values will be shown on GitHub when notebook runs.*

---

## 📊 Visualizations

- Churn class distribution using countplots
- Model accuracy comparison using barplots

---


