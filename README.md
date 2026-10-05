# TFP Prediction

An R project that uses country-level macroeconomic and demographic data to model and predict total factor productivity (TFP).

## Overview

This repository contains an R Markdown workflow for studying how TFP changes across countries and years. The analysis imports data from `final.xlsx` and `data1.csv`, merges them into a panel dataset, cleans missing values, and trains several predictive models in R.

## Models used

The project compares multiple statistical and machine learning approaches implemented in R:

- Linear regression
- LASSO regression with `glmnet`
- Reduced linear model
- Decision tree with `tree`
- Random forest with `randomForest`
- Ensemble model averaging predictions across models

The notebook also includes an experimental neural network section written through the R `keras` and `tensorflow` packages.

## Analysis included

- Data import and cleaning
- Exploratory data analysis of TFP over time
- Visualizations relating TFP to GDP and capital formation
- Country-specific sensitivity analysis
- Test-set model comparison using mean squared error

## Project structure

```text
TFP_Predictions/
├── FinalProject.Rmd
└── data/
    ├── final.xlsx
    └── data1.csv
```

`FinalProject.Rmd` is the main analysis file and contains the full workflow from preprocessing through evaluation.

## Requirements

This project is written in **R**. To run it, use RStudio or another R environment with the following packages installed:

```r
install.packages(c("pacman", "janitor", "caret", "readxl", "tidyverse"))
pacman::p_load(
  ggplot2, glmnet, dplyr, keras, tidyverse, tensorflow, magrittr,
  mlbench, car, coefplot, randomForest, tree, ISLR, rpart,
  rattle, pROC, partykit, janitor
)
```

## How to run

1. Clone the repository.
2. Add `final.xlsx` and `data1.csv` to the `data/` folder.
3. Open `FinalProject.Rmd` in RStudio.
4. Run the code chunks or knit the file to generate the analysis output.

## Notes

Some sections of the notebook appear to be in-progress, including repeated blocks and a partially completed neural network implementation.[1] Before publishing, it would help to clean commented code and add a short written summary of the main findings and best-performing model.[1]
