---
noteId: "e5f40c90707f11f19ec49d9bd6d884a1"
tags: []

---

# Iris Dataset Visualization and Statistical Analytics

This repository contains a completed research notebook for exploring and modeling the Iris dataset. The work is written as a practical analytics report rather than a bare code exercise.

## What This Notebook Covers

- Dataset loading and quality review
- Descriptive statistics by species
- Exploratory visual analytics with distribution, scatter, violin, and pair plots
- Correlation and multicollinearity checks using VIF
- PCA variance analysis to show that not every variable explains equal variation
- ANOVA and eta-squared effect-size testing
- VADER sentiment applicability audit
- Regularized multiclass logistic regression with holdout and cross-validation evaluation

## Main Result

Petal length and petal width are the strongest species-separation variables. Sepal features provide supporting information but are more overlapping, especially between versicolor and virginica.

## How to Run

```bash
pip install -r requirements.txt
jupyter notebook notebooks/01_iris_dataset_visualization.ipynb
```

The notebook saves its exported charts in `outputs/figures/`.
