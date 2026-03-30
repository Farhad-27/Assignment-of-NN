# Problem Set 02: Bank Marketing Prediction

## Project Overview
This project aims to predict whether a customer will subscribe to a term deposit based on their banking behavior using **Logistic Regression**.

## Dataset
- **Name:** Bank Marketing Data Set
- **Source:** Provided UCI Machine Learning Repository link
- **Attributes:** 17 (Demographics, account details, previous contact info, etc.)

## Methodology
- **Data Preprocessing:** Handled categorical data using One-Hot Encoding.
- **Scaling:** Used `StandardScaler` to normalize numerical features.
- **Data Splitting:** Divided data into Training (70%), Validation (10%), and Testing (20%).
- **Model:** Logistic Regression with `max_iter=1000`.

## Evaluation Results
- **Training Accuracy:** **91%**
- **Validation Accuracy:** **91%**
- **Testing Accuracy:** **90%**
- **AUC Score:** 0.90

## Findings
- The model shows strong predictive power with a high AUC score.
- Banking duration and previous outcomes were key factors in predicting subscriptions.
- No significant overfitting was observed as Training and Validation accuracies are consistent.

## Usage
1. Open `code.ipynb` in Google Colab.
2. Upload dataset.
3. Run all cells sequentially.
4. View outputs including accuracy, confusion matrix, and ROC curve.
