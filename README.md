# MIT516 — Data Analytics for Cyber Security
## Assessment D: Phishing & Spam Email Detection
Sharof Moktan
S2501034

---

## Project Overview
This project applies machine learning and anomaly detection techniques to detect phishing and spam emails using the UCI Spambase dataset. The analysis follows a full data analytics pipeline including preprocessing, exploratory data analysis, anomaly detection, classification, and evaluation.

---

## Dataset
- **Name:** UCI Spambase Dataset
- **Source:** [UCI Machine Learning Repository](https://archive.ics.uci.edu/ml/datasets/spambase)
- **Size:** 4,601 emails | 57 features | 1 label
- **Label:** 1 = Spam, 0 = Not Spam
- **Features:** Word frequencies, character frequencies, capital run-length statistics

---

## Project Structure
```
├── MIT516_D_Notebook.ipynb   # Main Jupyter notebook
├── spambase.data             # Dataset file
└── README.md                 # This file
```

---

## Pipeline Steps
1. **Data Loading & Inspection** — Load dataset, check for missing values and class distribution
2. **Data Preprocessing** — StandardScaler normalisation, train/test split, SMOTE oversampling
3. **Exploratory Data Analysis** — Class distribution, feature distributions, correlation heatmap
4. **Anomaly Detection** — Isolation Forest to flag suspicious emails
5. **Machine Learning Classifiers** — Random Forest, Decision Tree, Naive Bayes, Logistic Regression
6. **Model Evaluation** — Confusion matrices, ROC curves, classification reports
7. **Security Visualisation Dashboard** — 9-panel analytics dashboard

---

## Libraries Used
- `pandas` — data manipulation
- `numpy` — numerical computing
- `matplotlib` & `seaborn` — data visualisation
- `scikit-learn` — machine learning models and evaluation
- `imbalanced-learn` — SMOTE for class balancing
- `scipy` — statistical functions

---

## How to Run
1. Clone this repository or download all files
2. Make sure `spambase.data` is in the same folder as the notebook
3. Open `MIT516_D_Notebook.ipynb` in Jupyter Notebook, JupyterLab, or Google Colab
4. Run all cells: **Kernel → Restart & Run All** (Jupyter) or **Runtime → Run All** (Colab)

---

## Results Summary
| Classifier | Accuracy | F1 (Spam) | AUC-ROC |
|---|---|---|---|
| Random Forest | ~0.97 | ~0.96 | ~0.99 |
| Logistic Regression | ~0.93 | ~0.91 | ~0.97 |
| Decision Tree | ~0.92 | ~0.91 | ~0.93 |
| Naive Bayes | ~0.82 | ~0.79 | ~0.90 |

**Key Findings:**
- Capital run-length features are the strongest spam predictors
- Dollar sign (`$`) and exclamation (`!`) character frequencies are highly discriminative
- Random Forest achieves near-perfect AUC-ROC with SMOTE balancing
- Isolation Forest successfully flags anomalous emails with strong spam overlap

---

## Author
MIT516 — Data Analytics for Cyber Security  
Assessment D Submission
