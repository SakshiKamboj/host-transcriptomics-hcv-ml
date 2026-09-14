# host-trancriptomics-hcv-ml
A reproducible workflow to develop machine learning models to classify the control and HCV infected samples using host transcriptomics data.

# Host Transcriptomics Machine Learning Workflow

## Overview

This repository contains a small machine-learning workflow for classifying Control and HCV-labelled samples using host gene-expression data.

I prepared this as a simplified demonstration of ML workflow used in my ongoing transcriptomics work. The example here uses simulated expression values, study labels, and generic gene names because the real dataset and results are currently unpublished.

The results shown does not represent any biological findings. The purpose is to demonstrate the code, validation strategy, and interpretation of model performance.

## Analysis

The notebook:

- simulates host gene-expression data from four studies;
- adds a small artificial signal to five features;
- introduces study-specific variation and missing values;
- handles imputation and scaling inside a scikit-learn pipeline;
- trains a linear Support Vector Machine;
- evaluates the pipeline using repeated stratified cross-validation;
- performs leave-one-study-out validation;
- reports balanced accuracy, MCC, ROC-AUC, and average precision;
- examines the fitted SVM feature weights;
- saves the results, figures, and simulated-data model.

## Repository Structure
host-transcriptomics-hcv-ml/
└── 01_hcv_control_ml_demo.ipynb
├── outputs/
│   ├── repeated_cv_results.csv
│   ├── loso_results.csv
│   ├── svm_feature_weights.csv
│   ├── repeated_cv_results.png
│   ├── svm_feature_weights.png
│   └── simulated_svm_pipeline.joblib
├── requirements.txt
├── README.md
└── .gitignore
