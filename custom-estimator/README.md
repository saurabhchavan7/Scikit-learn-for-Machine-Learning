## Custom Estimators in Scikit-Learn

### Introduction
In machine learning with scikit-learn, estimators are objects that can learn from data. They encapsulate the fitting of models to data and predicting outcomes for new data points.

### What is an Estimator?
An estimator in scikit-learn is any object that learns from data, identified by the presence of a `fit` method.

### Example of Estimators
In scikit-learn, examples of estimators include:
- **Linear Regression:** Learns coefficients from data.
- **Support Vector Machines (SVM):** Learns decision boundaries from data.
- **Decision Trees:** Learns hierarchical splits in data.

### Types of Estimators
Estimators can be broadly categorized into two types:
- **Predictors:** Estimators that predict outcomes for new data after learning from the training data.
- **Transformers:** Estimators that transform input data in some way after learning from the training data, but do not perform prediction.

### Predictor Example
A common example of a predictor is the `LinearRegression` estimator in scikit-learn, which learns coefficients from the data and predicts target values for new data points using its `predict` method.

### Transformer Example
An example of a transformer is the `StandardScaler` in scikit-learn, which learns statistics from the training data to later scale input data.

### Custom Estimators
Sometimes, the built-in estimators might not meet specific requirements. In such cases, scikit-learn allows creating custom estimators by extending base classes like `BaseEstimator` and implementing required methods such as `fit` for learning from data and optionally `predict` for making predictions.

### Example of Custom Estimator
Will be implementing simple custom estimator to  understand how to construct a custom estimator. We will create a`MostFrequentClassClassifier` custom estimator which learns and predicts the most frequent class from the training data. It extends `BaseEstimator` and `ClassifierMixin`, implementing `fit` to learn from data and `predict` to make predictions based on the most frequent class found during fitting.

## Mixins in scikit-learn

### Definition
Mixins in scikit-learn are classes that provide additional methods and functionalities to estimators.

### Purpose
While base estimators have basic methods like `fit` and `predict`, mixins add extra methods for tasks such as scoring and classification.

### Examples
- **ClassifierMixin**: Adds scoring functions to classifiers.
- **RegressorMixin**: Adds scoring functions to regressors.
- **TransformerMixin**: Adds `fit_transform` method to transformers.