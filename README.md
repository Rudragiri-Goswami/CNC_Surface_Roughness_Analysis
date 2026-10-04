# CNC Surface Roughness Prediction

### Multiple Linear Regression on CNC Turning Data

## Overview

This project analyzes the relationship between CNC turning parameters and surface roughness using multiple linear regression.

The main parameters are:

- Cutting speed (`vc`)
- Feed rate (`f`)
- Depth of cut (`ap`)
- Surface roughness (`Ra`)

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
