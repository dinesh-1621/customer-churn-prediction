## 🔄 Customer Churn Prediction

> An end-to-end Machine Learning project to predict which customers are likely to cancel their subscription — helping businesses take action before losing them.

---

## 📊 Project Overview

Customer churn is one of the biggest challenges for subscription-based businesses. This project builds a complete ML pipeline that:
- Identifies customers at risk of churning
- Segments them into High / Medium / Low risk groups
- Quantifies the revenue at risk
- Visualizes actionable insights through a Power BI dashboard

---

## 📁 Dataset

| Property      | Detail                                |
|---------------|---------------------------------------|
| Source        | Kaggle — Customer Churn Dataset       |
| Total Rows    | 64,374 customers                      |
| Total Columns | 12 features                           |
| Target Column | 'Churn' (0 = Stayed, 1 = Churned)     |
| Churn Rate    | ~47.4% (balanced — no SMOTE required) |

**Features include:** Age, Gender, Tenure, Usage Frequency, Support Calls, Payment Delay, Subscription Type, Contract Length, Total Spend, Last Interaction

---

## 🔧 Project Workflow

| Step | Description                                                                                                           |
|------|-----------------------------------------------------------------------------------------------------------------------|
|  1   | **Setup & Load Data** — Import libraries, load CSV, explore with df.head(), df.info(), df.describe()                  |
|  2   | **Exploratory Data Analysis** — Churn rate, histograms, box plots, correlation heatmap, feature correlation bar chart |
|  3   | **Data Cleaning** — Check missing values, remove duplicates, drop CustomerID                                          |
|  4   | **Feature Engineering** — Ordinal encoding for categorical columns (Gender, Subscription Type, Contract Length)       |
|  5   | **Model Building** — Train/test split (80/20), RobustScaler, Logistic Regression, Decision Tree with GridSearchCV     |
|  6   | **Model Evaluation** — Classification report, Confusion matrix, ROC-AUC curves                                        |
|  7   | **Export & Power BI Dashboard** — Export predictions CSV, build interactive business dashboard                        |
|  8   | **GitHub & Documentation** — Clean repo, README, LinkedIn post                                                        |

---

## 🤖 Models Used

## Logistic Regression (Baseline)
| Metric    |Score  |
|-----------|-------|
| Accuracy  | 83%   |
| AUC Score | 0.90  |

### Decision Tree with GridSearchCV (Final Model) ✅
| Metric                 | Score      |
|------------------------|------------|
| Accuracy               | **95.60%** |
| AUC Score              | **0.994**  |
| Best Max Depth         |      5     |
| Best Min Samples Split |     10     |
| Best Min Samples Leaf  |      5     |

> Decision Tree was selected as the final model due to significantly higher accuracy and AUC score compared to Logistic Regression.

---

## 📈 Key Business Insights (from Power BI Dashboard)

- **50.09% churn rate** among evaluated customers
- **6,450 customers** predicted to churn
- **₹3.44M revenue at risk** from churning customers
- Customers with **5+ support calls** have 64%+ churn rate vs 25% for those with 0 calls
- Churn rate **jumps sharply after 30 months** of tenure — long-term customers are leaving more
- Churn is **almost equal across subscription types** — plan type alone is not a driver

---

## 🛠️ Tools & Technologies

![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=flat&logo=pandas&logoColor=white)
![Scikit-learn](https://img.shields.io/badge/Scikit--learn-F7931E?style=flat&logo=scikit-learn&logoColor=white)
![Power BI](https://img.shields.io/badge/Power%20BI-F2C811?style=flat&logo=powerbi&logoColor=black)
![Matplotlib](https://img.shields.io/badge/Matplotlib-11557C?style=flat)
![Seaborn](https://img.shields.io/badge/Seaborn-4C72B0?style=flat)

---

## 📂 Repository Structure

'''
customer-churn-prediction/
│
├── Customer_Churn_Prediction.ipynb   # Main notebook (full pipeline)
├── churn_predictions.csv             # Exported predictions (test set)
├── Churn_Dashboard.pdf               # Power BI dashboard export
└── README.md                         # Project documentation
'''

---

## ▶️ How to Run

1. Clone this repository
'''bash
git clone https://github.com/yourusername/customer-churn-prediction.git
'''

2. Install required libraries
'''bash
pip install pandas numpy matplotlib seaborn scikit-learn
'''

3. Open the notebook
'''bash
jupyter notebook Customer_Churn_Prediction.ipynb
'''

4. Run all cells from top to bottom

> **Note:** Dataset file must be in the same directory or update the file path in Step 1 of the notebook.

---

## 💡 What I Learned

- How to follow a complete end-to-end ML workflow
- Importance of scaling **after** train/test split to prevent data leakage
- Using 'stratify=y' in train/test split for balanced class representation
- Hyperparameter tuning with GridSearchCV
- Translating ML predictions into business insights using Power BI

---

## 👤 Author

**RIKKA DINESH REDDY**
- LinkedIn: www.linkedin.com/in/dineshreddyrikka
- GitHub: [your-github-url]
