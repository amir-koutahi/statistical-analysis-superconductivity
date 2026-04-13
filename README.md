# Statitical Superconductivity Analysis

## Overview
This repository contains the final project for **STA302 – Methods of Data Analysis** at the University of Toronto. The project investigates statistical factors associated with **superconductor critical temperatures** using multiple linear regression.

The analysis focuses on identifying which physical and electronic properties are associated with higher critical temperatures in cuprate-based superconductors.

## Project Summary
- Response variable: Critical temperature (Tc), log-transformed as log(Tc + 1)
- Dataset: Top 1000 cuprate superconductors (UC Irvine ML Repository)
- Method: Multiple Linear Regression with both numerical and categorical predictors
- Goal: Interpret relationships rather than build predictive models

As stated in the report, the study examines:
> “Which physical properties of cuprate-based superconductors are correlated with high critical temperatures?” :contentReference[oaicite:0]{index=0}

## Key Features
- Log-transformation to address skewness and improve model assumptions
- Full model retained based on:
  - Partial F-tests
  - AIC and BIC comparison
- Diagnostic analysis:
  - Residual plots
  - Q–Q plots
  - Influence measures (Cook’s Distance, leverage, DFFITS)
- Sensitivity analysis with influential observations removed

## Key Findings
- **Positive associations with Tc:**
  - Weighted valence entropy (strongest effect)
  - Mean thermal conductivity

- **Negative associations with Tc:**
  - Mean electron affinity
  - Atomic radius

- **Categorical effects:**
  - Valence range plays a significant role, with some categories increasing and others decreasing Tc

- Model performance:
  - \( R^2 \approx 0.1965 \)
  - Adjusted \( R^2 \approx 0.1885 \)
  - Indicates moderate explanatory power

## Model
The final model is:

\[
\log(T_c + 1) = \beta_0 + \beta_1 X_1 + \cdots + \beta_4 X_4 + \text{Valence Range Terms} + \epsilon
\]

where predictors include entropy, electron affinity, atomic radius, thermal conductivity, and valence range.

## Structure
- `STA302_Proposal.pdf` – Full project report
- (Optional) R code / analysis files (if added later)

## Authors
- Amir Koutahi  
- Canberk Soytekin  
- Andrew Hongyi Wu  
- Bruce Kaiyuan Chen  

## Notes
- The model is **interpretative**, not predictive
- Results represent **statistical associations**, not causation
- A large portion of variability remains unexplained due to the complexity of superconductivity

## Usage
This repository is intended for:
- Academic reference
- Learning regression modeling and diagnostics
- Understanding applied statistical analysis in physics-related data

Please provide proper credit if reusing any part of this work.
