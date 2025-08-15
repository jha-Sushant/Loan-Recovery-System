# Loan Recovery System

A machine learning project that analyzes and predicts loan recovery strategies using borrower and loan data.  
The system segments borrowers into risk groups, predicts the likelihood of default, and recommends tailored recovery actions.  
This project is implemented in a Jupyter Notebook using Python and popular data science libraries.

---

## 📌 Project Overview

The core pipeline of this project includes:

1. **Data Exploration & Cleaning**  
   - Initial analysis of the `loan-recovery.csv` dataset.  
   - Checking for missing values and understanding the statistical properties of the data.

2. **Data Visualization**  
   - Visual exploration of relationships between key variables such as:
     - `Payment_History`
     - `Recovery_Status`
     - Loan and borrower attributes

3. **Borrower Segmentation**  
   - **Algorithm:** K-Means Clustering  
   - Groups borrowers into distinct segments based on financial and loan-related features.

4. **Risk Prediction Model**  
   - **Algorithm:** Random Forest Classifier  
   - Predicts the likelihood of a borrower being high-risk.

5. **Strategy Assignment**  
   - A rule-based system recommends a recovery strategy based on predicted risk score:
     - Automated reminders
     - Settlement offers
     - Legal notices

---

## ✨ Key Features

- **Exploratory Data Analysis (EDA):**  
  Comprehensive overview of dataset structure and contents.

- **Visual Insights:**  
  Plots showing how factors like `Monthly_Income`, `Loan_Amount`, and `Num_Missed_Payments` relate to loan recovery outcomes.

- **Unsupervised Learning:**  
  K-Means clustering to identify natural borrower groupings.

- **Supervised Learning:**  
  Random Forest for classification of high-risk borrowers.

- **Actionable Strategies:**  
  Risk scores are translated into tangible recovery actions.

---

## 📂 Dataset

The project uses a single CSV file: **`loan-recovery.csv`**

### **Key Columns:**
- **Borrower_ID:** Unique borrower identifier  
- **Age, Gender, Employment_Type:** Borrower demographics  
- **Monthly_Income:** Income level of borrower  
- **Loan_Amount, Loan_Tenure, Interest_Rate:** Loan details  
- **Payment_History, Num_Missed_Payments, Days_Past_Due:** Payment metrics  
- **Recovery_Status:** Loan outcome (`Fully Recovered`, `Partially Recovered`, `Written Off`)  
- **Collection_Method, Collection_Attempts, Legal_Action_Taken:** Recovery actions taken  

---

## 📊 Borrower Segments Identified

1. **High Income, Low Default Risk**  
   High income, manageable loan — low default risk.

2. **High Loan, Higher Default Risk**  
   Very large loan amounts — higher chance of default.

3. **Moderate Income, High Loan Burden**  
   Moderate income with high loan-to-income ratio — likely payment stress.

4. **Moderate Income, Medium Risk**  
   Balanced loan-to-income ratio — moderate risk level.

---

## 🧠 Machine Learning Models

- **Borrower Segmentation:** K-Means Clustering
- **Risk Prediction:** Random Forest Classifier
- **Strategy Mapping:** Rule-based thresholds  
  - Risk > 0.75 → Immediate legal notices & aggressive recovery attempts  
  - 0.50 ≤ Risk ≤ 0.75 → Settlement offers & repayment plans  
  - Risk < 0.50 → Automated reminders & monitoring  

---

## 📌 Conclusion

This project demonstrates how machine learning can:
- Identify meaningful borrower segments
- Predict high-risk borrowers
- Recommend optimal recovery strategies

The approach can help financial institutions:
- Improve collection efficiency
- Reduce write-offs
- Optimize recovery resource allocation

---

## 🚀 Future Improvements

- Integrate real-time risk scoring API
- Use scalable frameworks (Dask, PySpark) for large datasets
- Implement explainable AI (SHAP) for risk interpretation
- Automate retraining with recent borrower data

---

## 🛠 Tech Stack

- **Languages:** Python  
- **Libraries:** Pandas, NumPy, Matplotlib, Seaborn, scikit-learn  
- **Environment:** Jupyter Notebook

---
