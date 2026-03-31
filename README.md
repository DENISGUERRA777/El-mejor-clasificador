# El-mejor-clasificador

## Descripción / Description

Este repositorio contiene un proyecto de clasificación de préstamos usando Machine Learning. El objetivo es predecir si un préstamo será pagado (`PAIDOFF`) o entrará en cobranza (`COLLECTION`), comparando cuatro algoritmos de clasificación.

This repository contains a loan classification project using Machine Learning. The goal is to predict whether a loan will be paid off (`PAIDOFF`) or go to collection (`COLLECTION`), comparing four classification algorithms.

## Algoritmos comparados / Algorithms compared

| Algorithm | Description |
|-----------|-------------|
| **K-Nearest Neighbors (KNN)** | k=5 |
| **Decision Tree** | entropy criterion, max_depth=4 |
| **Support Vector Machine (SVM)** | RBF kernel |
| **Logistic Regression** | C=0.01, liblinear solver |

## Dataset

- **Source**: IBM Skills Network — `loan_train.csv` / `loan_test.csv`
- **Size**: 346 training records (75% PAIDOFF, 25% COLLECTION)
- **Features**: Principal, Terms, Age, Gender, Weekend, Education

## Resultados / Results

The best performing model is **SVM** with the highest Jaccard Index and F1-score on the test set.

## Requisitos / Requirements

```
numpy
pandas
matplotlib
seaborn
scikit-learn
```

## Uso / Usage

Open and run the notebook `ML0101EN-Proyecto-Final-py-v1_ES_py.ipynb` in Jupyter.

## Errores corregidos / Bug fixes

- Fixed wrong dataframe reference (`df` → `test_df`) in test date conversion cells.
- Replaced deprecated `jaccard_similarity_score` with `jaccard_score` (scikit-learn ≥ 0.23).
- Replaced deprecated `DataFrame.append()` with `pd.concat()` (pandas ≥ 2.0).
- Removed duplicate `import numpy as np` statement.
