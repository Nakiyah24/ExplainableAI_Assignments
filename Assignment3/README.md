# README – Explainable Techniques: Machine Learning Court  

## Project Overview  
This project is part of the *Machine Learning Court* assignment, where students investigate a real-world AI decision and argue for or against its validity using explainable AI (XAI) methods. I was assigned the **Loan Approval Case** as the **Prosecution**, tasked with challenging the fairness of the model’s decision.  

## Objectives  
- Analyze the given loan dataset and pre-trained model.  
- Apply at least two XAI techniques to interpret the model’s decision.  
- Evaluate whether the model’s reasoning is fair, valid, and free from bias.  
- Present evidence in a structured, case-like argument.  

## Methods Used  
- **LIME** (Local Interpretable Model-Agnostic Explanations) to identify influential features in the model’s prediction.  
- **Anchors** to uncover rule-based explanations and highlight conditions that may almost always lead to a loan denial.  

## Key Findings  
- The model placed disproportionate weight on weak and potentially unfair signals (e.g., marital status, relationship type) instead of more relevant financial indicators.  
- Anchors revealed rigid rules that penalize applicants based on non-financial attributes - strongly suggest bias.  
- Positive factors such as education, occupation, and work hours were undervalued in the prediction process.  
- Model was trained on corrupted y variables which had to be fixed to create the correct model 

## Files  
- **Assignment3.ipynb** – Jupyter Notebook containing the full analysis, code, and plots.  
**machine_learning_court.ipynb** - Starter court for the assignment
- **Explainable Techniques - Machine Learning Court.pdf** – Written report presenting the prosecution’s case, including interpretations and fairness evaluation.  


## Notes  
- Code for building LIME and Anchors explanations, along with plot generation, was developed with help from **ChatGPT-5**.
