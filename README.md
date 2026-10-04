# CNC Surface Roughness Prediction

### Multiple Linear Regression for CNC Turning Data

## Overview

This project investigates the relationship between CNC turning parameters and surface roughness using experimental machining data.

Cutting speed, feed rate, and depth of cut are used as explanatory variables, while surface roughness (Ra) is treated as the response variable.

Multiple linear regression is used as the main modelling approach because it provides an interpretable relationship between the machining parameters and surface roughness.

The project also includes exploratory data analysis, train-test evaluation, cross-validation, prediction analysis, and residual diagnostics.

---

## Objectives

- Explore the experimental CNC turning dataset
- Analyze the relationship between machining parameters and surface roughness
- Build a multiple linear regression model
- Evaluate model performance using R², MAE, and RMSE
- Validate the model using five-fold cross-validation
- Analyze prediction errors using residual diagnostics
- Interpret the fitted regression coefficients
- Establish an interpretable baseline for surface roughness prediction

---

## Dataset

The dataset contains **324 experimental observations** and **27 variables** related to CNC turning experiments.

The main variables used in this project are:

| Variable | Description |
|---|---|
| `vc` | Cutting speed |
| `f` | Feed rate |
| `ap` | Depth of cut |
| `Ra` | Surface roughness |

The dataset also contains additional measurements including cutting forces, tool information, machining conditions, and other surface roughness parameters.

Only cutting speed, feed rate, and depth of cut are used as predictors in the main regression model.

---

## Methodology

The analysis follows these steps:

1. Load and inspect the experimental dataset
2. Check dataset dimensions and missing values
3. Select the variables required for modelling
4. Perform exploratory data analysis
5. Analyze correlations between variables
6. Fit a multiple linear regression model
7. Evaluate training performance
8. Evaluate performance on a held-out test set
9. Perform five-fold cross-validation
10. Analyze actual vs predicted surface roughness
11. Examine residuals
12. Interpret regression coefficients
13. Summarize the model results and limitations

---

## Regression Model

The model is formulated as:

$$
R_a = \beta_0 + \beta_1v_c + \beta_2f + \beta_3a_p
$$

where:

- $R_a$ = surface roughness
- $v_c$ = cutting speed
- $f$ = feed rate
- $a_p$ = depth of cut
- $\beta_0$ = intercept
- $\beta_1, \beta_2, \beta_3$ = regression coefficients

---

## Model Performance

The fitted model produced the following results:

| Metric | Training | Test | 5-Fold CV |
|---|---:|---:|---:|
| R² | 0.589 | 0.620 | 0.579 |
| MAE | 0.158 | 0.155 | 0.160 |
| RMSE | 0.211 | 0.215 | 0.214 |

The similar training, test, and cross-validation results suggest that the model does not show strong evidence of severe overfitting on this dataset.

The five-fold cross-validation results provide the main reference for evaluating the model's predictive performance.

---

## Regression Coefficients

The fitted coefficients were:

| Parameter | Coefficient |
|---|---:|
| Cutting speed (`vc`) | -0.000969 |
| Feed rate (`f`) | 9.928713 |
| Depth of cut (`ap`) | -0.061453 |

The positive coefficient for feed rate indicates an increase in predicted surface roughness as feed rate increases, while cutting speed and depth of cut have negative fitted coefficients.

These coefficients describe the fitted linear relationships within the experimental conditions and should not be interpreted as causal effects.

---

## Key Findings

The multiple linear regression model explains approximately 58% of the variation in surface roughness according to the five-fold cross-validation R².

The model achieved a cross-validation MAE of approximately 0.160 and RMSE of approximately 0.214.

The relatively similar training, test, and cross-validation performance indicates that the model generalizes reasonably consistently within this dataset.

Feed rate has a positive fitted relationship with surface roughness, while cutting speed and depth of cut have negative coefficients.

The regression model provides an interpretable baseline for relating machining parameters to surface roughness.

---

## Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Jupyter Notebook

---
