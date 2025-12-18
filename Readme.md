# 🏡 California Housing Price Prediction: Regression Analysis

## 📌 Project Overview
This project performs a comprehensive regression analysis on the **California Housing Dataset** to predict median house values (`MedHouseVal`). 

The goal is to build a robust model by injecting complexity through **Feature Engineering** (Polynomial features, Interactions, One-Hot Encoding) and comparing the generalization performance of standard **Linear Regression** against regularized models (**Ridge**, **Lasso**, **ElasticNet**).

---

## 🚀 Key Features
* **Dataset:** California Housing (via `sklearn.datasets`).
* **Feature Engineering:** * Binning `Latitude` into Geographic Zones (North/Central/South).
    * One-Hot Encoding for categorical regions.
    * Degree-2 Polynomial Features & Interaction terms.
* **Models Trained:**
    1.  Linear Regression (Baseline)
    2.  Ridge Regression ($L_2$ Regularization)
    3.  Lasso Regression ($L_1$ Regularization)
    4.  ElasticNet

---

## 📊 Results Summary
After training and evaluating on the test set (20% split), the **Standard Linear Regression** model achieved the best generalization performance.

| Model | Train MSE | Test MSE | Test R2 Score |
| :--- | :--- | :--- | :--- |
| **Linear Regression** | **0.4872** | **0.5120** | **0.6093** |
| Ridge (L2) | 0.4874 | 0.5168 | 0.6056 |
| Lasso (L1) | 0.5068 | 0.6814 | 0.4800 |
| ElasticNet | 0.4973 | 0.5966 | 0.5447 |

*Note: Lasso and ElasticNet required higher iterations to converge fully, highlighting the efficiency of the simpler Linear model for this specific feature set.*
