# 🛡️ Fraud Detection Case Study - Internship Round 3

This project was completed as part of **Round 3** of a Data Science Internship recruitment process. The task was to build a fraud detection model using a real-world transactional dataset. The focus was on data cleaning, feature selection, model building, evaluation, and interpreting fraud signals.

---

## 📁 Dataset Overview

- **Rows:** 6,362,620  
- **Columns:** 10  
- **Target Variable:** `isFraud` (Binary – 0: Genuine, 1: Fraudulent)

The dataset contains over 6 million financial transactions including fields such as:

- `step`: Time step in hours
- `type`: Transaction type (e.g., CASH_OUT, TRANSFER)
- `amount`: Transaction amount
- `nameOrig` and `nameDest`: Origin and destination customer IDs
- `oldbalanceOrg`, `newbalanceOrig`, `oldbalanceDest`, `newbalanceDest`: Account balances before and after transaction
- `isFraud`: Target variable indicating if the transaction was fraudulent

Due to the large size, sampling or optimized operations (e.g. chunk processing) were used to ensure efficient computation.


---

## 🔧 Tasks Performed

1. **Data Cleaning**
   - Handled missing values
   - Treated outliers using IQR method
   - Checked for multicollinearity using VIF

2. **Exploratory Data Analysis (EDA)**
   - Visualized class imbalance
   - Compared feature distributions for fraud vs non-fraud
   - Correlation heatmaps and boxplots

3. **Feature Selection**
   - Removed highly correlated or unimportant features
   - Selected features based on domain relevance and data insights

4. **Model Building**
   - Used `RandomForestClassifier` from `sklearn`
   - Trained model on 80/20 split (with stratification)
   - Addressed class imbalance using SMOTE

5. **Model Evaluation**
   - Classification report with precision, recall, f1-score
   - Confusion matrix
   - Achieved high precision on fraud class (minority)

6. **Fraud Indicator Analysis**
   - Identified key fraud predictors: transaction type, amount, and account balance patterns

---

## 📈 Results

- **Accuracy**: ~100% (due to class imbalance)
- **Recall on fraud cases**: ~76%
- **Precision on fraud cases**: ~100%
- Model correctly identifies most frauds while avoiding false alarms

---

## 🔍 Key Insights

- Most frauds occur in `TRANSFER` and `CASH_OUT` transaction types
- Fraudulent transactions tend to have unusually high amounts and balance differences
- SMOTE helped to improve model sensitivity on minority class

---

## 🛡️ Suggestions for Prevention

- Implement real-time anomaly detection for suspicious transaction types
- Set threshold alerts on large amount or unusual balance changes
- Strengthen identity verification steps for `TRANSFER` and `CASH_OUT`

---

## ✅ Next Steps

- Deploy the model using a cloud service (e.g., Streamlit + GCP/AWS)
- Monitor model performance post-deployment
- Retrain regularly as fraud patterns evolve

---

## 📎 File Info

- `fraud_detection_case_study.ipynb` – Jupyter notebook with code, visualizations, and model

---

## 🔗 How to View

👉 [Click here to open the notebook](paste-your-notebook-link-here)  
(Replace with your actual GitHub file URL)

---

## 👨‍💻 Author

**Mirsha Kudukkan**  
_Data Science Intern | Self-taught learner_  
[LinkedIn](https://www.linkedin.com/in/mirshakudukkan) | [GitHub](https://github.com/mirshak)

