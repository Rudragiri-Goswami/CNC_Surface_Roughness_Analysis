# CNC Surface Roughness Prediction

### Multiple Linear Regression on CNC Turning Data

## Overview

Surface roughness is an important indicator of machining quality and is influenced by different cutting conditions.

This project investigates how cutting speed, feed rate, and depth of cut are related to surface roughness and uses multiple linear regression to build an interpretable prediction model.

## Methods

- Exploratory Data Analysis
- Correlation Analysis
- Multiple Linear Regression
- Train-Test Evaluation
- 5-Fold Cross-Validation
- Residual Analysis

## Results

| Metric | 5-Fold CV |
|---|---:|
| R² | 0.579 |
| MAE | 0.160 |
| RMSE | 0.214 |

The model provides an interpretable baseline for relating machining parameters to surface roughness.

## Tools

Python · Pandas · NumPy · Matplotlib · Seaborn · Scikit-learn · Jupyter
