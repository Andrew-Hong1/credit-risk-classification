# Module 12 Report Template

## Overview of the Analysis

In this section, describe the analysis you completed for the machine learning models used in this Challenge. This might include:

* Explain the purpose of the analysis.
* Explain what financial information the data was on, and what you needed to predict.
* Provide basic information about the variables you were trying to predict (e.g., `value_counts`).
* Describe the stages of the machine learning process you went through as part of this analysis.
* Briefly touch on any methods you used (e.g., `LogisticRegression`, or any resampling method).


  * The purpose of analysis is to use logistic regression to predict whether or not a loan status would be healthy or high-risk based off of the data provided.
  * The financial information was based off individuals and their loans. This included what their loan size was, their interest rates, the borrower income, the debt_to_income, number of accounts,
    derogatory marks, and total debt. Using this information, the model could predict an individual's loan status.
  * The variable we wantedd to predict was the loan status. The variables were either 0 or 1. 0 meant a healthy loan while 1 was a high-risk loan. Using value_counts, we can see that there are about 75000 healthy  
    loans and 2500 high-risk loans, so about 3% of the loans are at-risk.
  * The first stage was to load the data into a pandas dataframe.
    We then separated the information between y(labels) and x(features). We set the loan status as y and every other column as x. We then reviewed this information and used value_counts to count each label.
    Using train_test_split, we split the data into training and testing subsets. We do this in order to fit the data into the logistic regression model.
    We then import the logistic regression model and fit the data into it, as described above.
    Using the logistic regression model, we can then make predictions of what the loan statuses would be.
    We review the accuracy score using balanced_accuracy_score, which comes out to 95%.
    We then create a confusion matrix to determine the number of true positives, false positives, true negatives, and false negatives. Since very few false positives and false negatives exist, we can see that the information so far is accurate precise.
    Lastly, we review the classification report, which gives us the precision and recall values for each loan status as well as the accuracy score. We discover that the precision and recall all have high scores, so the model is reliable.
  * Logistic regression is a method that allows us to predict continuous values. Since we have a large dataset, we can use this to determine the trends that the data presents and use those trends to predict what
    the loan statuses of newer individuals would be if they were to be entered into the dataset.


## Results

Using bulleted lists, describe the balanced accuracy scores and the precision and recall scores of all machine learning models.

* Machine Learning Model 1:
  * Description of Model 1 Accuracy, Precision, and Recall scores.
  * Accuracy Score: 95%
  * Precision Scores: 100% for healthy loan statuses, 85% for at risk loan statuses.
  * Recall Scores: 99% for healthy loan statuses, 91% for at risk loan statuses


* Machine Learning Model 2:
  * Description of Model 2 Accuracy, Precision, and Recall scores.
    * Description of Model 1 Accuracy, Precision, and Recall scores.
    * Accuracy Score: 95%
    * Precision Scores: 100% for healthy loan statuses, 85% for at risk loan statuses.
    * Recall Scores: 99% for healthy loan statuses, 91% for at risk loan statuses

## Summary

Summarize the results of the machine learning models, and include a recommendation on the model to use, if any. For example:
* Which one seems to perform best? How do you know it performs best?
* Does performance depend on the problem we are trying to solve? (For example, is it more important to predict the `1`'s, or predict the `0`'s? )

If you do not recommend any of the models, please justify your reasoning.

 * From the results, both models perform roughly the same. We can review the confusion matrix and the classification report to determine the precision and recall rates for each loan status, which helps us determine the reliablity of the data. The confusion matrix is useful because we can determine the number of false positives and false negatives. If the rate of false positives and false negatives are low, then we can determine that the model is reliable. The classification report shows us the precision/recall rates for each loan status. The prescision rates show us the ratio of correctly predicted positive observations to total predicited positive observations, while the recall rate shows us the ratio of correctly predicted positive observations to all predicted observations. Since the precision and recall ratios were high for both statuses, we can determine the model is reliable.
 * The performance can vary based on if you are trying to predict high-risk or healthy loan statuses. In general, it is highly important not to mislabel someone as being high-risk if they aren't as it can heavily impact them. This is the same for medical problems, as you want to be extremely careful in not misdiagnosing a disease for someone.