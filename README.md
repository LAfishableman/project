# Heart Attack Prediction Model
## Problem Statement
The goal of this project is to use a supervised machine learning model to predict the outcome of a heart attack (positive or negative) based on the features of a medical dataset (age, gender, heart rate, systolic blood pressure, diastolic blood pressure, blood glucose, CK-MB, and troponin). The dataset contains records of patients with binary labels indicating whether a heart attack has occurred.
## Methods
### Data Preprocessing:
Load and clean the dataset, removing outliers (e.g., heart rate > 200, blood glucose > 500).  
Convert the "Result" column to binary (positive as 1, negative as 0).  
Use StandardScaler to standardize numerical features.  
### Model Selection:
Choose a random forest classifier for its robustness and ability to handle nonlinear relationships.  
Optimize hyperparameters (e.g., number of trees, maximum depth) through grid search.  
### Evaluation:
Split the data into 80% training set and 20% test set, using stratified sampling to maintain label proportions.  
Evaluate the model using accuracy, precision, recall, F1 score, and ROC-AUC, with a focus on recall to reduce false negatives.  
Visualize results using confusion matrix, feature importance plots, and ROC curves.  
## Key Findings
### Feature Importance:
Troponin and CK-MB are the most important predictors as they are direct biomarkers of heart muscle damage. Age and blood pressure also contribute significantly.
### Data Quality: 
Identify and remove outliers (e.g., heart rate 1111) to improve model reliability.
### Model Performance:
Achieve high recall of approximately 0.96, prioritizing the reduction of missed diagnoses.  
ROC-AUC score of approximately 0.97, indicating good discriminatory ability.  
Confusion matrix shows fewer false negatives, which is crucial for medical applications.  
### Challenges: 
The dataset may have class imbalance (more positive cases), which could affect results. Outlier thresholds need validation by domain experts.

## Model Performance

**Accuracy:** Approximately 0.97.  
**Precision:** Approximately 0.98, indicating reliable positive predictions.  
**Recall:** Approximately 0.96, ensuring detection of most positive cases.  
**F1 Score:** Approximately 0.97, balancing precision and recall.  
**ROC-AUC:** Approximately 0.97, demonstrating excellent model performance.  
**Cross-Validation:** 5-fold cross-validation recall average of approximately 0.98, validating model robustness.  

## Potential Improvements
**Advanced Models:** Try XGBoost or gradient boosting models to further improve performance.  
**Feature Engineering:** Add interaction features (e.g., systolic/diastolic blood pressure ratio) or apply log transformations to CK-MB and troponin to handle skewed distributions.  
**Class Imbalance:** Apply techniques like SMOTE if necessary to handle imbalanced data.  
**Domain Validation:** Collaborate with medical professionals to optimize outlier thresholds and validate model predictions.  
**Deployment:** Integrate the model into a clinical decision support system, providing probability outputs to enhance interpretability.  

## Running the Method
Install dependencies: pip install pandas /numpy /scikit-learn /matplotlib /seaborn.  
Run the provided Jupyter Notebook file to preprocess data, train the model, and visualize results.  

## Conclusion
The random forest model effectively predicts heart attack outcomes, with troponin and CK-MB being key predictors. High recall ensures minimal missed diagnoses, which is crucial for medical applications. Future work should focus on addressing class imbalance, optimizing feature engineering, and validating with clinical experts.
