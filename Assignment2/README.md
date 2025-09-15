# Customer Churn Prediction — Interpretable ML  

This project explores different modeling approaches to predict **customer churn** using the [Telco Customer Churn dataset](https://www.kaggle.com/datasets/blastchar/telco-customer-churn). The focus is not only on predictive performance but also on **interpretability**, so that the results are actionable for a telecommunications company.  

## Project Overview  
The assignment walks through three modeling approaches and compares them:  

1. **Linear Regression (OLS)**  
   - Treats churn as a continuous outcome (0/1).  
   - Useful as a baseline, but violates key assumptions (heteroscedasticity, non-normal residuals, multicollinearity).  
   - R² ≈ 0.28, Accuracy ≈ 80%, ROC-AUC ≈ 0.83.  

2. **Logistic Regression**  
   - Handles churn properly as a binary variable.  
   - Feature selection done with **LASSO (L1 penalty)**, followed by a cleaned **L2 logistic regression**.  
   - Achieved Accuracy ≈ 80.7%, ROC-AUC ≈ 0.84, PR-AUC ≈ 0.63.  
   - Odds ratios provide clear interpretation:  
     - Long contracts, tenure, dependents, online security, and tech support **reduce churn**.  
     - Fiber optic internet, streaming services, paperless billing, and electronic check payments **increase churn**.  

3. **Generalized Additive Model (GAM)**  
   - Extends logistic regression by modeling non-linear effects.  
   - Accuracy ≈ 80%, ROC-AUC ≈ 0.84, PR-AUC ≈ 0.66.  
   - Revealed a sharp **early decline in churn risk with tenure**, flattening for long-tenured customers.  
   - Similar categorical effects as logistic regression.  

---

## Key Insights  
- **OLS**: Simple but inappropriate for binary churn — produces invalid probabilities and unstable coefficients.  
- **Logistic regression**: Strong baseline, interpretable, and business-friendly.  
- **GAM**: Adds flexibility for non-linear effects (especially tenure), making insights richer without losing interpretability.  
