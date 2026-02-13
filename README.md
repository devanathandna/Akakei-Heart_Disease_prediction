# Heart Disease Prediction Project

This project focuses on building a machine learning model to predict the presence of heart disease based on a set of patient attributes. The primary goal is to identify the key factors that contribute to a positive diagnosis and create an accurate predictive model.

The analysis and modeling are performed in the `Notebooks/Heart_disease.ipynb` Jupyter Notebook.

## Feature Selection

To build a robust and efficient model, a feature selection process was undertaken to identify the most influential attributes. This process helps in reducing model complexity, improving training speed, and potentially increasing prediction accuracy by focusing on the most relevant data.

The selection was primarily guided by two key analyses:

1.  **Correlation Analysis**: A correlation matrix was generated to examine the relationships between all the features and the target variable (`condition`). Features that showed a strong positive or negative correlation with the target were considered important candidates.

2.  **Feature Importance from Random Forest**: A Random Forest Classifier was trained on the full dataset. The `feature_importances_` attribute of the trained model was then used to rank features based on their contribution to the model's predictive power.

### Key Features Chosen

Based on the analysis, the following features were identified as the most important for predicting heart disease:

*   **`thal` (Thalassemia)**: This feature consistently showed up as one of the most significant predictors in the Random Forest feature importance plot. Thalassemia is a blood disorder, and certain types are strongly linked to heart complications.
*   **`thalach` (Maximum Heart Rate Achieved)**: The analysis revealed a strong negative correlation between the maximum heart rate achieved during exercise and the presence of heart disease. Lower maximum heart rates were associated with a higher likelihood of heart disease.
*   **`cp` (Chest Pain Type)**: Different types of chest pain are critical indicators of heart problems. This feature had a high correlation with the final condition.
*   **`exang` (Exercise Induced Angina)**: The presence of angina (chest pain) induced by exercise is a classic symptom of heart disease, making it a crucial predictive feature.
*   **`oldpeak` (ST Depression Induced by Exercise)**: This is a measurement from an ECG that indicates stress on the heart during exercise. It was found to be a significant predictor.

By focusing on these key features, we can build a more interpretable and efficient model without a significant loss in accuracy, as demonstrated by the model performance comparisons in the notebook.

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
