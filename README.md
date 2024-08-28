# Bioinformatics Predictive Models in R

This repository contains the R code and analysis for a statistical project focused on predictive modeling in bioinformatics. The project compares various machine learning models, including unconstrained linear models, Lasso regression, Ridge regression, Generalized Additive Models (GAM), and Random Forests, to predict patient survival based on a set of bioinformatics predictors.

## Table of Contents
- [Introduction](#introduction)
- [Dataset](#dataset)
- [Analysis Overview](#analysis-overview)
- [Models Used](#models-used)
- [Prerequisites](#prerequisites)
- [Installation](#installation)
- [Usage](#usage)
- [Results](#results)
- [Project Structure](#project-structure)
- [Contributing](#contributing)
- [License](#license)
- [Contact](#contact)

## Introduction

In this project, we explore various predictive models to analyze a dataset with 101 predictors and 1 binary response variable, LET_IS, which indicates patient survival. The high dimensionality and presence of missing data make this a challenging problem, suitable for advanced statistical techniques and machine learning methods.

## Dataset

- **Filename**: `MI.RData`
- **Description**: The dataset includes 102 columns (101 predictors and 1 response variable). It contains continuous and categorical predictors and some missing values, which are handled using predictive imputation.
- **Data Format**: RData file.

## Analysis Overview

The analysis includes:

1. **Data Exploration and Imputation**
   - Describing the predictor variables.
   - Handling missing data using the `mice` package for predictive imputation.
   - Splitting the data into training and testing sets.

2. **Model Fitting and Comparison**
   - Fitting and comparing an unconstrained linear model, Lasso regression, and Ridge regression.
   - Evaluating models based on accuracy, sensitivity, and specificity.
   - Comparing models to a baseline performance level.

3. **Incorporating Non-Linear Effects**
   - Identifying non-linear effects in the top predictors.
   - Fitting a Generalized Additive Model (GAM) and comparing its performance to regularized regression models.

4. **Random Forest Model**
   - Fitting a Random Forest model.
   - Comparing its performance to the linear models and analyzing how variables are used for predictions.

5. **ROC Curve Analysis**
   - Comparing the Area Under the Curve (AUC) for all models to evaluate their discriminative ability.

## Models Used

- **Unconstrained Linear Model**: A basic logistic regression model.
- **Lasso Regression**: L1-regularized logistic regression to handle high-dimensional data.
- **Ridge Regression**: L2-regularized logistic regression to handle multicollinearity.
- **Generalized Additive Model (GAM)**: A flexible model to capture non-linear effects.
- **Random Forest**: An ensemble learning method that handles complex interactions between variables.

## Prerequisites

- **R version**: 4.0 or higher
- **R packages**:
  - `mice`
  - `caret`
  - `glmnet`
  - `dplyr`
  - `gam`
  - `randomForest`
  - `pROC`

Ensure these packages are installed before running the analysis scripts.
