## Predicting survival of patients with liver disease

Read my publications regarding the project on Medium:  
* [Part 1](https://medium.com/@meinzaugarat/building-my-first-data-science-project-part-1-exploratory-analysis-9112684badcd)  
* [Part 2](https://medium.com/@meinzaugarat/building-my-first-data-science-project-part-2-prediction-cc4d971aa17a)

## Introduction
Prognosis is an important part in the assessment of any disease. Particularly, liver disease has become one of the most common 
causes of death around the world, after heart disease and cancer. Independently of etiology, cirrhosis is the final end point 
in patients with progressive liver disease, though it can be variable from patient to patient. As a consequence, establishing 
a method to assess the prognosis of a particular patient with liver disease still remains a challenge. 

## Purpose
The purpose of this project is to analysis a dataset containing information about liver disease patients and create a model to 
predict their survival. 

This repository includes the following main files:

* a dataset `dataset_55_hepatitis.csv` used to perform the analysis.
* a code book that describes the variables and the data called `CodeBook.md`. 
* a `README.md` that explains how all of the scripts work and how they are connected.
* a jupyter notebook that shows the exploratory data analysis performed called `EDA from dataset of patients with hepatitis.ipynb`. 
* a jupyter notebook that shows processing the data, creating, fitting and tunning the Random Forest Classifier used called `Prediction of survival in patients with hepatitis.ipynb`. 


## Data Set Information
The csv file corresponding used herein was downloaded from [Open ML](https://www.openml.org/d/55) and more information can also be found in [UCI Machine Learning Repository](https://archive.ics.uci.edu/ml/datasets/hepatitis). The dataset was originally donated by G.Gong (Carnegie-Mellon University) via Bojan Cestnik Jozef Stefan Institute in Ljubljana and date back to November, 1988.  This comprise an observational study where data was collected regarding 19 different features and an extra class (DIE or LIVE) from 155 patients with chronic liver disease within an age bracket of 7-78 years. 

## Analysis

`EDA from dataset of patients with hepatitis.ipynb` perform the following tasks:

* Reads the `CSV file` into a **Pandas DataFrame**.
* Replace the missing values identify with `?` for **Numpy** `NaN`, categorical values `yes` or `no` for `1` or `0` respectively, and converts the diagnostic `LIVE` or `DIE` for the numerical representations: `1` or `0`.
* *Exploratory Data Analysis*:
    - Checks if dataset suffers of **Class imbalance**
    - Obtains descriptive statistics summarizing central tendency, dispersion and shape of the dataset’s distribution
    - Creates visuals in order to explore the relationships existent in the dataset

`Prediction of survival in patients with hepatitis.ipynb` perform the following tasks:

* Replace the missing values identify with `?` for **Numpy** `NaN`, categorical values `yes` or `no` for `1` or `0` respectively, and converts the diagnostic `LIVE` or `DIE` for the numerical representations: `1` or `0`.
* *Random Forest Classifier*:
    - Splits the dataset into Train/Test sets
    - Creates Random Forest Classifier
    - Fit the algorithm with best parameters
    - Performs cross validation
    - Predict survival with test set
    - Calculate metrics from the model


## References
1. Dua, D. and Karra Taniskidou, E. (2017). UCI Machine Learning Repository [http://archive.ics.uci.edu/ml]. Irvine, CA: University of California, School of Information and Computer Science.
