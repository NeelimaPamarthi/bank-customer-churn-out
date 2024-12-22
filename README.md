# Customer Churn Prediction

This project is a machine learning application that predicts customer churn (whether a customer will leave a service or not) based on demographic and account-related features.

## Table of Contents

1. [Introduction](#introduction)
2. [Dataset](#dataset)
3. [Dependencies](#dependencies)
4. [Steps](#steps)
5. [Results](#results)

---

## Introduction

Customer churn is a critical business metric that indicates the percentage of customers leaving a service over a period of time. This project uses Logistic Regression to predict churn based on historical data.

---

## Dataset

The dataset (`Churn.csv`) contains customer information and features such as:
- **CustomerId**: Unique identifier for each customer
- **Surname**: Customer's surname
- **Geography**: Location of the customer
- **Gender**: Male or Female
- **Age**, **Balance**, **CreditScore**, and other numerical attributes
- **Exited**: Target variable (1 if the customer churned, 0 otherwise)

---

## Dependencies

The following Python libraries are required to run the project:
- `numpy`
- `pandas`
- `matplotlib`
- `seaborn`
- `scikit-learn`

Install them using pip:
```bash
pip install numpy pandas matplotlib seaborn scikit-learn
```

---

## Steps

### 1. Data Preprocessing
- Renamed columns to remove any leading/trailing spaces.
- Checked for and handled missing values.
- Dropped irrelevant features (`CustomerId` and `Surname`).
- Encoded categorical features:
  - Converted `Gender` to numeric (0: Male, 1: Female).
  - Used one-hot encoding for `Geography`.
- Split the dataset into features (`x`) and target (`y`).

### 2. Data Visualization
- **Class Distribution**: Visualized the proportion of churned vs. non-churned customers.
- **Feature Distribution**: Plotted histograms for all features to understand their distribution.
- **Correlation Heatmap**: Displayed correlations between features to identify relationships.

### 3. Data Standardization
- Standardized numerical features using `StandardScaler` to improve model performance.

### 4. Model Training
- Split the data into training and test sets (`70%` training, `30%` testing).
- Trained a Logistic Regression model using the training set.

### 5. Model Evaluation
- Calculated metrics:
  - **Accuracy**: Overall performance of the model.
  - **Confusion Matrix**: Classification performance for each class.
  - **Classification Report**: Precision, recall, and F1-score.

---

## Results

The Logistic Regression model achieved the following:
- **Accuracy**: `0.80`
- **Confusion Matrix**:
[[TN, FP], [FN, TP]]
- **Precision**, **Recall**, and **F1-Score**: Extracted from the classification report.

These results indicate that the model can predict customer churn with a reasonable degree of accuracy.

---
