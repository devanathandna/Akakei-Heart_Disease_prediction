# Heart Disease Prediction Project

This project focuses on building a machine learning model to predict the presence of heart disease based on a set of patient attributes. The primary goal is to identify the key factors that contribute to a positive diagnosis and create an accurate predictive model.

The analysis and modeling are performed in the `Notebooks/Heart_disease.ipynb` Jupyter Notebook.

## Feature Selection

The most influential features for the model were identified using correlation analysis and the feature importance scores from a Random Forest model. This helps create a more efficient and interpretable model.

### Key Features Chosen

The following features were selected as the most predictive for heart disease:

*   **`thal` (Thalassemia)**: A blood disorder strongly linked to heart complications.
*   **`thalach` (Maximum Heart Rate Achieved)**: Lower maximum heart rates are associated with a higher likelihood of heart disease.
*   **`cp` (Chest Pain Type)**: A critical indicator of heart problems.
*   **`exang` (Exercise Induced Angina)**: A classic symptom of heart disease.
*   **`oldpeak` (ST Depression Induced by Exercise)**: An ECG measurement indicating heart stress.

## Model Performance

Here are the classification reports for the models trained on the dataset.

### Random Forest (with important features)

```
Classification Report:
               precision    recall  f1-score   support

           0       0.77      0.72      0.74        32
           1       0.70      0.75      0.72        28

    accuracy                           0.73        60
   macro avg       0.73      0.73      0.73        60
weighted avg       0.74      0.73      0.73        60
```
**Accuracy:** 0.7333333333333333

### Logistic Regression (with important features)

```
Classification Report:
               precision    recall  f1-score   support

           0       0.74      0.72      0.73        32
           1       0.69      0.71      0.70        28

    accuracy                           0.72        60
   macro avg       0.72      0.72      0.72        60
weighted avg       0.72      0.72      0.72        60
```
**Accuracy:** 0.7166666666666667

### Conclusion

From this we can conclude that:
*   **Random Forest Accuracy:** 0.7333333333333333
*   **Logistic Regression Accuracy:** 0.7166666666666667
