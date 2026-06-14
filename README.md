[README.md](https://github.com/user-attachments/files/28924757/README.md)
# 🏦 Loan Approval Prediction

A machine learning project that predicts loan approval outcomes using classification algorithms, built on the [Kaggle Loan Prediction dataset](https://www.kaggle.com/ninzaami/loan-predication/home).

---

## 📌 About

Financial institutions process thousands of loan applications every year. Manual evaluation is time-consuming, inconsistent, and prone to bias. This project automates the loan approval decision process by training and benchmarking multiple classification algorithms on applicant demographic and financial data.

The goal is to identify the best-performing classifier that accurately predicts whether a loan application should be approved or rejected — helping lenders make faster, data-driven decisions.

---

## 📂 Dataset

- **Source:** [Kaggle — Loan Prediction Dataset](https://www.kaggle.com/ninzaami/loan-predication/home)
- **Format:** CSV
- **Target Variable:** `Loan_Status` (Y = Approved, N = Rejected)

### Features

| Feature | Description |
|---|---|
| `Gender` | Applicant gender (Male / Female) |
| `Married` | Marital status (Yes / No) |
| `Dependents` | Number of dependents (0 / 1 / 2 / 3+) |
| `Education` | Education level (Graduate / Not Graduate) |
| `Self_Employed` | Self-employment status (Yes / No) |
| `ApplicantIncome` | Applicant's monthly income |
| `CoapplicantIncome` | Co-applicant's monthly income |
| `LoanAmount` | Requested loan amount (in thousands) |
| `Loan_Amount_Term` | Repayment term in months |
| `Credit_History` | Credit history record (1.0 = good, 0.0 = bad) |
| `Property_Area` | Area type (Urban / Semiurban / Rural) |

---

## ⚙️ Methodology

### 1. Data Quality & Missing Value Assessment
Each feature was analysed for missing values. Imputation strategies applied:

| Feature | Imputation Strategy |
|---|---|
| `Gender` | Mode (Male) |
| `Married` | Mode (Yes) |
| `Dependents` | Mode (0) |
| `Self_Employed` | Mode (No) |
| `LoanAmount` | Mean |
| `Loan_Amount_Term` | Mode (360 months) |
| `Credit_History` | Mode (1.0) |

### 2. Feature Engineering
Categorical variables were label-encoded into numerical representations to make them compatible with scikit-learn classifiers.

### 3. Model Training & Evaluation
Five classification algorithms were trained and evaluated using **5-fold cross-validation** to ensure robust, unbiased performance estimates:

- Gradient Boosting Classifier
- Random Forest Classifier
- Decision Tree Classifier
- K-Nearest Neighbors (KNN)
- Support Vector Machine (Linear SVC)

---

## 📊 Results

| Model | Cross-Val Accuracy |
|---|---|
| **Gradient Boosting** | **Highest** ✅ |
| Random Forest | High |
| Decision Tree | Moderate |
| K-Nearest Neighbors | Moderate |
| SVM (Linear) | Moderate |

> **Gradient Boosting Classifier** achieved the highest cross-validated accuracy among all tested models — consistent with findings from prior work on similar classification tasks.

---

## 🛠️ Tech Stack

| Tool | Purpose |
|---|---|
| Python 3 | Core programming language |
| Pandas | Data loading and manipulation |
| NumPy | Numerical operations |
| Matplotlib | Visualisation |
| Seaborn | Statistical plots |
| scikit-learn | Model training and evaluation |

---

## 🚀 Getting Started

### Prerequisites
```bash
pip install pandas numpy matplotlib seaborn scikit-learn
```

### Run the Notebook
```bash
git clone https://github.com/your-username/loan-approval-prediction.git
cd loan-approval-prediction
jupyter notebook loan-approval-prediction.ipynb
```

> Place the dataset CSV file at `input/train_u6lujuX_CVtuZ9i.csv` before running.

---

## 📁 Repository Structure

```
loan-approval-prediction/
│
├── input/
│   └── train_u6lujuX_CVtuZ9i.csv     # Raw dataset
│
├── loan-approval-prediction.ipynb     # Main analysis notebook
├── README.md                          # Project documentation
└── requirements.txt                   # Python dependencies
```

---

## 📚 References

1. J. Heo and J. Y. Yang, "AdaBoost Based Bankruptcy Forecasting of Korean Construction Company," *Applied Soft Computing*, vol. 24, pp. 494–499, 2014.
2. C.-F. Tsai, "Feature Selection in Bankruptcy Prediction," *Knowledge Based Systems*, pp. 120–127, 2009.
3. [Titanic — Logistic Regression with Python (Baligh Mnassri)](https://www.kaggle.com/mnassrib/titanic-logistic-regression-with-python)

---

## 📄 License

This project is open-source and available under the [MIT License](LICENSE).

---

## 🙋 Author

Made with ❤️ for learning and experimentation. Contributions, suggestions, and forks are welcome!
