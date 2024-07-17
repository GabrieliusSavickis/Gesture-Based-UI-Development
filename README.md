# Gesture-Based UI: Comparative Analysis of Machine Learning Algorithms for Predicting Vehicle Driving Conditions

## Introduction

This repository contains the code and documentation for a machine learning project conducted as part of the Gesture-Based UI module at the university. The project involves a comparative analysis of three machine learning algorithms – Support Vector Machines (SVM), Logistic Regression, and K-Nearest Neighbors (kNN) – to classify vehicle driving conditions using sensor data from two different vehicles.

## Project Brief

The project aimed to:

1. Clean and preprocess the raw dataset sourced from Kaggle.
2. Train and compare three classification algorithms.
3. Evaluate the performance of each classifier using cross-validation and appropriate metrics.

## Dataset

The dataset used in this project is derived from vehicle sensors and is available on Kaggle: [Traffic, Driving Style, and Road Surface Condition](https://www.kaggle.com/datasets/gloseto/traffic-driving-style-road-surface-condition).

- **Vehicles:** Opel Corsa and Peugeot 207
- **Data Points:** Sensor readings over multiple journeys
- **Challenges:** Missing values, numerical representation errors, and class imbalances

## Methodology

### Data Preprocessing

1. **Data Cleaning:** 
   - Converted numeric columns with decimal commas to float format.
   - Used median imputation to handle missing values.

2. **Feature Evaluation:**
   - Visualized sensor readings to examine data distribution.
   - Used Random Forest to rank feature relevance.

3. **Dataset Balancing:**
   - Applied SMOTE (Synthetic Minority Over-sampling Technique) to address class imbalances.

### Classifier Training

Three classifiers were chosen for this study:

1. **Support Vector Machine (SVM):**
   - Configured with a linear kernel for its efficacy in high-dimensional spaces.

2. **Logistic Regression:**
   - Used as a baseline for performance due to its simplicity and interpretability.

3. **K-Nearest Neighbors (kNN):**
   - Selected k=5 to balance accuracy and generalization, avoiding overfitting.

### Experimental Setup

- **Data Split:** 70% training, 30% testing
- **Hyperparameter Tuning:** Utilized GridSearchCV for kNN to find the optimal number of neighbors.
- **Evaluation Metrics:** Precision, recall, and F1-score were used to assess classifier performance.

## Results

- **SVM:** Demonstrated moderate precision and recall.
- **Logistic Regression:** Showed comparable performance to SVM.
- **kNN:** Exhibited superior performance across all metrics, particularly for class 1.

### Visualizations

- **Feature Importance:** Random Forest feature importance visualization.
- **Classification Reports:** Summary of precision, recall, and F1-score for each classifier.
- **ROC Curves:** Receiver Operating Characteristic curves for each classifier with AUC values.

## Conclusion

The kNN classifier, with k=5, was identified as the most effective model, achieving the highest precision, recall, and F1-scores. The use of SMOTE for balancing the dataset and GridSearchCV for hyperparameter tuning were crucial in enhancing the classifiers' performance.

### Future Work

Future research could explore more advanced models, such as deep learning algorithms, to capture complex patterns in high-dimensional data.

## References

1. Ruta, M. "Traffic, Driving Style and Road Surface Condition," 2018. [Online]. Available: [Kaggle Dataset](https://www.kaggle.com/datasets/gloseto/traffic-driving-style-road-surface-condition).
2. Allison, P. D. "Missing Data," SAGE Publications, Inc., 2011.
3. Waskom, M. L. "seaborn: statistical data visualization," Journal of Open Source Software, 2021.
4. Breiman, L. "Random Forest," Machine Learning, vol. 45, no. 1, pp. 5-32, 2001.
5. Chawla, N. V., Bowyer, K. W., Hall, L. O. "Journal of Artificial Intelligence Research," vol. 16, pp. 321-357, 2002.
6. James, G., Witten, D., Hastie, T., Tibshirani, R. "An Introduction to Statistical Learning," Springer New York, 2013.
