# Interpretable Machine Learning Assignments  

This repo contains my coursework and projects for Interpretable ML. Each assignment has its own folder with a notebook, report, and README.  

**Assignment 2** — *Customer Churn Prediction*: Compared OLS, logistic regression (with LASSO feature selection), and GAMs on the Telco dataset. Focused on both predictive performance and interpretability.  

**Assignment 3** — *Machine Learning Court (Loan Case)*: Acted as the prosecution to challenge the fairness of a loan approval model using LIME and Anchors. Showed how the model relied on weak or biased signals while undervaluing key financial indicators.  

**Assignment 4** — *Student Performance Prediction*: Trained a Random Forest on student grade data and explored model interpretability using PDP, ICE, and ALE. Focused on the features `absences` and `studytime`, showing how their combinations influence predicted grades. PDP gave global averages, ICE revealed heterogeneous effects, and ALE highlighted local patterns without extrapolating into sparse regions.  

**Assignment 5** — *Explainable Deep Learning*: Used a pretrained ResNet-50 model to classify Himalayan bird species and applied Grad-CAM, Grad-CAM++, and Score-CAM to visualize model attention. Compared how each method highlighted different image regions and reflected on when the model focused on relevant versus misleading cues. The task emphasized explainability’s role in wildlife conservation by revealing how deep models perceive species and what features drive their predictions.  

**Assignment 6 – Part I: Blog — Permutation Feature Importance (PFI)**  
Explained the concept of Permutation Feature Importance for a general-audience blog. Introduced how PFI measures a model’s reliance on each feature by observing the drop in performance after randomly shuffling that feature. Used simple examples (like study hours and exam scores) to show how shuffling breaks the link between variables and targets. Discussed strengths (model-agnostic, easy to interpret), limitations (correlated features, computational cost), and why PFI provides an intuitive yet powerful way to peek inside black-box models.

**Assignment 6 – Part II: Code Tutorial — Permutation Feature Importance (PFI)**  
Implemented PFI using the California Housing dataset to understand which features most influence a Random Forest regressor’s predictions of median house value. Built a baseline model, computed the drop in R² for each feature, and visualized results with a table and bar chart (mean ± std). Found that **Median Income**, **Latitude**, and **Longitude** were dominant predictors. Reflected on how PFI provides a global ranking of feature importance and how it can be extended to multiple models and metrics for deeper interpretability analysis.  

*(More assignments will be added here as I complete them.)*
