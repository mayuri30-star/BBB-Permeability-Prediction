# BBB-Permeability-Prediction
Blood–Brain Barrier (BBB) permeability using Morgan fingerprints + predicted logBB and SMILES embeddings, comparing both approaches with XGBoost.
# Blood–Brain Barrier Permeability Prediction using Machine Learning

## Overview

This repository presents a machine learning workflow for predicting Blood–Brain Barrier (BBB) permeability of small molecules.

Two molecular representations were evaluated:

- Morgan Fingerprints + Predicted logBB
- Transformer-based SMILES Embeddings (MegaMolBART)

The objective is to classify compounds as BBB-permeable (BBB+) or BBB-non-permeable (BBB−).

---

## Workflow

```
Data Collection
        │
        ▼
Data Cleaning
        │
        ▼
Canonical SMILES
        │
        ▼
Feature Generation
   ├── Morgan Fingerprints
   └── SMILES Embeddings
        │
        ▼
logBB Prediction
(Random Forest)
        │
        ▼
XGBoost Classification
        │
        ▼
Performance Evaluation
```

---

## Repository Structure

```
scripts/
    data_processing.py
    smiles_embeddings.py
    model_training.py

results/
    ROC Curve
    Confusion Matrix
    Feature Importance

docs/
    Project Report
```

---

## Features

- Data preprocessing
- Canonical SMILES generation
- Morgan fingerprint generation
- Transformer-based molecular embeddings
- logBB regression
- XGBoost classifier
- ROC Curve
- Precision-Recall analysis
- Confusion Matrix
- Feature Importance

---

## Machine Learning Models

Regression

- Random Forest Regressor

Classification

- XGBoost

---

## Molecular Representations

- Morgan Fingerprints (RDKit)
- MegaMolBART Embeddings

---

## Technologies

- Python
- RDKit
- XGBoost
- HuggingFace Transformers
- Scikit-learn
- Pandas
- NumPy

---

## Results

The fingerprint-based model using predicted logBB achieved substantially better performance than the transformer-based embedding model, indicating that structural molecular fingerprints combined with physicochemical information provide more discriminative features for BBB permeability prediction.

---

## References

- LightBBB
- B3DB
- MegaMolBART
- RDKit
