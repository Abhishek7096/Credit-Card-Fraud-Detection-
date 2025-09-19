# 💳 Credit Card Fraud Detection

## 📌 Project Overview
This project focuses on detecting fraudulent credit card transactions using **Machine Learning**.  
The dataset is highly imbalanced, with fraud cases making up less than 0.2% of all transactions.  

The main goal is to build a model that:
- Accurately detects fraudulent transactions.
- Minimizes false negatives (missed frauds).
- Handles data imbalance effectively.

---

## 📂 Dataset
- Source: [Kaggle – Credit Card Fraud Detection](https://www.kaggle.com/mlg-ulb/creditcardfraud)  
- Transactions: **284,807**  
- Fraud Cases: **492 (0.17%)**  
- Features:  
  - `V1`–`V28`: anonymized PCA-transformed features  
  - `Amount`, `Time`: transaction details  
  - `Class`: target variable (0 = Not Fraud, 1 = Fraud)  

---

## ⚙️ Project Workflow
1. **Data Exploration** – Understanding distribution and imbalance.  
2. **Data Preprocessing** – Feature scaling (`Amount`, `Time`).  
3. **Handling Imbalance** – Applied **SMOTE** to oversample fraud cases.  
4. **Model Training** – Used **Random Forest Classifier**.  
5. **Evaluation** – Confusion Matrix, Classification Report, ROC-AUC.  
6. **Feature Importance** – Identified which features contribute most to fraud detection.  

---

## 📊 Results

### 🔹 Confusion Matrix Heatmap
![Confusion Matrix](images/confusion_matrix.png)

- True Negatives (Correctly predicted non-fraud): **56,847**  
- False Positives (Normal marked as fraud): **17**  
- False Negatives (Fraud missed): **18**  
- True Positives (Correctly predicted fraud): **80**

---

### 🔹 Classification Report
| Metric      | Class 0 (Not Fraud) | Class 1 (Fraud) |
|-------------|---------------------|-----------------|
| Precision   | 1.00                | 0.82            |
| Recall      | 1.00                | 0.82            |
| F1-Score    | 1.00                | 0.82            |

- **Accuracy:** ~99.96%  
- **ROC-AUC Score:** **0.97** (Excellent)  

---

### 🔹 ROC Curve
![ROC Curve](images/roc_curve.png)

- The model achieved an **AUC of 0.97**, indicating excellent ability to separate fraud from non-fraud cases.  

---

### 🔹 Class Distribution
![Fraud Distribution](images/class_distribution.png)

- Fraud cases are **extremely rare**, highlighting the importance of handling imbalance.  

---

### 🔹 Feature Importance
![Feature Importance](images/feature_importance.png)

- Features **V17, V14, V12, and V10** contributed most to fraud detection.  
- `Amount` also played a role in distinguishing fraudulent transactions.  

---

## 🛠️ Technologies Used
- **Python** (Pandas, NumPy, Matplotlib, Seaborn, Scikit-learn, Imbalanced-learn)  
- **Machine Learning** (Random Forest, SMOTE)  
- **Visualization** (Matplotlib, Seaborn)  

---

## 🚀 Future Improvements
- Try **XGBoost / LightGBM** for improved recall.  
- Build a **real-time detection system** with Streamlit/Flask.  
- Optimize thresholds to reduce false negatives further.  

---

## 📢 Conclusion
This project demonstrates the application of **Machine Learning for fraud detection**, handling class imbalance, and evaluating performance with appropriate metrics.  

The model achieved:
- **82% recall on fraud cases**  
- **97% ROC-AUC score**  
- Very low false alarms (17 out of 56,864 normal transactions)  

---

👨‍💻 **Author:** Abhishek Singh  
