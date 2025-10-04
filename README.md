# Telco Customer Churn Prediction: An End-to-End Data Science Pipeline  

## Project Overview  
This project demonstrates a full, professional data science workflow applied to a critical business problem: **predicting customer churn** for a telecommunications company.  

The objective was to leverage historical customer data to build a robust machine learning model capable of identifying customers at high risk of leaving. This predictive capability allows the retention team to execute targeted, cost-effective interventions.  

---

## Key Results and Business Insights  
The final model, an **XGBoost Classifier**, achieved strong performance metrics (e.g., an estimated **0.84 AUC**) with a focus on maximizing **Recall** for the churn class—meaning it is highly effective at catching actual churners.  

The model uncovered the top drivers of churn, providing clear actions for the business:  

- **Contract Type**: The Month-to-month contract is the single greatest risk factor.  
- **Tenure**: Customers in the 0–1 year tenure group are highly unstable.  
- **Service Type**: Customers with Fiber optic internet service have a disproportionately high churn rate, suggesting potential service quality or cost issues.  

For a detailed breakdown of the model performance, feature importance, and actionable steps, please read the **Executive Summary**.  

---

## Project Pipeline (The 5 Stages)  

This repository contains the complete code for each stage of the data science lifecycle:  

| File                     | Stage                    | Description |
|---------------------------|--------------------------|-------------|
| `data_cleaning.py`        | 1. Data Cleaning         | Loaded data, converted `TotalCharges` to numeric, handled missing values, and encoded the target variable. |
| `eda_analysis.py`         | 2. EDA                   | Analyzed distributions of numerical and categorical data, and uncovered initial patterns and correlations driving churn. |
| `feature_engineering.py`  | 3. Feature Engineering   | Applied One-Hot Encoding, Standard Scaling, binned tenure into commitment groups, and performed the Train/Test split. |
| `modeling_evaluation.py`  | 4. Modeling & Evaluation | Trained and benchmarked Logistic Regression, Random Forest, and XGBoost models. Selected XGBoost for production use. |
| `communication_report.py` | 5. Communication         | Generated feature importance plots (SHAP/Feature Imp.) and interpreted the model's top drivers. |
| `executive_summary.md`    | Final Deliverable        | A concise, non-technical report for stakeholders, detailing findings and recommendations. |

---

## Setup and Installation  

### Data Source  
The dataset used is the publicly available **IBM Telco Customer Churn dataset**.  
It is generally included in the project files, but if not, it can be sourced from Kaggle or other public repositories.  
The expected filename is: WA_Fn-UseC_-Telco-Customer-Churn.csv


###Running the Project
The project is built using **Python 3** and the following dependencies.

**1. Clone the repository:**  

    git clone https://github.com/abhisargupta85/telco-churn-prediction.git
    cd telco-churn-prediction

**2. Install dependencies:**

Use the requirements.txt file to install all necessary libraries:

    pip install -r requirements.txt

**3. Execute the Pipeline:**
Run the Python files sequentially to regenerate the analysis, models, and results:

    python data_cleaning.py
    python eda_analysis.py
    python feature_engineering.py
    python modeling_evaluation.py
    python communication_report.py
