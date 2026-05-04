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
- Mean calibration gap: about 6%

The model is useful but moderate. It should be interpreted as a group-level pattern-finding tool, not as a deterministic classifier for individual students.

## Repository Structure
├── Final.qmd
├── Final.pdf
├── Final_Capstone_Presentation.pptx
├── data/
├── versions/
├── outputs/
└── figures/
