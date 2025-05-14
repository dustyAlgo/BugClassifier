# 🐞 Bug Prediction using KNN and Logistic Regression

This project applies machine learning techniques to predict software bugs using the dataset `Antfile17.CSV`. The main goal is to classify whether a software module contains a bug (1) or not (0) based on 20 features.

## 📂 Dataset

- **File:** `Antfile17.CSV`
- **Features:** 20 software metrics (columns)
- **Label:** `bug` (0 = No Bug, 1 = Bug)

---

## ⚙️ Project Structure

### 🔹 KNN Classifier
Applies the K-Nearest Neighbors algorithm in two ways:
1. **Random `k` value** (e.g., 5)
2. **Best `k` value** (based on accuracy from range `k = 1 to 30`)

#### Steps:
- Load dataset and check class distribution
- Apply SMOTE Tomek if the data is imbalanced
- Train-test split: **90% train / 10% test**
- Standardize features using `StandardScaler`
- Train KNN and evaluate:
  - Accuracy
  - Confusion Matrix
  - Classification Report
- Plot accuracy vs. `k` values to choose optimal `k`

---

### 🔹 Logistic Regression
Implements Logistic Regression with model evaluation and visualization.

#### Steps:
- Load and balance dataset (SMOTE Tomek if required)
- Train-test split: **80% train / 20% test**
- Standardize features
- Train logistic regression model
- Evaluate using:
  - Accuracy
  - Confusion Matrix (with heatmap)
  - Classification Report
  - ROC Curve with AUC score

---

## 📦 Requirements

Install all required packages:

```bash
pip install scikit-learn
pip install imbalanced-learn
pip install seaborn
