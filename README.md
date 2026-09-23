# 🏦 Banking Fraud Detection

> **Leakage-Free & Cost-Sensitive Fraud Detection with Temporal Validation**

A DWDM research project focused on building a practical machine-learning pipeline for detecting fraudulent banking transactions under **class imbalance, temporal constraints, and different misclassification costs**.

## 🎯 What are we trying to answer?

Instead of simply asking:

> *“Which model has the highest accuracy?”*

we investigate:

> **“How reliable is fraud detection when we handle time, imbalance, leakage, and financial cost correctly?”**

## 🔬 Planned Experiments

We will compare three models:

- Logistic Regression
- Random Forest
- XGBoost

under three settings:

```text
Original Data
     │
     ├── Baseline
     ├── SMOTE
     └── Cost-Sensitive Learning
```

## 📊 Evaluation

Accuracy will not be our main focus because fraud is a highly imbalanced problem.

**Precision • Recall • F1-Score • PR-AUC • Confusion Matrix • Expected Financial Loss**

## ⏱️ Key Idea: Temporal Validation

Transactions are ordered by time so that the model learns from **past transactions** and is evaluated on **future transactions**.

```text
Past ────────────────► Future
  TRAIN                 TEST
```

Learned preprocessing and SMOTE will be applied only to the training data to help prevent information leakage.

## 🛠️ Project Workflow

```text
Raw Data
   ↓
Understand
   ↓
Clean & Preprocess
   ↓
EDA & Outlier Analysis
   ↓
Temporal Validation
   ↓
Baseline Models
   ↓
SMOTE
   ↓
Cost-Sensitive Learning
   ↓
Financial Loss Analysis
   ↓
Final Comparison
   ↓
Streamlit Dashboard
```

## 📁 Repository

```text
banking-fraud-detection/
├── data/
├── notebooks/
├── results/
├── app/
├── README.md
└── requirements.txt
```

## 🚧 Status

**Currently:** Dataset understanding & initial data-quality analysis.

Upcoming: preprocessing → EDA → temporal split → baseline models → SMOTE → cost-sensitive experiments → Streamlit.

## 🎓 Academic Project

Developed as part of the **Data Warehouse and Data Mining (DWDM)** course.

The goal is not to invent another algorithm, but to build a **transparent, reproducible, and practically meaningful fraud-detection evaluation pipeline**.
