# Module 12 Report Template

## Overview of the Analysis

In this section, describe the analysis you completed for the machine learning models used in this Challenge. This might include:

* Explain the purpose of the analysis.

Purpose: To build and evaluate models capable of identifying the creditworthiness of borrowers based on historical lending activity.


* Explain what financial information the data was on, and what you needed to predict.

We used a dataset containing financial information from a peer-to-peer lending services company. The key prediction task was to classify loans into two categories: healthy loans (0) and high-risk loans (1).

* Provide basic information about the variables you were trying to predict (e.g., `value_counts`).

The variable we sought to predict was "loan_status," where a value of 0 indicated a healthy loan and 1 indicated a high-risk loan. We checked the balance of these labels to understand the class distribution.


* Describe the stages of the machine learning process you went through as part of this analysis.

1. Data Preparation: We read the dataset, created feature and label sets, and checked the class balance.
2. Model 1 (Non-Oversampled): We trained a logistic regression model on the original data and evaluated its performance using accuracy, precision, recall, and other metrics.
3. Model 2 (Oversampled): We addressed class imbalance by oversampling the data using the RandomOverSampler and trained a logistic regression model. We then evaluated its performance     similarly.


* Briefly touch on any methods you used (e.g., `LogisticRegression`, or any resampling method).

Utilised LogisticRegression and resampling model namely oversampling

## Results

Using bulleted lists, describe the balanced accuracy scores and the precision and recall scores of all machine learning models.

* Machine Learning Model 1:
  * Description of Model 1 Accuracy, Precision, and Recall scores.

Machine Learning Model 1 (Non-Oversampled):
- Balanced Accuracy: 0.9218124642767772
- Precision for label 0 (healthy loan): 1.00
- Recall for label 0 (healthy loan): 0.99
- Precision for label 1 (high-risk loan): 0.85
- Recall for label 1 (high-risk loan): 0.91



* Machine Learning Model 2:
  * Description of Model 2 Accuracy, Precision, and Recall scores.

Machine Learning Model 2 (Oversampled):
- Balanced Accuracy: 0.9205494133884273
- Precision for label 0 (healthy loan): 1.00
- Recall for label 0 (healthy loan): 0.99
- Precision for label 1 (high-risk loan): 0.85
- Recall for label 1 (high-risk loan): 0.91
  
  
 
## Summary

Summarize the results of the machine learning models, and include a recommendation on the model to use, if any. For example:
* Which one seems to perform best? How do you know it performs best?
* Does performance depend on the problem we are trying to solve? (For example, is it more important to predict the `1`'s, or predict the `0`'s? )

Both Machine Learning Model 1 (Non-Oversampled) and Model 2 (Oversampled) perform remarkably well in predicting healthy loans (0) with high precision and recall. They also have a good balance between precision and recall for high-risk loans (1).

The slight differences in balanced accuracy between the two models are negligible, and both models have similar precision and recall scores. Therefore, the choice between the two models may not significantly impact overall performance.

The choice of model may depend on the specific goals and priorities of the analysis:

Importance of Predicting 0 and 1: 
- If it is crucial to minimize false negatives (high-risk loans incorrectly classified as healthy), Model 1 may be preferred, as it has a slightly higher recall for label 1. However, Model 2 also offers good performance in this regard.
Class Imbalance:
- Model 2 (Oversampled) addresses class imbalance explicitly, which could be advantageous if class balance is a significant concern. It ensures that both healthy and high-risk loans are adequately represented in the training data.


If you do not recommend any of the models, please justify your reasoning.


