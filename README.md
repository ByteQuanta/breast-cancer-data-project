# Breast Cancer Data Project
Breast Cancer Classification using Decision Tree & Random Forest

# Data Source
# This data was obtained from https://www.kaggle.com/datasets/yasserh/breast-cancer-dataset.

## 🚀 Project Goal
The goal of this project is to achieve the highest possible model performance using the dataset. To do this, we first identify the most effective hyperparameter optimization method, and then apply it to both Decision Tree and Random Forest algorithms to obtain the best results.
## 📊 Project Steps and Methods
This project follows a structured workflow to achieve the **best possible model performance** and provide **model interpretability**. The main steps and methods used are:


#### ✅ What Was Done in This Step

**Data Preparation & EDA**
- Loaded the Breast Cancer Wisconsin (Diagnostic) dataset.
- Dropped unnecessary columns (`id`) and encoded the `diagnosis` column (`M=1`, `B=0`).
- Performed exploratory data analysis (EDA) using `ydata_profiling` to generate a comprehensive report.

**Hyperparameter Optimization**
- Compared and evaluated three hyperparameter optimization methods:
  - GridSearchCV
  - RandomizedSearchCV
  - Optuna

**Model Training**
- Applied the best hyperparameters to Decision Tree and Random Forest models.
- Used a Pipeline including RobustScaler and LDA.

**Model Evaluation**
- Evaluated models on the test set using F1 Score, Accuracy, and ROC-AUC Score.
- Performed Stratified 10-Fold CV and compared mean ± std across folds.

**Model Explainability & Visualization**
- Plotted ROC and Precision-Recall curves
- Plotted Decision Tree (after LDA)
- Visualized Random Forest Feature Importance



#### ⏳ What Was Not Done in This Step
- Additional feature engineering (e.g., polynomial features, interaction terms).
- Handling missing values (not necessary for this dataset).
- Outlier analysis was not performed because removing potential outliers could result in significant loss of important information in this medical dataset.
- Data augmentation or synthetic data generation was not performed; class imbalance was handled using `class_weight='balanced'` during model training.
- Feature selection was not performed manually because LDA was used for dimensionality reduction.




