# 🛡️ Cost-Sensitive Credit Card Fraud Detection

An advanced machine learning project focused on **minimizing financial losses** for banks by prioritizing the detection of fraudulent transactions (High Recall).

## 🚀 Project Overview
In credit card fraud detection, **missing a fraudulent transaction (False Negative) is much more costly** than flagging a legitimate transaction as suspicious (False Positive). 

Standard models often prioritize "Accuracy", which is misleading in highly imbalanced datasets. This project focuses on **Threshold Tuning** and **Robust Preprocessing** to maximize the detection rate of fraudsters.

## 🔑 Key Features & Techniques
Unlike standard implementations on this dataset, this project utilizes:

* **Advanced Preprocessing:** * `Log Transformation` to handle skewed `Amount` data.
    * `RobustScaler` to manage extreme outliers without losing information (critical for fraud detection).
* **Imbalance Handling:** Implemented **SMOTE** (Synthetic Minority Over-sampling Technique) to synthesize minority class samples.
* **Business-Centric Optimization:**
    * Moved beyond default thresholds.
    * Performed **Threshold Tuning** (lowering decision threshold to 0.30) to prioritize Recall.

## 📊 Results & Business Impact

By shifting the decision threshold and using a robust Random Forest classifier, I significantly improved the model's ability to catch fraud.

| Metric | Default Model (Threshold 0.5) | Tuned Model (Threshold 0.3) | Business Impact |
| :--- | :---: | :---: | :--- |
| **Recall** | 0.68 | **0.84** | **16% more fraudsters caught** |
| **Precision** | 1.00 | 0.54 | Accepted trade-off (SMS verification) |
| **F1-Score** | 0.81 | 0.66 | Optimized for Safety |

> **Insight:** The tuned model catches **32 out of 38** fraud cases in the test set, whereas the base model only caught 26. This prevents significant potential financial loss.

## 🛠️ Tech Stack
* **Python** (Pandas, NumPy)
* **Machine Learning:** Scikit-Learn (Random Forest), Imbalanced-Learn (SMOTE)
* **Visualization:** Seaborn, Matplotlib

## 📂 Project Structure
```text
├── data/               # Dataset (not included in repo)
├── notebooks/          # EDA, Preprocessing, and Modeling steps
├── models/             # Saved models
├── images/             # Confusion matrices and plots
└── README.md           # Project documentation
