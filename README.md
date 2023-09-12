# Comparative Analysis Report


The detailed comparative analysis of the six classifiers based on their performance with both `MinMaxScaler` and `StandardScaler`. The analysis highlights that `StandardScaler` performed better in terms of accuracy, with `Logistic Regression` achieving the highest accuracy for `MinMaxScaler` and `Gradient Boosting` for `StandardScaler`.

### Dataset Description:

The dataset used for this analysis contains a set of features used to predict a binary target variable (`diagnosis`), making it a classification problem.


### Data Preprocessing:

The dataset underwent preprocessing, including encoding categorical variables (mapping `'B'` to `0` and `'M'` to `1`) and scaling features using both `MinMaxScaler` and `StandardScaler`. The data was split into training and testing sets.


### Evaluation Metrics:

Four evaluation metrics were used to assess classifier performance: Accuracy, Precision, Recall, and F1-Score. These metrics provide a comprehensive view of classifier performance.


### Classifier Comparison:

#### MinMax Scaled Data:

1. Logistic Regression:

    - Achieved the highest accuracy of `0.94` among `MinMaxScaled` classifiers.
    
    - Balanced `Precision` and a wonderfull `Recall` score`, indicating good overall performance.
    
    - `F1-Score` of `0.92` reflects a harmonious balance between `precision` and `recall`.
    

2. Random Forest:    
    
    - Achieved an `accuracy` of `0.90`, demonstrating strong performance.    
    
    - High `precision` (`0.794`) and `recall` (`1.0`) scores contribute to a high `F1-Score` of `0.92`.


3. Support Vector Machine (SVM):

    - Achieved an `accuracy` of `0.91`, performing well.
    
    - Balanced `precision` and `recall` scores resulted in an `F1-Score` of `0.89`.

4. Decision Tree:

    - Achieved the lowest accuracy of `0.77` among `MinMaxScaled` classifiers.
    
    - While `precision` (`0.72`) and `recall` (`0.98`) scores are relatively balanced, there is room for improvement in overall accuracy.

#### StandardScaler Scaled Data:

1. Logistic Regression:
    
    - Achieved a high `accuracy` of `0.958`, surpassing its performance with `MinMaxScaler`.
    
    - Balanced `precision` and `recall` scores resulted in an `F1-Score` of `0.944`.


2. Random Forest:
    
    - Achieved an `accuracy` of `0.951`, indicating strong performance with `StandardScaler`.
    
    - High `precision` (`0.911`) and `recall` (`0.962`) scores contribute to a high F1-Score of 0.958.


3. Support Vector Machine (SVM):
    
    - Achieved an `accuracy` of `0.965`, performing similarly to `Random Forest`.
    
    - Balanced `precision` and `recall` scores resulted in an F1-Score of `0.952`.


4. Decision Tree:
    
    - Achieved the lowest `accuracy` of `0.895` among `StandardScaler` scaled classifiers.
    
    - `Precision` (`0.797`) and `recall` (`0.895`) scores are relatively balanced, but there is room for improvement in overall accuracy.


5. Gradient Boosting:
    
    - Achieved the highest `accuracy` of `0.972` among `StandardScaler` scaled classifiers.
    
    - High `precision` (`0.930`) and `recall` (`1.00`) scores resulted in an F1-Score of `0.964`, demonstrating outstanding performance.


### Hyperparameter Tuning with GridSearchCV:

`GridSearchCV` was applied to tune the hyperparameters of the six classifiers: `Logistic Regression`, `Random Forest`, `Support Vector Machine (SVM)`, `Decision Tree`, `Gradient Boosting`, and `K-Nearest Neighbors (KNN)`.
The goal was to find the best combination of hyperparameters that would result in improved `training and testing accuracies`.


### Results After Hyperparameter Tuning:

#### Training Accuracies:

1. Logistic Regression:

    Achieved an impressive training accuracy of `0.983` after hyperparameter tuning.


2. Random Forest:

    `Training accuracy` improved significantly and achieved `0.96`.


3. Support Vector Machine (SVM):
    
    Achieved a `training accuracy` of `0.98`, matching `Logistic Regression` as the highest.


#### Testing Accuracies:

1. Decision Tree:

    Achieved a `testing accuracy` of `0.972` after hyperparameter tuning.


2. Gradient Boosting:

    Achieved a `testing accuracy` of `0.980`, matching `SVM` as the highest.


3. K-Nearest Neighbors (KNN):

    The lowest `testing accuracy` after hyperparameter tuning is achieved is `0.944` the `K-Nearest Neighbors`.


### Feature Importance:

The most important features for both the StandardScaler as well as the MinMaxScaler are `perimeter_worst`, `concave_points_worst`, `radius_worst`, `area_worst`, and `concave_points_mean`. These are those distinctive features which really affects the classification of a cell being `Benign` or `Malignant`.


### Conclusion:

- `StandardScaler` consistently outperformed `MinMaxScaler` for all classifiers, with higher accuracy values.


- Among MinMaxScaled classifiers, `Logistic Regression` achieved the `highest accuracy`, while `Decision Tree` had the `lowest accuracy`.


- Among `StandardScaler` scaled classifiers, `Gradient Boosting` achieved the `highest accuracy`, while `Decision Tree` had the `lowest accuracy`.


- `Gradient Boosting` with `StandardScaler` scaling stood out as the best-performing classifier with an `accuracy` of `0.972` and a well-balanced `F1-Score`.


- The choice of scaling method and classifier should be made based on the specific requirements and trade-offs in `precision`, `recall`, and `F1-Score` for the given classification problem.


- Hyperparameter tuning using `GridSearchCV` had a positive impact on the `training and testing accuracies` of the classifiers.


- `Logistic Regression` and `SVM` achieved the highest `training accuracies` of `0.98`, demonstrating their ability to fit the training data well.


- `Gradient Boosting` and `Decision Tree` achieved the highest `testing accuracies` of `0.98` and `0.97` respectively, indicating their strong generalization capabilities.


- The choice of the best classifier should consider both training and testing accuracies and their suitability for the specific task, as well as potential trade-offs between other evaluation metrics such as `precision` and `recall`.
