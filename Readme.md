# 📊 BMI Prediction Using Cardiovascular Health Indicators
## A Regression Analysis Study
## 📌 Project Overview

This project investigates whether cardiovascular and lifestyle health indicators can be used to predict Body Mass Index (BMI) using regression models.

The dataset was originally designed for heart disease prediction, but in this study, BMI was selected as the target variable to evaluate whether indirect health features are sufficient predictors.

The primary goal was not only predictive performance but also to evaluate feature–target relationships and dataset suitability for regression modeling.

## 📂 Dataset Source

Dataset obtained from:

Kaggle – Heart Disease Prediction Dataset

### ⚠️ Important Note:
The dataset was originally structured for heart disease classification, not BMI prediction.

## 🔎 Research Question

Can cardiovascular indicators (cholesterol, blood pressure, stress level, smoking status, etc.) reliably predict BMI without using direct anthropometric measurements such as height and weight?

## 🧪 Methodology
### 1️⃣ Data Preprocessing

Removed missing values

Train–test split (80/20)

Feature scaling using StandardScaler

Correlation analysis

### 2️⃣ Models Implemented

Ridge Regression

Random Forest Regressor

Neural Network (MLP Regressor)

### 3️⃣ Evaluation Metric

R² Score

Mean Squared Error (MSE)

## 📉 Key Finding: Extremely Weak Feature Correlation

Correlation analysis revealed:

Most features had correlation values around 0.02 with BMI

Very weak linear relationship between predictors and target

No strong statistical dependency between cardiovascular indicators and BMI

This indicates that the dataset lacks predictive signal for BMI.

## 📊 Model Results
Model	Test R² Score
Ridge Regression	-0.009
Random Forest	-0.004
Neural Network	-0.080
Interpretation:

A negative R² score means:

The model performs worse than simply predicting the mean BMI for all samples.

This confirms that the dataset does not contain sufficient information to predict BMI effectively.

## 🧠 Scientific Interpretation

The poor performance is not due to model weakness but due to dataset–target mismatch.

BMI is primarily calculated using:

Height

Weight

These key anthropometric features were not present in the dataset.

Instead, the dataset contains indirect lifestyle and cardiovascular indicators, which show negligible correlation with BMI.

Therefore:

Cardiovascular markers alone are insufficient predictors of BMI.

The dataset is structurally unsuitable for BMI regression.

## 🎯 Conclusion

This study demonstrates the importance of:

Proper dataset–target alignment

Correlation analysis before modeling

Evaluating feature relevance before selecting prediction tasks

While multiple regression models were implemented correctly, the dataset lacked predictive signal for BMI, resulting in near-zero or negative R² scores.

This highlights a critical lesson in data science:

Model performance is fundamentally limited by the quality and relevance of the data.

## 🚀 Future Work

Use a dataset containing height and weight for meaningful BMI prediction.

Instead of BMI, predict a target aligned with the dataset purpose (e.g., heart disease risk).

Perform feature selection before choosing a regression objective.

Explore statistical tests to quantify feature significance.

## 🛠 Technologies Used

- Python

- Pandas

- NumPy

- Matplotlib

- Seaborn

- Scikit-learn

## 📌 Key Learning Outcome

This project emphasizes that:

Strong modeling techniques cannot compensate for weak feature–target relationships.

Dataset suitability analysis is a critical first step in any machine learning project.

Negative results can provide meaningful scientific insights when interpreted correctly.
