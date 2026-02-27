# Multiple Linear Regression – Cholesterol Analysis  
Biomedical Statistics Project (R)

---

## Project Overview

This project investigates the relationship between cholesterol levels and anthropometric variables using multiple linear regression.

Outcome variable:
- Cholesterol (C)

Explanatory variables:
- Weight (W)
- Height (H)
- Age (A)

The main statistical focus of the project is:

- Confounding effects
- Collinearity diagnostics
- Model comparison
- Interpretation of regression coefficients
- Prediction and hypothesis testing

---

## Dataset

The dataset contains measurements of:

- Age (years)
- Height (cm)
- Weight (kg)
- Cholesterol level

Sample size: 100 observations.

---

## Statistical Analysis

### Simple Linear Regression

First, cholesterol was modeled using weight only:

C ~ W

Initial interpretation suggested that cholesterol decreases with increasing weight.

However, this relationship was misleading due to confounding.

---

### Confounding Assessment

Stratified visualization by age showed that:

- Within age groups, slopes were mostly positive.
- Age acted as a confounder.

This demonstrated how aggregated regression results can be misleading.

---

### Multiple Linear Regression

Full model:

C ~ W + A + H

Key results:

- Weight coefficient became positive after adjustment.
- Age had a significant negative association.
- Height contributed independently.

Model fit:
- R² ≈ 0.74
- Residual standard error reduced substantially compared to the simple model.

---

## Collinearity Diagnostics

Variance Inflation Factors (VIF):

- W ≈ 9.49  
- A ≈ 20.90  
- H ≈ 31.69  

Strong collinearity between anthropometric variables was detected.

---

## Feature Engineering to Address Collinearity

To reduce collinearity, a new variable was constructed:

Excess Weight (EW)

Defined as:

Ideal weight = 0.5 × height − 10  
EW = max(0, real_weight − ideal_weight)

New model:

C ~ EW + A

Results:

- R² ≈ 0.77
- VIF ≈ 1 (collinearity resolved)
- Improved interpretability
- Reduced residual standard deviation

---

## Model Validation

- Residual diagnostics
- Q-Q plots
- Cook’s distance
- DFFITS
- Linearity and homoscedasticity checks

---

## Hypothesis Testing

Linear hypothesis tests were performed to assess:

- Whether predicted cholesterol equals a specific clinical value
- Statistical significance of contrast hypotheses

---

## Prediction

The model was used to:

- Compute confidence intervals
- Compute prediction intervals
- Compare absolute and relative prediction differences between models

---

## Technologies Used

- R
- car package
- HH package
- Linear modeling (lm)
- VIF diagnostics
- ANOVA (Type I & Type II)

---

## Skills Demonstrated

- Multiple linear regression
- Confounding detection
- Collinearity diagnostics (VIF)
- Feature engineering
- Model comparison
- Hypothesis testing
- Prediction intervals vs confidence intervals
- Statistical interpretation

---

## Note

This project is for educational purposes and focuses on statistical methodology and interpretation.
