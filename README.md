# Glaucoma Detection Using Machine Learning

The project integrates classical image processing, machine learning, and deep learning to automatically compute the Cup-to-Disc Ratio (CDR) and classify images as healthy or glaucomatous.


## Overview

Glaucoma is a leading cause of irreversible blindness. Early and accurate diagnosis is essential, yet conventional clinical evaluation is time-consuming and depends on expert interpretation. This project provides an automated system for:

- Preprocessing retinal fundus images
- Segmenting the optic disc and cup
- Calculating Cup-to-Disc Ratio (CDR)
- Classifying images using ML and DL models:
  - Support Vector Machine (SVM)
  - Decision Tree (DT)
  - K-Means Clustering
  - MobileViT Vision Transformer
- Laying the groundwork for a mobile-based glaucoma screening interface

---

## Features

### Preprocessing
- RGB channel extraction  
- CLAHE contrast enhancement  
- Adaptive thresholding  
- Morphological operations  
- Convex hull smoothing for optic cup boundaries  

### CDR Calculation
- Contour detection  
- Ellipse fitting on disc and cup  
- Vertical diameter measurement  
- Automatic computation of:  
  `CDR = (Vertical Cup Diameter) / (Vertical Disc Diameter)`

### Feature Extraction
- CNN deep features  
- Texture features (LBP, GLCM, Haralick)  
- Shape descriptors (area, perimeter, eccentricity, circularity)  
- CDR numeric values  

### Models Implemented
- SVM with hyperparameter tuning  
- Decision Tree classifier  
- K-Means with PCA  
- MobileViT (lightweight Vision Transformer)

---

## Results

| Model        | Accuracy | Precision | Recall | F1-Score |
|--------------|----------|-----------|--------|----------|
| MobileViT    | 97.38% | 97.00 | 97.50 | 97.25 |
| SVM          | 92.16% | 91.50 | 92.00 | 91.75 |
| Decision Tree| 84.31% | 83.50 | 84.00 | 83.75 |
| K-Means      | 83.17% | 82.00 | 83.50 | 82.75 |


## System Architecture

Fundus Image
     │
     ▼
Preprocessing (CLAHE + Thresholding + Morphology)
     │
     ▼
Disc & Cup Segmentation
     │
     ▼
CDR Calculation (Ellipse Fitting)
     │
     ▼
Feature Extraction (CNN + Texture + Shape + CDR)
     │
     ▼
ML/DL Classification (SVM / DT / K-Means / MobileViT)
     │
     ▼
Glaucoma / Healthy

## Repository structure

├── preprocessing/
├── cdr/
├── models/
│   ├── svm/
│   ├── decision_tree/
│   ├── kmeans/
│   └── mobilevit/
├── features/
├── interface/
├── images/
├── README.md
└── GlaucomaPaper.pdf

## Mobile Screening Interface

This project supports integration into mobile applications for real-time glaucoma screening:

- Upload retinal image  
- Automatic preprocessing  
- CDR calculation  
- ML/DL classification  
- Instant glaucoma prediction  
