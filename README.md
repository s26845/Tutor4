# **Breast Cancer Classification Project**

This project focuses on building and evaluating machine learning models to classify breast cancer tumors as benign or malignant using the **Breast Cancer Wisconsin (Diagnostic) Dataset**.

---

## **Objective**
The goal of this project is to:
1. Compare the performance of three machine learning models:
   - Logistic Regression
   - Random Forest
   - K-Nearest Neighbors (KNN)
2. Evaluate the models based on accuracy, precision, recall, and F1-score.
3. Select the best-performing model and discuss trade-offs.

---

## **Dataset**
The dataset used for this project is the **Breast Cancer Wisconsin (Diagnostic) Dataset**, available on Kaggle:
- **Source**: [Breast Cancer Wisconsin Data](https://www.kaggle.com/uciml/breast-cancer-wisconsin-data)
- **Features**:
  - Includes 30 numerical features representing various measurements of cell nuclei.
  - Target variable (`diagnosis`): `M` (Malignant) or `B` (Benign).

---
## **Project Workflow**

### **1. Data Preprocessing**
- Remove irrelevant columns (`id` and `Unnamed: 32`).
- Encode the target variable (`M` -> 1, `B` -> 0).
- Standardize the features to ensure all models work efficiently.

### **2. Model Training**
- Train the following models:
  - **Logistic Regression**: A simple and interpretable baseline model for binary classification.
  - **Random Forest**: An ensemble model that captures feature interactions and reduces overfitting.
  - **KNN (K-Nearest Neighbors)**: A non-parametric, distance-based model.
    
 ----
 ## **Key Observations**

### Logistic Regression:
- The best model in terms of **accuracy (97.37%)** and **F1-score (96.47%)**.
- Ideal for scenarios where both interpretability and performance are critical.
- Performs well without overfitting despite the simple linear decision boundary.

### Random Forest:
- Slightly behind Logistic Regression but showed the **highest precision (97.56%)**.
- A robust choice when reducing false positives is crucial, such as in diagnosing malignant cases.

### KNN:
- The least accurate model, with lower precision and F1-score.
- Consistently strong **recall (93.02%)**, indicating it effectively identifies malignant cases.
- Sensitivity to hyperparameters (e.g., `k`) and computational overhead were limiting factors.

---

## **Best Model**

- **Logistic Regression** is the best-performing model overall, combining:
  - The highest accuracy and F1-score.
  - Simplicity and interpretability.
  - Computational efficiency for deployment in clinical or diagnostic systems.
