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
    - Inspect the target variable
    - Identify the unique number of values
    - Check if the df has NaN values and rows with missing values
    - Plot box, violin and histogram plots to check all the numerical features (Distributions and Outliers)
  
<p align="center">
<image src="Notebook/images/1.jpg"/>
</p>
  
  - **Data preparation and preprocessing:**
    - Drop some feaures (Explained in the notebook)
    - Define X and Y
    - Split the data into train and test data: train_test_split (sklearn.model_selection)
    
  - **Superviced Machine Learning Algorithms:**
    - Compare several models, just to check how each of them works.
    - To check them, the main steps have been:
        - Pipeline building
        - Cross validation with default hyperparameters
        - Hyperparameter tuning
        - Cross validation with the best hyperparameters
        - Confusion matrix display
 
### Logistic Regression
 
<p align="center">
<image src="Notebook/images/2.png"/>
</p>
 
### Decision Tree

<p align="center">
<image src="Notebook/images/3.png"/>
</p>

### Random Forest

<p align="center">
<image src="Notebook/images/4.png"/>
</p>

### Support Vector Machine (SVM)

<p align="center">
<image src="Notebook/images/5.png"/>
</p>

### K - Nearest Neighbors (KNN)

<p align="center">
<image src="Notebook/images/6.png"/>
</p>

### XGBoost 

<p align="center">
<image src="Notebook/images/7.png"/>
</p>

  - **Evaluation and comparision of all the models:**
    - The best predictive model is XGBoost, that's why we are going to continue working just with this one.
 
<p align="center">
<image src="Notebook/images/8.png"/>
</p> 
 
   - SHAP: This tool decomposes a model prediction such that it’s a linear sum of individual contributions of features (additive feature attribution techniques). This give us the capacity to "understand" how the model is working, which allows us to draw conclusions.

### Global Interpretation - Feature Importance Globally

<p align="center">
<image src="Notebook/images/9.jpg"/>
</p>

### Local Interpretations

<p align="center">
<image src="Notebook/images/10.jpg"/>
</p>

### Partial Dependence 
This one is not really usefull because the features data have been transform.

<p align="center">
<image src="Notebook/images/11.jpg"/>
</p>
