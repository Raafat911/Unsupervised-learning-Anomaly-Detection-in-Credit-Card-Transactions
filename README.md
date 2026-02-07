# Unsupervised Fraud Detection (Isolation Forest & LOF)

This project explores **unsupervised anomaly detection** for credit card fraud detection, with a focus on **alerting efficiency** rather than supervised classification.

## Dataset
The dataset used is the **Credit Card Fraud Detection** dataset from Kaggle:

Credit Card Fraud Detection – Kaggle  
https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud

- 284,807 transactions  
- Highly imbalanced (fraud ≈ 0.17%)  
- PCA-transformed features (`V1`–`V28`) + `Amount`  
- Labels (`Class`) are **used only for evaluation**, not training

## Models Used

### 1. Isolation Forest
- Treated anomaly detection as a **ranking / alerting problem**
- Achieved strong recall at a low alert rate
- Scalable and transferable to new data
- Best-performing model in this study

### 2. Local Outlier Factor (LOF)
- Evaluated as a **local density–based** anomaly detector
- Computationally expensive on the full dataset
- Performed poorly in detecting fraud compared to Isolation Forest
- Demonstrates the importance of matching model assumptions to data structure

## Key Takeaway
Isolation Forest provided the best balance between **fraud detection performance and scalability**, while LOF highlighted limitations of local density methods for this dataset.

## Notes
- No supervised classifiers were used
- No deep learning models were included
- Time-based feature experiments were evaluated only within the Isolation Forest framework
