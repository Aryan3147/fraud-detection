# 💳 Credit Card Fraud Detection using Machine Learning

Detecting fraudulent credit card transactions using supervised machine learning techniques. This project focuses on handling class imbalance and evaluating models using ROC AUC and other key metrics.

---

## 📁 Dataset

- **Source**: [Kaggle - Credit Card Fraud Detection](https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud)
- **Rows**: 284,807 transactions
- **Features**: 30 numerical features (V1–V28), `Amount`, `Time`
- **Target**: `Class`
  - `0`: Legitimate
  - `1`: Fraudulent

---

## 🧹 Data Preprocessing

- Dropped `Time` column as it wasn't meaningful without transformation.
- Scaled `Amount` using `StandardScaler`.
- Checked for and removed missing values (none found).
- Handled class imbalance with either:
  - Sampling for faster training
  - (Optionally) SMOTE or `class_weight='balanced'`

---

## ⚙️ Models Used

- **Logistic Regression**
- **Random Forest Classifier**

---

## 📊 Model Performance

| Metric        | Logistic Regression | Random Forest |
|---------------|---------------------|----------------|
| ROC AUC Score | 0.7907              | 0.8877         |
| Accuracy      | ~99.2%              | ~99.4%         |
| Precision     | High for Class 0    | High for both  |
| Recall        | Low for Class 1     | Improved for Class 1 |

> Note: Due to heavy class imbalance (only ~0.17% fraud), ROC AUC and Recall are more important than Accuracy.

---

## 📈 ROC Curve

![ROC Curve](path_to_roc_curve_image.png)  
*ROC Curve for Random Forest Model*

---

## 📬 Contact

Created by **Aryan Gaikwad**  
📧 aryangaikwad3986@gmail.com | 🔗 www.linkedin.com/in/aryan-gaikwad-9bb560285
