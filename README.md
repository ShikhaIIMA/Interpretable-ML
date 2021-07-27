# Interpretable-ML
This repository will house the materials I used while completing the guided project on Coursera on Interpretable Machine Learning Applications Part 1

Link - (https://www.coursera.org/projects/interpretable-machine-learning-applications-part-1)

The Python code uses the ELI5 library that provides explainability frameworks for black-box models. The Permutation Importance feature is used to provide the most explainable features for decision tree and random forests. 

## Permutation Feature Importance
# Need for feature importance measures
In prediction problems, not all features have equal importance. Certain features are more instrumental in determining the value of the outcome variable. In contexts of use of machine learning models for decision making, an inight into which features are more important for predictions helps to increase the interpretability and trustworthiness of the model.

# Intuition behind permutation importance
Shuffling more important features is akin to introducing noise in the variable that the model relies heavily on for prediction on unseen data. A strong predictor when shuffled will cause more decrease in predictive accuracy as compared to a case where a weak predictor is shuffled. The Mean Deacrease in Accuracy (MDA) gives a measure of how important a certain feature is for the prediction task.


Obtaining the permuation importance score involves the following steps:
1. Train the model on training data of predictors and associated labels. 
2. In the test data, shuffle each predictor one at a time and use the model trained in step 1 for predictions and note the decrease in accuracy with respect to the 'no shuffling' case.
3. Repeat step 2 for multiple shuffling arrangements of the same predictor.
4. Repeat step 2 and 3 for each predictor present in predictor set.


**References**
1. [Kaggle] (https://www.kaggle.com/dansbecker/permutation-importance)
2. https://eli5.readthedocs.io/en/latest/blackbox/permutation_importance.html
