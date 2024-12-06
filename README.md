# Bike Buyers Analysis 🚴💡

This project focuses on data preprocessing techniques to enhance model accuracy in predicting whether a customer will purchase a bike. Below are the key highlights and steps of the project.

---

## Table of Contents 🔍

1. [Overview](#overview)
2. [Data Preprocessing](#data-preprocessing)
3. [Model Evaluation](#model-evaluation)
4. [Model Improvement](#model-improvement)
5. [Key Results](#key-results)
6. [Further Considerations](#further-considerations)

---

## Overview 📃

This notebook uses a dataset of bike buyers with features such as:

- Demographic details
- Income
- Marital status
- Commute distance
- Region

The goal is to create a predictive model that classifies customers based on their likelihood to purchase a bike.

---

## Data Preprocessing ♻️

The following preprocessing steps were applied:

1. **Data Cleaning**:

   - Removed columns with insignificant impact (e.g., `ID`, `Education`).
   - Eliminated duplicate rows.
   - Addressed null values using `SimpleImputer` and `KNNImputer`.

2. **Feature Engineering**:

   - Encoded categorical variables using `OneHotEncoder` and `OrdinalEncoder`.
   - Identified and removed outliers using `Local Outlier Factor (LOF)`.

3. **Scaling**:

   - Applied scaling techniques such as `MinMaxScaler` and `StandardScaler`.

---

## Model Evaluation 📊

Initial modeling involved using a `RandomForestClassifier` evaluated with cross-validation. Key steps include:

1. Dropping redundant features.
2. Encoding the target label.
3. Performing initial scoring based on numerical features.

**Initial Accuracy**: \~64.4%

---

## Model Improvement ⚙️

### Techniques Applied:

1. **Variance Threshold**:

   - Ensured features with sufficient variance were retained.

2. **Feature Selection**:

   - Applied `Recursive Feature Elimination (RFE)` to select the top 75% of features.

3. **Advanced Imputation**:

   - Used frequent value imputations for categorical variables.
   - Leveraged KNN Imputation for numerical columns.

4. **Inclusion of Additional Features**:

   - Revisited the inclusion of the `Education` feature for final evaluations.

### Results:

After applying these steps, accuracy improved from **64.4%** to **70.1%**, representing a **5.7% improvement** in classification performance.

---

## Key Results 🔄

| Methodology                     | Accuracy (%) |
| ------------------------------- | ------------ |
| Initial Model                   | 64.4         |
| With RFE                        | 69.0         |
| With Imputation and `Education` | 70.1         |

---

## Further Considerations 🎨

Potential next steps for model improvement:

- Fine-tune hyperparameters for imputers and classifiers.
- Explore alternative models such as Gradient Boosting or SVM.
- Experiment with additional feature engineering and selection techniques.
- Perform deeper analysis into the relationship between features.

---

## Installation and Setup 🚀

To reproduce the results:

1. Install required libraries:
   ```bash
   pip install pandas numpy scikit-learn matplotlib seaborn
   ```
2. Run the notebook `Trabajo Elina Filatova (en).ipynb` in Jupyter Notebook or VSCode.

---
