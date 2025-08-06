# Group Project - Dados e Aprendizagem Automática


## Overview

This project was developed as part of the “Dados e Aprendizagem Automática” (Data and Machine Learning) course. It involved two major analytical tasks: one focused on a competition dataset provided by instructors related to solar energy and meteorological data and another on a group-selected dataset related to diabetes prediction. Both tasks followed the CRISP-DM methodology and involved extensive data preprocessing, feature engineering, model training and evaluation.

---

## Learning Objectives

- Apply machine learning techniques to real-world problems.
- Explore, preprocess and prepare data for modeling.
- Train and optimize models for classification and regression.
- Evaluate models using accuracy, F1-score and confusion matrices.
- Understand model limitations and select appropriate techniques for different problems.

---

## Task 1: Competition Dataset – Solar Energy Prediction

### Dataset Description

Merged meteorological and energy datasets to create a single training and testing set. The data included features such as:

**Energy Dataset Features:**
- Data, Hora (timestamp)
- Normal (kWh), Horário Económico (kWh)
- Auto consumo (kWh), Injeção na rede (kWh)

**Meteorological Dataset Features:**
- Temperature, humidity, wind speed, atmospheric pressure
- Weather description, cloudiness and rainfall

### Data Treatment & Analysis

- Categorical to numerical transformations (e.g., weather description).
- Decomposition of date into year, month, day.
- Outlier detection and management.
- NaN handling (e.g., rainfall filled with 0).
- Feature elimination for redundant or missing data columns.

### Models Used

- **Decision Tree & Random Forest:** Achieved ~89.6% accuracy on public data using Random Forest.
- **Logistic Regression:** ~86% accuracy with ‘newton-cg’ solver.
- **Neural Networks:** ~86.5% accuracy using Keras with MinMax scaling.
- **Support Vector Machine:** ~86% accuracy, used K-Fold cross-validation.
- **XGBoost:** Best model with ~89.6% public accuracy and 87.4% private accuracy.

### Key Considerations

- CRISP-DM allowed iterative refinement of models.
- Tradeoff between outlier removal and model accuracy.
- Random Forest and XGBoost yielded superior results.

---

## Task 2: Group Dataset – Diabetes Prediction

### Dataset Overview

Selected from Kaggle, this dataset included 70,682 entries and 17 features plus a binary target indicating the presence of diabetes.

**Features Included:**
- Demographics: Age, Gender
- Health metrics: BMI, Physical Health, Mental Health, General Health
- Lifestyle: Smoking, Alcohol, Fruits/Vegetables consumption, Physical Activity
- Pre-existing conditions: Stroke, Heart Disease, High Cholesterol, High Blood Pressure

### Data Analysis

- Count and distribution visualizations (pie charts, histograms).
- Outlier detection using boxplots (e.g., BMI).
- Feature analysis relative to diabetes presence.

### Data Preparation

- Removal of duplicates.
- Feature binning for BMI, mental and physical health.
- Min-Max normalization.
- Addressed class imbalance via upsampling of minority class.

### Models Applied

- **Decision Tree & Random Forest:** Best accuracy ~72% with Random Forest.
- **Logistic Regression:** Consistent ~74% accuracy across solvers.
- **SVM:** Used GridSearch and cross-validation; ~74% accuracy.
- **Neural Networks:** ~69.7% accuracy after tuning with GridSearch.
- **XGBoost:** Achieved ~73% accuracy; selected as best for this dataset.

---

## Technologies Used

- Python (Jupyter Notebooks)
- Pandas, NumPy for data manipulation
- Scikit-learn, XGBoost, Keras
- Matplotlib, Seaborn for visualization
