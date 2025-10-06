# Interpretable Machine Learning — Assignment 4

This repository contains code and analysis for **Assignment 4: Interpretable Machine Learning**.  
The main focus is to apply and compare different model interpretability methods on student performance prediction using tree-based models.


## Project Overview

The dataset consists of student-level features (e.g., absences, study time, failures, etc.) and the target variable is **final Math grade (G3)**.  
A Random Forest Regressor is trained, and we explore **feature interpretability** with global and local explanation tools.  

Key features of interest:  
- `absences`  
- `studytime`  


## Methods

I use three main interpretability techniques:

1. **Partial Dependence Plot (PDP)**  
   - Shows the *average marginal effect* of a feature on model predictions.  
   - Useful for global insights, but can hide heterogeneous effects.  

2. **Individual Conditional Expectation (ICE)**  
   - Plots the effect of varying a feature for *each individual observation*.  
   - Highlights interactions and variation hidden by PDP averaging.  

3. **Accumulated Local Effects (ALE)**  
   - Captures *local changes* in predictions as a feature varies.  
   - More robust than PDP in skewed or correlated data regions, since it does not extrapolate into sparse areas.  


## Results

- **1D PDP + ICE** for `absences` and `studytime` show general trends but also individual differences.  
- **2D ALE plots** highlight how *combinations* of `absences` and `studytime` affect predictions.  
  - High absences + low studytime → lower grades.  
  - Moderate absences + high studytime → better grades.  
  - Extreme values (very high absences or very low studytime) → negative effect.  
