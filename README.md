# Project-4-Credit-Risk
Credit Risk Analysis using K-Means Clustering

This project uses K-Means Clustering to segment loan applicants into distinct groups based on their financial profiles, which are then interpreted as different credit risk levels.

Project Goal

Can we identify distinct clusters of borrowers that represent different levels of credit risk (such as low, medium, and high)?

Analysis Pipeline

The analysis is performed in the credit_risk.ipynb notebook:

Data Cleaning: Loaded the credit_risk_dataset.csv, handled outliers, and dropped rows with missing values.

EDA: Analyzed numeric and categorical feature distributions, correlations, and default status vs. income.

Preprocessing: One-hot encoded categorical features and scaled all numeric features using StandardScaler.

Model Selection: Used the Elbow Method to determine that $k=3$ is the optimal number of clusters.

Clustering: Trained a K-Means model with $k=3$ and visualized the results using PCA.

Cluster Analysis & Results

The three clusters were interpreted as distinct borrower personas:

Cluster 0: The Cautious Borrowers (Low Risk)

Key Traits: Below-average loan amounts and very low debt-to-income ratios.

Narrative: Risk-averse borrowers taking small, manageable loans.

Cluster 1: The Established Borrowers (Low Risk)

Key Traits: Significantly older, with higher incomes and long credit histories.

Narrative: Financially stable individuals with established careers.

Cluster 2: The Over-Leveraged Borrowers (High Risk)

Key Traits: High loan amounts, high loan-to-income ratios, and the highest frequency of historical defaults.

Narrative: The riskiest segment, taking on more debt than their income comfortably supports.

Ethical Considerations

Deploying this model without oversight carries risks:

Bias Amplification: The model could inadvertently scale up historical discrimination if features like income correlate with protected demographics.

Negative Feedback Loops: The model may unfairly penalize younger, "cautious" borrowers (Cluster 0) for having thin credit files, preventing them from building credit.

Lack of Explainability: It can be difficult to explain a cluster-based loan denial to a borrower, making it hard for them to know how to improve.

