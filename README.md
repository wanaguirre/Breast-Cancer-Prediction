This repository is just to show ans teach some of the Supervised ML models used to solve Classification problems.

# Breast-Cancer-Prediction

In this repository I'll work with ML models to classify is a cell nuclei characteristics provided for the experts could tell us if a breas cancer is malignant (M) or benign (B).

This classification will be done through the use of different Machine Learning models, such as the following:
- Logistic Regression
- Decision Tree
- Random Forest
- Support Vector Machine

Also implementing techniques and tools such as, the Hyperparameter Tuning of this models and the feature interpretation using SHAP.

---

### Background:

The main characteristics have been extracted from many samples of nuclei, cells, and tumors found in the breasts of a large number of patients.

These characteristics are intended to predict, without the need for a more expensive study, whether the tumor is malignant or benign.


### Task:

Predict whether the cancerous tumor is malignant or benign, based on certain attributes explained below.


### [Feature Descriptions](https://archive.ics.uci.edu/ml/datasets/Breast+Cancer+Wisconsin+%28Diagnostic%29):

1) ID number
2) Diagnosis (M = malignant, B = benign)

Ten real-valued features are computed for each cell nucleus:

a) radius (mean of distances from center to points on the perimeter)

b) texture (standard deviation of gray-scale values)

c) perimeter

d) area

e) smoothness (local variation in radius lengths)

f) compactness (perimeter^2 / area - 1.0)

g) concavity (severity of concave portions of the contour)

h) concave points (number of concave portions of the contour)

i) symmetry

j) fractal dimension ("coastline approximation" - 1)

---
### Methodology

  - **Data Understanding:** 
    - Check the type of values of each column and shape of the DataFrame 
    - Check if the df has NaN values
    - Plot histograms to check all the numerical features (Distributions and Outliers)
    - Check the number of categories per categorical feature and take a closer look at features with many categories
  
  - **Data preparation and preprocessing:**
    - Drop "duration" feaure (Explained in the notebook)
    - Define X and Y
    - Split the data into train and test data: train_test_split (sklearn.model_selection)
    - Split numerical and categorical features
    - Pipeline: we created pipelines for both the categorical (incl. OneHotEncoder) and the numeric data (incl. StandardScaler) as well as a preprocessor (ColumnTransformer) to combine these two pipelines
    
  - **Superviced Machine Learning Algorithm:**
    - Compare several models, just to check how each of them works.
      - Logistic Regression: Cross validaion with No Penaly, L1 (Lasso) and L2 (Ridge).
      - KNN (K-Nearest Neighbour)
      - Naive Bayes
      - SVM
      - Random Forest
      - AdaBoost
      - XGBoost
      
    Surprisingly the best scoring model was Logistic Regression, and one of the main reasons could be because it was the only one to which Hyperparameter Tuning was applied.
    
    - Feature Importance: 
    
    Trees based models like RandomForest, XGBoost, etc. provide us feature importance based on the training. A very relevant aspect if you want to know more about how each of the features affects.

---

### Future steps:
- Hyperparameter Tuning
- Feature Interpretation (SHAP)
- Provide a conclusion based on what has been learned, about this business problem.
