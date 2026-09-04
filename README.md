# Loan Approval Prediction

## Overview
This project is a Machine Learning classification model designed to predict whether a loan application should be approved or rejected. By analyzing an applicant's demographic and financial background, this model automates the decision-making process to minimize financial risk and improve operational efficiency.

## Dataset
The dataset (`loan_data.csv`) contains 45,000 records and 14 features, including:
* **Applicant Demographics:** Age, Gender, Education Level, Home Ownership status.
* **Financial Metrics:** Annual Income, Employment Experience.
* **Loan Details:** Loan Amount, Intent, Interest Rate, Loan Percent of Income.
* **Credit History:** Credit Score, Credit History Length, Previous Loan Defaults.
* **Target Variable:** `loan_status` (1 = Approved, 0 = Rejected).

## Technologies Used
* **Language:** Python
* **Environment:** Jupyter Notebook
* **Libraries:** Pandas, NumPy, Scikit-Learn, Matplotlib, Seaborn

## Project Workflow
1. **Data Preprocessing:** Handled missing numerical values using the median to avoid outlier bias, and filled categorical missing values with the mode.
2. **Feature Encoding:** Converted categorical text data into numerical formats using One-Hot Encoding (`pd.get_dummies`).
3. **Feature Scaling:** Applied `StandardScaler` to ensure large numerical values (like Income) do not disproportionately bias the model over smaller percentages (like Interest Rate).
4. **Model Training:** Split the data (80% training, 20% testing) and trained a **Random Forest Classifier**.

## Key Results
The model performed exceptionally well on the unseen test data:
* **Accuracy:** 92.87%
* **ROC AUC Score:** 97.46%

**Top 3 Drivers for Loan Approval:**
Based on the feature importance analysis, the model relies most heavily on:
1. **Previous Loan Defaults** (Highest impact on rejection)
2. **Loan Percent of Income**
3. **Loan Interest Rate**

## How to Run
1. Clone this repository.
2. Ensure `loan_data.csv` is in the same directory as the Jupyter Notebook.
3. Run all cells in the Jupyter Notebook to view the preprocessing steps, model evaluation metrics, and visualizations.
