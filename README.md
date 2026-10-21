# QSAR-Based Machine Learning Pipeline for EGFR Inhibitor Discovery

![Python](https://img.shields.io/badge/Python-3.8%2B-blue)
![RDKit](https://img.shields.io/badge/RDKit-Cheminformatics-green)
![Scikit-Learn](https://img.shields.io/badge/Scikit--Learn-Machine%20Learning-orange)
![License](https://img.shields.io/badge/License-MIT-lightgrey)

## Overview
This repository contains an end-to-end Quantitative Structure-Activity Relationship (QSAR) machine learning pipeline designed to predict the bioactivity pIC_50 of small-molecule inhibitors against **Epidermal Growth Factor Receptor (EGFR)**. 

By integrating programmatic data extraction from the ChEMBL database, cheminformatics feature engineering via `RDKit`, and supervised regression modeling using `scikit-learn`, this project demonstrates how machine learning can accelerate early-stage lead optimization in drug discovery.

---

## Key Features
* **Automated Data Pipeline:** Programmatically fetches, cleans, and standardizes raw biological activity data IC_50 directly from the ChEMBL API.
* **Cheminformatics Feature Engineering:** Converts 1D SMILES strings into 2D chemical graphs to compute **Lipinski Descriptors** and **1024-bit Morgan Fingerprints (ECFP4)**.
* **Predictive Modeling:** Trains and evaluates a **Random Forest Regressor** to predict continuous binding affinities pIC_50.
* **Model Interpretability:** Extracts feature importances to highlight key physicochemical properties driving molecular activity.

---

## Repository Structure

```text
├── data/
│   ├── CHEMBL203_IC50_bioactivity_data.csv   # Raw bioactivity data fetched from ChEMBL
│   └── processed_qsar_dataset.csv            # Cleaned data with features & pIC50
├── notebooks/
│   ├── 01_data_fetching.ipynb                # ChEMBL API retrieval & cleaning
│   ├── 02_feature_engineering.ipynb          # RDKit descriptor & fingerprint generation
│   └── 03_model_training.ipynb               # Random Forest training & evaluation
├── requirements.txt                          # Dependencies for environment replication
├── LICENSE                                   # MIT License
└── README.md                                 # Project documentation
