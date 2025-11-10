# 🧮 Credit Risk Analysis using K-Means Clustering

This project applies **K-Means Clustering** to segment loan applicants into distinct groups based on their financial profiles, revealing different levels of **credit risk**.

---

## 🎯 Project Goal
Can we identify distinct clusters of borrowers that represent different levels of credit risk (e.g., low, medium, and high)?

---

## 🧠 Analysis Pipeline

The full analysis is implemented in [`credit_risk.ipynb`](./credit_risk.ipynb).

### 1. Data Cleaning
- Loaded the `credit_risk_dataset.csv` dataset.
- Handled outliers and dropped rows with missing values.

### 2. Exploratory Data Analysis (EDA)
- Examined distributions of numeric and categorical features.
- Investigated correlations between key variables.
- Analyzed default status versus income and debt ratios.

### 3. Preprocessing
- Applied **One-Hot Encoding** to categorical features.
- Scaled numeric features using **StandardScaler**.

### 4. Model Selection
- Used the **Elbow Method** to determine the optimal number of clusters (`k = 3`).

### 5. Clustering
- Trained a **K-Means model** with `k = 3`.
- Visualized clusters in 2D space using **PCA** for interpretability.

---

## 📊 Cluster Analysis & Results

| Cluster | Name | Key Traits | Risk Level |
|----------|------|-------------|-------------|
| **0** | 🟢 *Cautious Borrowers* | Low loan amounts, low debt-to-income ratios | Low |
| **1** | 🔵 *Established Borrowers* | Older, higher income, long credit histories | Low |
| **2** | 🔴 *Over-Leveraged Borrowers* | High loan-to-income ratios, frequent defaults | High |

**Visualization:** PCA plot highlights clear separation between low- and high-risk borrower segments.

---

## ⚖️ Ethical Considerations

> Machine learning in credit decisions must be deployed responsibly.

- **Bias Amplification:** Income or demographic correlations may reinforce historical inequalities.  
- **Negative Feedback Loops:** Younger or new borrowers could be unfairly penalized for thin credit histories.  
- **Lack of Explainability:** Clustering decisions are difficult to interpret, limiting borrowers’ ability to improve their credit profiles.

---

## 🧰 Tech Stack

- **Python** (Pandas, NumPy, scikit-learn, Matplotlib, Seaborn)
- **Machine Learning:** K-Means Clustering, PCA  
- **Data Preprocessing:** One-Hot Encoding, StandardScaler  
- **Visualization:** Pairplots, Elbow Method, PCA Projection  

---

