# Project Title

A short description of what your project does or aims to achieve.

## Table of Contents
1. [Introduction](#introduction)
2. [Methodology](#methodology)
3. [Model Evaluation](#model-evaluation)
4. [Results](#results)
5. [Conclusion](#conclusion)
6. [Installation & Usage](#installation--usage)
7. [Project Structure](#project-structure)
8. [References](#references)

---

## Introduction
- **Objective**:
The goal of this project is to first, to identify the key factors that influence individuals to open a term deposit, and to compare the performance of different classification models in predicting these outcomes. 
The dataset comprises various demographic info such as job type, marital status, and education level for each individual contacted. By analyzing these features, this study aims to pinpoint the most significant 
determinants that drive a person’s decision to secure a term deposit.

## Methodology

### Data Cleaning & Preparation
- There was no missing data found in the dataset.
- Pipelines were created for scaling and encoding the data, using `StandardScaler` and `OneHotEncoder`.

### Model Selection
- Many models were used, such as: **Logistic Regression, KNN, Decision Trees, and SVM**

### Train/Test Split
- An 80/20 train/test split was performed.
- **X** includes all features excluding `y`, and **y** is the target (`term_deposit`).


## Model Evaluation

**Performance Metrics:**

| Model | Duration | TrainAccuracy | TestAccuracy |
|-------|----------|---------------|--------------|
| Improved Logistic Regression | 2383.7926s | 0.9154 | 0.9155 |
| Improved KNN | 399.3780s | 0.9178 | 0.9120 |
| Improved DT | 158.4452s | 0.9177 | 0.9084 |
| Improved SVM | 1848.5441s | 0.9159 | 0.9132 |


## Results
Based on the metrics above, I observed that the Decision Tree has the faster training time compared to the rest of the models, followed by KNN, SVM and Logistic Regression. The KNN and SVM training time 
is a little bit skewed due to me not adding the time variables to track the time. In reality, it would have been DT > KNN > LG > SVM. Looking at the charts above, the models have shown good accuracy from 
the chosen features and params from the gridsearchcv. All of the models used had shown similar Accuracy for both traininig and test.

## Conclusion

I found that the Decision tree model had the faster training time while maintaining a good Accuracy score compared to the other models. Decision tree model is a greedy algorithm which makes locally optimal
decisions rather than globally optimal decisions. This makes the model less computationally intensive. Future improvements would be to better fine tune the parameters to get better results to further enhance
accuracy.

