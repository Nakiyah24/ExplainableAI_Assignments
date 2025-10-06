# Explainable Deep Learning — Assignment 5

This repository contains code and analysis for **Assignment 5: Explainable Deep Learning**.  
The main focus is to implement and compare different **explainability methods** for deep learning models to  understand what parts of an image a model attends to when making predictions.

## Overview

For this assignment, I used a **pretrained ResNet-50** model from `torchvision.models` and applied explainability methods to classify **Himalayan bird species**. The project is motivated by **wildlife conservation**, aiming to understand how deep learning models perceive and differentiate species in natural environments.  
To evaluate explainability methods on realistic data, I curated a small collection of **Himalayan bird images** from **Kaggle’s bird species datasets**, providing a practical context for analyzing model attention and interpretability in biodiversity monitoring.

**Species included:**
- Bonelli’s Eagle (`bonegl`)
- Chestnut-bellied Rock Thrush (`cbrtsh`)
- Himalayan Bulbul (`himbul`)

Each class includes 2 sample images.


## Objectives

- Use a **pretrained model** (ResNet-50) for image classification.
- Implement **Grad-CAM**, **Grad-CAM++**, and **Score-CAM**.
- Generate **attention heatmaps** for at least 5 input images.
- Compare and analyze what regions each method highlights.
- Reflect on the **importance of explainability** in real-world computer vision tasks.


## Implementation Details

**Model Used:** `ResNet-50 (pretrained on ImageNet)`  

**Explainability Methods:**
- Grad-CAM  
- Grad-CAM++  
- Score-CAM  

**Steps:**

1. Load and preprocess bird images (224×224, normalized to ImageNet stats).
2. Run predictions through pretrained ResNet-50.
3. Generate Grad-CAM, Grad-CAM++, and Score-CAM visualizations.
4. Overlay heatmaps on original images for interpretability.
5. Compare how different CAM variants localize model attention.


## Results & Analysis

**Bonelli’s Eagle:**
Grad-CAM often highlighted rocky backgrounds, leading to misclassification (“cliff” or “valley”), showing model bias toward contextual textures rather than the bird itself.

**Chestnut-bellied Rock Thrush:**
The model’s attention was on correct regions, but still misclassified due to visual similarity with other species — indicating potential feature overlap in embeddings.

**Himalayan Bulbul:**
All CAM methods correctly focused on the bird’s head and body, corresponding to accurate predictions.