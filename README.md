# 🏦 Banking Fraud Detection

> **Leakage-Free & Cost-Sensitive Fraud Detection with Temporal Validation**

A DWDM research project focused on building a practical and reproducible machine-learning pipeline for detecting fraudulent banking transactions under severe class imbalance and temporal constraints.

## 🎯 What are we trying to answer?

Instead of simply asking:

> “Which model has the highest accuracy?”

we investigate:

> “How reliable is fraud detection when time, class imbalance, data leakage, and misclassification costs are handled correctly?”

## 🔬 Experiments

We compare three machine-learning models:

* Logistic Regression
* Random Forest
* XGBoost

under different approaches:

```text
Original Data
     │
     ├── Baseline
     ├── SMOTE
     └── Cost-Sensitive Classification
```

## 📊 Evaluation

Accuracy is not the main focus because fraud detection is highly imbalanced.

**Precision • Recall • F1-Score • PR-AUC • Confusion Matrix**

The final evaluation also considers the practical impact of false positives and false negatives.

## ⏱️ Key Idea: Temporal Validation

Transactions are ordered chronologically so that the model learns from past transactions and is evaluated on future transactions.

```text
Past ───────────────────► Future
       TRAIN                  TEST
```

Preprocessing is fitted using training data only, and SMOTE is applied only to the training data to help prevent information leakage.

## 🛠️ Project Workflow

```text
Raw Data
   ↓
Data Understanding
   ↓
Preprocessing
   ↓
EDA & Outlier Analysis
   ↓
Temporal Validation
   ↓
Baseline Models
   ↓
SMOTE Experiment
   ↓
Cost-Sensitive Experiment
   ↓
Model Comparison
   ↓
Final Evaluation
```

## 📁 Repository

```text
banking-fraud-detection/
├── data/
├── notebooks/
├── results/
├── README.md
└── requirements.txt
```

## 📌 Current Results

The final evaluation uses Logistic Regression with SMOTE as the selected candidate based on the model comparison.

Final temporal test performance:

* **Precision:** 0.0216
* **Recall:** 0.4545
* **F1-Score:** 0.0412
* **PR-AUC:** 0.0213

The results also show a high number of false positives, highlighting the difficulty of achieving useful fraud detection performance under severe class imbalance.

## 🎓 Academic Project

Developed as part of the **Data Warehouse and Data Mining (DWDM)** course.

The goal is not to invent another algorithm, but to build a transparent, leakage-free, temporally validated, and reproducible fraud-detection evaluation pipeline.
