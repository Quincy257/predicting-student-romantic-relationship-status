# predicting-student-romantic-relationship-status
Capstone project using machine learning to predict student romantic relationship status.
This repository contains my capstone project on predicting whether a high-school student reports being in a romantic relationship.

## Project Overview

Adolescent romantic relationships are an important social and emotional development context. This project uses machine-learning methods to examine which student characteristics are most connected to romantic relationship status.

The project is predictive and descriptive rather than causal. The goal is not to label individual students, but to understand broad patterns in student social, academic, and behavioral contexts.

## Research Question

Which student characteristics best predict whether a high-school student reports being in a romantic relationship? Which content can most likely to involve their romantic relationship status?

## Data Source

The project uses the Kaggle **Student Alcohol Consumption** dataset:

https://www.kaggle.com/datasets/uciml/student-alcohol-consumption

The dataset includes two course files:

- `student-mat.csv`
- `student-por.csv`

Because some students appear in both course files, the final analysis merges repeated records into one student-level dataset.

## Final Modeling Pipeline

The final analysis uses:

- Student-level merged dataset
- Feature engineering
- Recipe preprocessing with `tidymodels`
- Logistic regression baseline
- Random Forest
- XGBoost
- SVM
- Elastic Net
- MLP
- Decision Tree
- Average-probability ensemble
- Stacking ensemble
- Probability calibration diagnostics

## Final Result

The final selected model is a tuned Random Forest.

Main held-out test results:

- Accuracy: 0.684
- AUC: 0.686
- The probability diagnostics suggest that the model provides useful group-level probability estimates, but not exact individual labels.

The model is useful but moderate. It should be interpreted as a group-level pattern-finding tool, not as a deterministic classifier for individual students.

## Development History

This project went through multiple iterations:

1. Initial baseline modeling with logistic regression and random forest.
2. Student-level duplicate handling across Math and Portuguese course files.
3. Feature engineering for behavioral, academic, and family-background variables.
4. Sex-specific modeling for female and male students.
5. Course-level grouped analysis to test whether keeping both course records improved prediction.
6. Ensemble and stacking comparison.
7. Probability-focused evaluation with calibration and KDE diagnostics.
8. Final pooled student-level model with sex retained as a predictor.

The final version does not simply maximize complexity. It balances predictive performance, interpretability, stability, and ethical interpretation.

## Repository Structure

```text
predicting-student-romantic-relationship-status/
├── README.md
├── Final_.pdf
├── Final_Capstone_Presentation.pptx
├── Final_code.qmd
├── student-mat.csv
├── student-por.csv
├── Final_project - E5.qmd
├── Final_project---E6.rmarkdown
├── final_project_e6.qmd
├── final_project_7.qmd
├── final_project_7 .2.qmd
├── final_project_8_probability.qmd
└── final_project_9_pooled_clean.qmd
```
