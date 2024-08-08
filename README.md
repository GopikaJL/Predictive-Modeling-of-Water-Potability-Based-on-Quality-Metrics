# Predictive-Modeling-of-Water-Potability-Based-on-Quality-Metrics
# Water Potability Classification Project

## Overview

Safe drinking water is essential for all forms of life and public health. The United Nations (UN) and various countries have recognized access to safe drinking water as a fundamental human right. This project aims to develop a model to determine whether water samples from different water bodies are safe for human consumption.

## Problem Statement

Given a dataset with water quality metrics for 3,276 different water bodies, the task is to build a classification model to predict whether the water sample is potable (fit for human consumption) or not. The dataset includes various attributes related to water quality:

- **pH**: Indicates the acidic or alkaline condition of the water. WHO recommends a pH range of 6.5 to 8.5.
- **Hardness**: Caused by calcium and magnesium salts dissolved in water.
- **Solids**: Total Dissolved Solids (TDS) measure the concentration of dissolved minerals.
- **Chloramines**: Disinfectants used in water treatment. Safe levels are up to 4 mg/L.
- **Sulfate**: Naturally occurring in minerals, soil, and rocks. Typical freshwater concentration ranges from 3 to 30 mg/L.
- **Conductivity**: Measures the water's ability to conduct electric current. WHO recommends a maximum of 400 μS/cm.
- **Organic Carbon**: Measures the total amount of carbon in organic compounds in water.
- **Trihalomethanes**: Chemicals formed in chlorinated water. Levels up to 80 ppm are considered safe.
- **Turbidity**: Measures the amount of solid matter in suspension. WHO recommends a maximum of 5.00 NTU.

**Potability**: The target variable indicating whether the water is safe for consumption (1) or not (0).

## Dataset

- **Dataset Link**: [Water Potability Dataset](https://s3-whjr-v2-prod-bucket.whjr.online/69e55114-dbd8-46c8-9c0a-4bdf19008d79.csv)
- **Dataset Credits**: [Kaggle Dataset](https://www.kaggle.com/adityakadiwal/water-potability)

## Steps and Methodology

1. **Exploratory Data Analysis (EDA) and Data Preparation**
   - Conducted an initial exploration of the dataset.
   - Visualized the distribution of the target classes using count plots.
   - Preprocessed the data to handle missing values and normalize features.

2. **Handling Class Imbalance**
   - Analyzed class distribution to identify imbalances between potable (1) and non-potable (0) classes.
   - Implemented resampling techniques to address the class imbalance:
     - **Random Undersampling**
     - **Random Oversampling**
     - **Synthetic Minority Oversampling Technique (SMOTE)**

3. **Model Building and Evaluation**
   - Built and evaluated different classification models:
     - k-Nearest Neighbors (kNN)
     - Support Vector Classifier (SVC)
     - Random Forest Classifier
     - Decision Tree Classifier
   - Compared the performance of models using various evaluation metrics, including accuracy and F1-score.

4. **Results and Insights**
   - **kNN Classifier**: Performed well after applying resampling techniques, with the best performance observed using random undersampling.
   - **SVC**: Showed good performance with an unbalanced dataset but generally had lower accuracy compared to Random Forest.
   - **Random Forest**: Outperformed SVC and Decision Tree but was complex to tune.
   - **Decision Tree**: Offered less accuracy compared to other models.

5. **Conclusions**
   - Simpler models like kNN and Logistic Regression should be tried first.
   - Complex models like Random Forest and SVC may offer better results but require careful hyperparameter tuning to avoid overfitting.
   - Resampling techniques are crucial for improving model performance on imbalanced datasets.

## Final Results

The project demonstrated that random undersampling improved the F1-score for the minority class (potable water) significantly compared to other resampling techniques. The SVC model provided reliable performance with an unbalanced dataset but was outperformed by Random Forest in overall accuracy.

