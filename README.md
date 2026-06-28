# 📉 Customer Churn Prediction

> Predicting which telecom customers are likely to leave — using Machine Learning to help businesses retain their customers.

[![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)](https://python.org)
[![Scikit-learn](https://img.shields.io/badge/scikit--learn-F7931E?style=for-the-badge&logo=scikit-learn&logoColor=white)](https://scikit-learn.org)
[![Pandas](https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white)](https://pandas.pydata.org)
[![Jupyter](https://img.shields.io/badge/Jupyter-F37626?style=for-the-badge&logo=jupyter&logoColor=white)](https://jupyter.org)
[![Kaggle](https://img.shields.io/badge/Kaggle-20BEFF?style=for-the-badge&logo=kaggle&logoColor=white)](https://www.kaggle.com/datasets/blastchar/telco-customer-churn)

---

## 📌 Project Overview

Customer churn is one of the biggest problems in the telecom industry. In this project, I built an end-to-end machine learning pipeline to predict whether a customer will churn (leave) or stay — using real-world data from **7,043 Telco customers**.

The goal: give businesses an early warning system so they can take action before losing a customer.

---

## 📊 Dataset

| Detail | Value |
|--------|-------|
| **Source** | [Telco Customer Churn — Kaggle](https://www.kaggle.com/datasets/blastchar/telco-customer-churn) |
| **Total Customers** | 7,043 |
| **Total Features** | 21 |
| **Churn Rate** | 26.5% (1,869 churned) |
| **Stayed** | 73.5% (5,174 stayed) |

### Key Features Used
- `tenure` — How long the customer has been with the company
- `MonthlyCharges` — Monthly bill amount
- `TotalCharges` — Total amount paid
- `Contract` — Month-to-month, One year, Two year
- `InternetService`, `OnlineSecurity`, `TechSupport`
- `PaymentMethod`, `SeniorCitizen`, `Partner`, `Dependents`

---

## 🛠️ Tech Stack

| Tool | Purpose |
|------|---------|
| Python 3 | Core language |
| Pandas & NumPy | Data loading and cleaning |
| Matplotlib & Seaborn | Data visualization |
| Scikit-learn | ML models and evaluation |
| Jupyter Notebook | Development environment |
| Kaggle API | Dataset download |

---

## 🔄 Project Pipeline

```
📥 Data Download (Kaggle API)
    ↓
🔍 Exploratory Data Analysis (EDA)
    ↓
🧹 Data Cleaning & Preprocessing
    ↓
📊 Feature Engineering & Encoding
    ↓
✂️ Train / Test Split (80/20)
    ↓
🤖 Model Training (Logistic Regression + Random Forest)
    ↓
📈 Evaluation (Accuracy, F1, ROC-AUC)
    ↓
📊 Visualization (Confusion Matrix, ROC Curve, Feature Importance)
```

---

## 📈 EDA — Key Insights

### Churn Overview
- **26.5%** of customers churned — a significant business problem
- Customers on **month-to-month contracts** churn the most
- **Senior citizens** have a higher churn rate than non-seniors

### Top Features Correlated with Churn

| Feature | Correlation |
|---------|-------------|
| Contract Type | 0.397 ███████████ |
| Tenure | 0.352 ██████████ |
| Online Security | 0.289 ████████ |
| Tech Support | 0.282 ████████ |
| Total Charges | 0.199 █████ |
| Monthly Charges | 0.193 █████ |

> **Insight:** Customers with longer tenure and annual/bi-annual contracts are far less likely to churn. Offering security & support services also reduces churn.

---

## 🤖 Models Trained

### Model 1 — Logistic Regression
- Simple, fast, and interpretable baseline model
- Scaled features using StandardScaler

### Model 2 — Random Forest Classifier
- Ensemble model with 100 decision trees
- Max depth: 10, Random state: 42

---

## 🏆 Results

| Metric | Logistic Regression | Random Forest |
|--------|--------------------:|-------------:|
| **Accuracy** | **79.9%** | 79.6% |
| **F1 Score** | **0.5916** | 0.5710 |
| **ROC-AUC** | **0.8403** | 0.8357 |

> **Winner: Logistic Regression** — slightly better F1 and ROC-AUC scores, and much faster to train.

### Classification Report (Logistic Regression)

| Class | Precision | Recall | F1-Score |
|-------|-----------|--------|----------|
| Stayed | 0.84 | 0.89 | 0.87 |
| Churned | — | — | 0.59 |

### Train/Test Split
- Training samples: **5,634**
- Testing samples: **1,409**
- Features used: **19**

---

## 📁 Project Structure

```
Customer-Churn-Prediction/
│
├── Customer_Churn_Prediction.ipynb   # Main notebook (full pipeline)
├── WA_Fn-UseC_-Telco-Customer-Churn.csv  # Dataset (auto-downloaded via Kaggle API)
│
├── plots/
│   ├── plot_churn_overview.png       # Churn distribution charts
│   ├── plot_tenure_charges.png       # Tenure & charges analysis
│   ├── plot_segments.png             # Senior citizen & payment analysis
│   └── plot_confusion_roc.png        # Confusion matrix + ROC curves
│
└── README.md
```

---

## 🚀 How to Run

### Option 1 — Google Colab (Recommended)
1. Open the notebook in Google Colab
2. Add your Kaggle API credentials (username + key) in Cell 2
3. Run all cells (`Runtime → Run All`)

### Option 2 — Local
```bash
# Clone the repo
git clone https://github.com/dawoodahmadbakhsh21-web/Customer-Churn-Prediction-Project.git
cd Customer-Churn-Prediction-Project

# Install dependencies
pip install pandas numpy matplotlib seaborn scikit-learn

# Open Jupyter
jupyter notebook Customer_Churn_Prediction.ipynb
```

> **Note:** You need a Kaggle account for the dataset. Get your API key from [kaggle.com/account](https://kaggle.com/account).

---

## 💡 Business Takeaways

1. **Prioritize long-term contracts** — Month-to-month customers churn 3x more
2. **Bundle security & support services** — Strong negative correlation with churn
3. **Focus on new customers** — Low tenure = high churn risk; early engagement matters
4. **Senior citizen outreach** — Higher churn rate suggests a need for targeted plans

---

## 👨‍💻 Author

**Dawood Ahmad**
- GitHub: [@dawoodahmadbakhsh21-web](https://github.com/dawoodahmadbakhsh21-web)
- LinkedIn: [dawood-ahmad-b46641361](https://linkedin.com/in/dawood-ahmad-b46641361)
- Email: dawoodahmadbakhsh21@gmail.com

---

## 🔗 Related Projects

| Project | Description |
|---------|-------------|
| [House Price Prediction](https://github.com/dawoodahmadbakhsh21-web/house-price-prediction) | Random Forest regression model |
| [Movie Recommendation System](https://github.com/dawoodahmadbakhsh21-web/Movie-Recommendation-System) | TF-IDF & Cosine Similarity |
| [Email Spam Detection](https://github.com/dawoodahmadbakhsh21-web/Email-spam-detection) | NLP-based classification |
| [Journyify](https://github.com/dawoodahmadbakhsh21-web/journal-spark-108) | AI Journaling SaaS App |

---

⭐ **If this project helped you, consider giving it a star!**
