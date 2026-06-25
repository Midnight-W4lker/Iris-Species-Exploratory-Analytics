# Iris Species Exploratory Analytics

## Web Report

A static web representation is available in `docs/index.html`. After enabling GitHub Pages from the `docs` folder, it can be viewed as a project report page.


## Project Overview

This project analyzes the classic Iris dataset as a compact but complete research workflow for exploratory analytics, statistical testing, feature interpretation, and multiclass classification. The goal is to understand how well four flower measurements can separate three Iris species: setosa, versicolor, and virginica.

The notebook is written as a research report rather than a simple plotting exercise. It studies the data quality, compares species-level distributions, checks whether all variables explain equal variation, and builds a transparent classification baseline.

## Problem Definition

Botanical identification can be time-consuming when observations must be inspected manually. The business/research problem is to determine whether simple physical measurements are enough to distinguish Iris species reliably.

The specific questions are:

- Which measurements best separate the species?
- Do all variables contribute meaningful independent information?
- Is a simple interpretable model enough for accurate species classification?
- Is sentiment analysis relevant for this dataset?

## Dataset

The dataset is loaded from `sklearn.datasets.load_iris` and contains:

- 150 flower observations
- 4 numeric measurements: sepal length, sepal width, petal length, petal width
- 3 balanced species classes

No external CSV is required for this project.

## What Is Covered

- Data loading and quality review
- Descriptive statistics by species
- Distribution, scatter, violin, and pair-plot visualizations
- Correlation heatmap and multicollinearity review using VIF
- PCA variance analysis
- ANOVA and eta-squared effect-size testing
- VADER sentiment applicability audit
- Regularized multiclass logistic regression
- Holdout and cross-validation evaluation

## Key Findings

- Petal length and petal width provide the clearest separation between species.
- Setosa is visually and statistically distinct from the other two classes.
- Versicolor and virginica overlap more, especially in sepal-based views.
- Sepal width is the weakest separator among the four measurements.
- Petal length and petal width are highly correlated, so they should not be interpreted as fully independent signals.
- PCA shows that most variance is concentrated in the first component, meaning not every feature explains equal independent variation.
- VADER sentiment analysis is not applicable because the dataset has no free-text fields.

## Solution Approach

The solution uses a transparent analytics pipeline:

1. Inspect the dataset for shape, balance, missingness, and feature types.
2. Use exploratory visualizations to understand species separation.
3. Apply statistical tests to confirm which features are meaningfully different across species.
4. Use VIF and PCA to understand redundancy and variance concentration.
5. Train a regularized logistic regression classifier for interpretable species prediction.

## Results Summary

The notebook shows that a simple regularized multiclass classifier is appropriate for this dataset. The model performs strongly because the petal variables naturally separate the species, especially setosa. The main analytical lesson is not just that Iris can be classified, but that petal measurements carry most of the useful signal.

## Repository Structure

```text
notebooks/
  01_iris_dataset_visualization.ipynb
outputs/figures/
  Exported charts from the notebook
requirements.txt
README.md
```

## How to Run

```bash
pip install -r requirements.txt
jupyter notebook notebooks/01_iris_dataset_visualization.ipynb
```

## Conclusion

Petal measurements are the strongest basis for Iris species classification. Sepal measurements still provide context, but they are less decisive. The final model is intentionally simple and interpretable, which fits the size and cleanliness of the dataset.
