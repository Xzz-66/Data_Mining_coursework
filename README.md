# Data Mining Techniques – Group Project 

## Overview

This repository contains our group work for **Assignment 1** of the *Data Mining Techniques* course at Vrije Universiteit Amsterdam. We worked on the **advanced mental-health smartphone dataset**, where the goal is to predict **next-day mood** from irregular, longitudinal behavioural and self-report data. The assignment explicitly frames the advanced version around a complex temporal dataset and asks for both a standard machine-learning pipeline and an inherently temporal model. 

Our workflow follows the CRISP-DM spirit of the assignment:
1. exploratory data analysis,
2. data cleaning,
3. missing-value imputation,
4. feature engineering,
5. classification and regression modelling,
6. evaluation and interpretation. 

## Dataset Properties 

The dataset is not a clean tabular matrix. It is a **multivariate longitudinal dataset** with:
- **irregular timestamps**,
- **multiple users**,
- **variables measured at different frequencies**,
- **explicit and implicit missingness**,
- **noisy and infeasible duration records**,
- and a **temporal prediction target** rather than a static label. 

## Skills and methods used
### 1. Data understanding and exploratory analysis
### 2. Data cleaning tailored to irregular temporal data
Instead of relying only on generic outlier rules, we used **domain-aware and time-aware cleaning**:
### 3. Missing-value imputation for health time series
The advanced assignment asks for time-series-aware imputation. We compared:
- **linear interpolation** as a transparent baseline,
- **BRITS** as a neural imputation method for multivariate time series. 
### 4. Feature engineering for temporal prediction
A key skill in this project was transforming raw time series into an **instance-based prediction dataset** for standard machine learning, exactly as required in the advanced assignment. 

## Application of neural networks
A major part of the repository is the application of a **Long Short-Term Memory (LSTM)** neural network as the inherently temporal model requested in the advanced assignment. 

The neural network was used in both:
- **classification**, where next-day mood was turned into discrete classes, and
- **regression**, where next-day mood remained numerical. 


## Modelling summary
### Classification
We compared:
- a **feature-engineered HistGradientBoosting classifier**,
- and a **sequence-based LSTM classifier**. 

### Numerical prediction
We compared:
- **Ridge regression** on the feature-engineered dataset,
- and an **LSTM ensemble** on daily sequences. fileciteturn0file1L229-L266

