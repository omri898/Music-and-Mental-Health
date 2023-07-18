# Music Preferences and Mental Health State: Final Project

This repository contains an investigation into the correlation between an individual's musical preferences and their mental health state, leveraging statistical analysis and machine learning methods.

This README includes the necessary steps to download datasets, install dependencies, and replicate the project's results.

## Table of Contents

- [Getting Started](#getting-started)
- [Downloading Datasets](#downloading-datasets)
- [Running the Analysis](#running-the-analysis)
- [Files](#files)

## Getting Started

The project requires R and RStudio. It utilizes the following R packages: dplyr, scales, tidyr, ggplot2, data.table, readr, tidymodels, ranger, knitr, summarytools, tidyverse, recipes, stats, janitor, FactoMineR, factoextra, cluster, car, pheatmap, randomForest, Boruta.

To install these packages, run the following commands in your R console - this also present in each the first chunck of the rmd files:

```r
pkg <- c('dplyr', 'scales', 'tidyr', 'ggplot2', 'data.table', 'readr', 
         'tidymodels', 'ranger', 'knitr', 'summarytools', 
         'tidyverse', 'recipes', 'stats', 'janitor','FactoMineR','factoextra','cluster','car','pheatmap','randomForest','Boruta')

check_and_install <- function(p) {
  if(!require(p, character.only = TRUE)) {
    install.packages(p, dependencies = TRUE)
    library(p, character.only = TRUE)
  }
}

sapply(pkg, check_and_install)
```

## Downloading Datasets

This project uses two datasets available on Kaggle:

1. ["Music & Mental Health Survey Results"](https://www.kaggle.com/datasets/catherinerasgaitis/mxmh-survey-results): A survey of over 700 individuals asking about their music preferences, as well as their self-rated mental health scores.

2. ["Spotify Tracks Dataset"](https://www.kaggle.com/datasets/maharshipandya/-spotify-tracks-dataset): Information about 10,000 different songs on Spotify.

After downloading, place the datasets in a `data` folder in the main directory of the project.

## Running the Analysis

This project consists of two analyses:

1. **Regression Method**: Run the `regression_model.Rmd` file to perform the regression analysis. It contains the code to preprocess the data, generate the regression model, and visualize the results.

```r
rmarkdown::render("regression_model.Rmd")
```

2. **Classification Method**: Run the `classfication_model.Rmd` file to carry out the classification analysis. It includes the code for data preprocessing, creating the classification model, and visualizing the outcome.
   
```r
rmarkdown::render("classification_model.Rmd")
```
Note: This project uses a seed value of 123 in all random processes to ensure the reproducibility of the results and set in all relevant chunks in the code

## Files

- `regression_model.Rmd`: This R Markdown document contains the regression analysis. It includes code for data preprocessing, model generation, and results visualization.

- `classification_model.Rmd`: This R Markdown document contains the classification analysis. It includes code for data preprocessing, model generation, and results visualization.

- `/data`: This directory should contain the datasets. After downloading the datasets, please place them into this folder.
