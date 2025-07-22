# Improved Detection of Fraud Cases for E-commerce and Bank Transactions

## Project Overview

This project aims to develop accurate fraud detection models for both e-commerce and bank credit transactions using advanced machine learning techniques. The project addresses the unique challenges of highly imbalanced datasets and incorporates geolocation analysis and transaction pattern recognition.

## Business Context

As a data scientist at Adey Innovations Inc., this project focuses on creating robust fraud detection systems that balance security with user experience, minimizing both false positives and false negatives.

## Datasets

- **Fraud_Data.csv**: E-commerce transaction data with user demographics, device info, and transaction details
- **creditcard.csv**: Bank transaction data with anonymized features from PCA transformation
- **IpAddress_to_Country.csv**: Mapping of IP address ranges to countries for geolocation analysis

## Project Structure

```
├── data/                          # Raw datasets
├── notebooks/                     # Jupyter notebooks for analysis
├── src/                          # Source code modules
├── reports/                      # Analysis reports and visualizations
├── models/                       # Trained model artifacts
├── requirements.txt              # Python dependencies
└── README.md                     # Project documentation
```

## Setup Instructions

1. Clone the repository
2. Create a virtual environment: `python -m venv .venv`
3. Activate the environment: `.venv\Scripts\activate` (Windows)
4. Install dependencies: `pip install -r requirements.txt`
5. Run the analysis: `jupyter notebook notebooks/fraud_detection_analysis.ipynb`

## Current Progress (Interim 1 - Task 1 Completed)

### Data Analysis and Preprocessing ✅

- **Data Loading**: Successfully loaded all three datasets
- **Missing Value Analysis**: Identified and handled missing values in both datasets
- **Data Cleaning**: Removed duplicates and corrected data types
- **Exploratory Data Analysis**: Comprehensive univariate and bivariate analysis
- **Geolocation Integration**: Merged IP address data with country mapping
- **Feature Engineering**: Created time-based features and transaction patterns
- **Class Imbalance Analysis**: Analyzed severe class imbalance (both datasets <1% fraud)

### Key Findings from EDA

1. **Severe Class Imbalance**:
   - Fraud_Data: ~6% fraudulent transactions
   - creditcard: ~0.17% fraudulent transactions
2. **Geographic Patterns**: Certain countries show higher fraud rates
3. **Temporal Patterns**: Fraud peaks during specific hours and days
4. **Device/Browser Patterns**: Specific combinations associated with higher fraud risk

### Feature Engineering Completed

- `time_since_signup`: Duration between signup and purchase
- `hour_of_day`: Extracted from purchase timestamp
- `day_of_week`: Day of week pattern analysis
- `transaction_frequency`: User transaction patterns
- Country mapping from IP addresses
- Categorical encoding for browsers, sources, gender

### Data Preprocessing Strategy

- **Sampling Strategy**: SMOTE for handling class imbalance (applied to training only)
- **Scaling**: StandardScaler for numerical features
- **Encoding**: One-hot encoding for categorical variables
- **Train-Test Split**: 80-20 split with stratification

## Next Steps (Tasks 2-3)

- [ ] Model Building: Logistic Regression + Ensemble Model (XGBoost/LightGBM)
- [ ] Model Evaluation: Focus on AUC-PR, F1-Score, Precision-Recall
- [ ] SHAP Analysis: Model explainability and feature importance
- [ ] Final Report: Model comparison and business recommendations

## Key Challenges Addressed

1. **Class Imbalance**: Using appropriate metrics (AUC-PR, F1) and SMOTE sampling
2. **Feature Engineering**: Creating meaningful time and behavioral features
3. **Geolocation Analysis**: IP-to-country mapping for fraud pattern detection
4. **Business Context**: Balancing false positives vs false negatives

## Team

- **Tutors**: Mahlet, Rediet, Kerod, Rehmet
- **Project Timeline**: July 16-29, 2025

## Submission Status

- ✅ **Interim 1** (Due: July 20, 2025) - Task 1 Completed
- ⏳ **Interim 2** (Due: July 27, 2025) - Task 2 in Progress
- ⏳ **Final Submission** (Due: July 29, 2025) - Task 3 Pending

## Repository Link

This repository contains all code, analysis, and documentation for the fraud detection project.
