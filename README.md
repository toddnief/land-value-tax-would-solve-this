A description of the directory structure, and a brief description of the purpose of each file and the number of lines of code in it. 

You should have a separate directory for code written as part of this project, and a separate directory for code not written by a team mem- ber or not written as a part of this project. These should be clearly identified in your readme file. 

Any other relevant information about your code.

## Notebooks

The primary notebook is the `regression-notebook.ipynb`. This includes code that will load the City of Philadelphia's assessment data for tax year 2023 and perform regression on it.

The notebook contains the following main sections:

1. Data-Cleaning Pipeline: Clean the data, bucket continuous variables, and prepare it for the regression task
2. Adaptive Weights Smoothing: Perform nonparametric kernel regression to estimate land values from vacant lot transactions. Use the adaptive weights smoothing method of Kolbe, at al. from "Identifying Berlin's land value map using Adaptive Weights Smoothing"
3. Feature Selection: Identify the most important features for regression in an interpretable fashion. XGBoost feature selection calculates feature importance by calculating the improvement in the splitting metric (Gini index, information gain, etc.) weighted by the number of observations at that node.
4. Cross-validation and Model Scoring: Evaluate ordinary least squares, Ridge, Lasso, and XGBoost using mean absolute error, coefficient of dispersion, price-related differential, and more.
5. Fit and Test Models: Fit models to the training data and test them on the testing set (not used in training or model tuning)

This directory also includes `unused-code.ipynb`. Throughout this project, I experimented with a variety of methods in different notebooks. I consolidated most of the potentially interesting code from those methods into this notebook as a reflection of "other things tried during this project." The code in here does not work and is not particularly organized. However, the headings should give an idea of what the code is doing.

## Data

The data used in this project is located in `notebooks/data`. This is the data used in the models and comes from Open Data Philly here: https://www.opendataphilly.org/dataset/opa-property-assessments