# Customer-Churn-Prediction
This project focuses on analyzing customer behavior to predict churn (customers leaving a service). It includes:  
Exploratory Data Analysis (EDA) 
Data Cleaning &amp; Preprocessing Feature Engineering Visualizations &amp; 
Insights Goal: Identify patterns and key drivers of churn to help businesses retain customers.

# 📊 Customer Churn Prediction - Data Analysis Project
Predicting customer churn using demographic, transactional, and service interaction data.

**📌 Project Overview**
This project focuses on analyzing customer behavior to predict churn (customers leaving a service). It includes:

Exploratory Data Analysis (EDA)
Data Cleaning & Preprocessing
Feature Engineering
Visualizations & Insights
Goal: Identify patterns and key drivers of churn to help businesses retain customers.
🗂** Dataset Description**
The dataset consists of 4 Excel sheets:

**Customer_Demographics**

Columns: CustomerID, Age, Gender, MaritalStatus, IncomeLevel
Use: Demographic trends in churn.
Transaction_History

Columns: CustomerID, TransactionDate, Amount, ProductCategory
Use: Purchase behavior analysis.
Customer_Service

Columns: CustomerID, InteractionType, ResolutionTime, SatisfactionScore
Use: Service quality impact on churn.
Churn_Status (Target Variable)

Columns: CustomerID, Churn (1 = Churned, 0 = Retained)


**🔍 Exploratory Data Analysis (EDA)**
Key Steps:
Univariate Analysis: Distributions of Age, IncomeLevel, etc.

Python

sns.histplot(data=df, x='Age', hue='Churn', kde=True)
Age Distribution

**Bivariate Analysis:**

Churn rate by IncomeLevel: High-income customers churn less.
Correlation between SatisfactionScore and churn.

Outlier Detection:

Used IQR to cap extreme TransactionAmount values.


🧹 Data Cleaning & Preprocessing
Steps:Handling Missing Values:

Dropped rows with missing SatisfactionScore (5% of data).
Imputed ResolutionTime with median.

**Feature Engineering**:

Created AvgTransactionAmount per customer.
Binned Age into categories (e.g., 18-25, 26-40).
Encoding & Scaling:

**One-hot encoded ProductCategory.**
Scaled numerical features (Age, Amount) using StandardScaler.
📈 Key Insights

**Demographics:**

Customers aged 30-45 have the highest churn rate.
Low-income customers are 2x more likely to churn.

**Behavioral**:

Customers with ≥3 service interactions churn 60% more often.
Unsatisfied customers (score ≤2) churn 75% of the time.

**🛠 Tools Used**
Python Libraries:
Python

pandas, numpy, matplotlib, seaborn, scikit-learn

Jupyter Notebook for analysis.
Git for version control.
📂 Project Structure
Bash
.
├── data/                   # Raw and processed data
│   ├── Customer_Churn_Data_Large.xlsx
│   └── cleaned_data.csv
├── notebooks/              # Analysis code
│   └── churn_analysis.ipynb
├── images/                 # Visualizations
│   └── age_dist.png
├── README.md               # Project documentation
└── requirements.txt        # Dependencies
**🚀 How to Run**

git clone https://github.com/priyadharshanbobby/customer-churn-analysis.git
Install dependencies:
Bash

pip install -r requirements.txt
Open Jupyter Notebook:
Bash
jupyter notebook notebooks/churn_analysis.ipynb
**📝 Future Work**

Build a predictive model (e.g., Random Forest, XGBoost).
Deploy as a Dash/Streamlit dashboard for business teams.

