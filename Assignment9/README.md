# Reverse-Complement LSTM — Mechanistic Interpretability

This project trains a tiny LSTM to learn the reverse-complement transformation of short DNA sequences. The goal isn’t high accuracy — it’s to build a model small enough that we can open it up, visualize its hidden states, and actually understand how it works.

## Project Overview

We generate synthetic DNA sequences using the four bases: **A, T, G, C**.

**The task:**

- **Input:** `A T G C A`  
- **Output:** `T G C A T` (reverse + complement)

We train a small 1-layer LSTM so that its internal activations are easy to inspect.

This setup creates a simple, controlled environment for mechanistic interpretability — basically, a tiny “brain” that we can poke at.


## What’s Inside the Notebook

### 1. Data Generation
- We create random DNA sequences and encode each base as an integer  
  (A=0, T=1, G=2, C=3).
- Then we compute the correct reverse-complement labels.

### 2. Model Training
We train:
- A **1-layer LSTM**
- A **very small hidden size** (so interpretation is possible)
- A **linear layer** that maps hidden states → base predictions

Training is intentionally lightweight so the internal structure doesn’t get too complicated.

### 3. Inspecting the Model
We visualize:
- Predicted logits for a sample sequence  
- Hidden activations after each base  
- A **heatmap** showing neuron activation by base type  
- A **line plot** showing how each neuron behaves across sequence positions  

These plots reveal which neurons encode what — for example, some track position, some respond to bases, and some barely activate at all.

### 4. Reflection
Includes a short written reflection on:
- What the hidden states revealed about how the model works  
- What was confusing or surprising  
- What you'd explore next (e.g., deeper LSTMs)

---

## Key Takeaways
- Even tiny LSTMs develop structured behaviors.  
- Visualizations are essential — raw activations mean nothing on their own.  
- Some neurons encode **position**, some encode **base identity**, and some do almost nothing.  
- Mechanistic interpretability becomes manageable when you shrink the model.

