# Latent Behavioral Structure in Synthetic Customer Data  
### PCA, Factor Analysis, and Regularized Regression

## 📌 Project Overview

This project investigates the latent behavioral structure of a large synthetic customer dataset using multivariate statistical techniques and regularized regression models.

The objective is to:

- Identify underlying behavioral dimensions using Principal Component Analysis (PCA)
- Interpret latent factors driving customer engagement and purchasing behavior
- Compare predictive performance of LASSO and Ridge regression
- Build a structured multivariate modeling pipeline suitable for real-world analytics

The dataset contains **50,000 synthetic customers** and multiple behavioral, demographic, and engagement features.

---

## 📊 Dataset Description

The synthetic dataset includes:

### Demographics
- Age
- Gender
- Country
- Income

### Engagement Metrics
- Website_Visits
- App_Opens
- Support_Tickets
- Avg_Session_Duration_Minutes

### Purchase Behavior
- Total_Purchases
- Avg_Purchase_Value
- Last_Purchase_Days_Ago

### Feedback Metrics
- Satisfaction_Score
- Likelihood_to_Recommend

### Target Variable
- Churn (Binary: 0 = Active, 1 = Churned)

All variables were standardized before multivariate analysis.

---

# 🔎 Principal Component Analysis (PCA)

PCA was conducted on standardized numeric features.

## Key Findings

- **9 principal components explain ~82% of total variance**
- No single dominant latent factor — dataset exhibits moderately distributed variance structure
- Indicates behavioral heterogeneity among customers

---

## 📌 Interpretation of Major Components

### PC1 – Transactional vs Affluent-Satisfied Behavior

Top loadings:

- Total_Purchases (+)
- Likelihood_to_Recommend (+)
- Income (-)
- Satisfaction_Score (-)
- Avg_Session_Duration_Minutes (-)

**Interpretation:**

This component captures a behavioral contrast between:

- High-frequency purchasers with high recommendation tendencies  
vs  
- Higher-income, highly satisfied, longer-session customers

---

### PC2 – Mature Loyal Users vs Active Browsers

Top loadings:

- Age (+)
- Satisfaction_Score (+)
- Avg_Session_Duration_Minutes (+)
- Website_Visits (-)
- Last_Purchase_Days_Ago (-)

**Interpretation:**

This dimension contrasts:

- Older, satisfied, longer-engagement users  
vs  
- More active website visitors and recent purchasers

---

# 🧠 Statistical Insight

The requirement of 9 components to reach 80% variance suggests:

- Moderate correlation structure
- Absence of strong dominant latent factors
- Realistic multivariate customer heterogeneity

This is consistent with high-dimensional behavioral datasets in real-world analytics.

---

# 📉 Factor Analysis (Next Phase)

To further investigate latent structures, exploratory Factor Analysis is applied:

- Extraction using Maximum Likelihood
- Rotation for interpretability
- Factor loading interpretation
- Dimensionality reduction beyond PCA

This allows clearer identification of latent behavioral constructs.

---

# 📈 Regularized Regression Models

To evaluate predictive structure, the following models are implemented:

- LASSO Regression (L1 Regularization)
- Ridge Regression (L2 Regularization)

Objectives:

- Identify key predictive drivers
- Compare coefficient shrinkage patterns
- Assess multicollinearity impact
- Improve model generalization

Regularization helps prevent overfitting and highlights meaningful predictors.

---

# 🛠 Methodology Pipeline

1. Data Standardization
2. PCA Decomposition
3. Cumulative Variance Analysis
4. Component Loading Interpretation
5. Factor Analysis with Rotation
6. LASSO vs Ridge Model Comparison
7. Model Performance Evaluation (MSE, Cross-validation)

---

# 📦 Tools & Libraries

- Python
- Pandas
- NumPy
- Scikit-learn
- Statsmodels
- Matplotlib / Seaborn

---

# 📌 Key Takeaways

- Customer behavior is multi-dimensional and not dominated by a single latent factor.
- Regularized regression provides stable predictive modeling under multicollinearity.
- PCA and Factor Analysis complement each other for structural understanding.

---

# 🚀 Future Extensions

- Bayesian Logistic Regression (PyMC)
- Churn classification using SVM / Tree models
- Clustering in principal component space
- Time-series behavioral modeling

---

# 👨‍💻 Author

Tushar Sachdev  
Data Science & Statistical Modeling  
Machine Learning | Bayesian Inference | Multivariate Analysis
