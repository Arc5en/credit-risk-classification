 # Module 12 Report Template

## Overview of the Analysis

In this section, describe the analysis you completed for the machine learning models used in this Challenge. This might include:

* Explain the purpose of the analysis.
* Explain what financial information the data was on, and what you needed to predict.
* Provide basic information about the variables you were trying to predict (e.g., `value_counts`).
* Describe the stages of the machine learning process you went through as part of this analysis.
* Briefly touch on any methods you used (e.g., `LogisticRegression`, or any resampling method).

The purpose of this analysis is to utilze a model to predict the type of loan that a borrower may have, whether the loan is healthy or high-risk based on their credit history. We utlized the loan's size and interest rate alongside more information about the borrower. This includes the borrower's income, debt to income ratio, number of accounts, number of derogatory marks, and total debt. With this model, I wanted to predict which borrowers were more likely to take out a healthy loan (i.e. have good credit) and which borrowers would take out a high-risk loan (i.e. have bad credit). I first had to split the data I currently had into training and testing sets for the model to prepare the model for machine learning via supervised learning. Then I created a logistic regression model with the unmodified data, where I realized that an overwhelming majority of loans were healthy. In a new sample, I compensated for the low count of high-risk loans with the reandom over sampler which increased the quantity of high-risk loans in the dataset used. The model also used logistic regression on the new sample to predict the loans as healthy and high-risk.

## Results

Using bulleted lists, describe the balanced accuracy scores and the precision and recall scores of all machine learning models.

* Machine Learning Model 1:
  * Model 1's accuracy was ~99%. 
  * For healthy loans, it had a precision of 100% and a recall of 99%, making this model a strong predictor of healthy loans. 
  * For high-risk loans, it had a precision of 84% and a recall of 99%, making this model a slightly weaker, but still good predictor of high-risk loans.



* Machine Learning Model 2:
  * Model 2's accuracy was ~99%. 
  * For healthy loans, it had a precision of 100% and a recall of 99%, making this model a strong predictor of healthy loans. 
  * For high-risk loans, it had a precision of 85% and a recall of 91%, making this model a slightly weaker, but still good predictor of high-risk loans.

## Summary

Summarize the results of the machine learning models, and include a recommendation on the model to use, if any. For example:
* Which one seems to perform best? How do you know it performs best?
* Does performance depend on the problem we are trying to solve? (For example, is it more important to predict the `1`'s, or predict the `0`'s? )

If you do not recommend any of the models, please justify your reasoning.
Both Model 1 and Model 2 had very similar scores in regards to their predictions. It would be difficult to notice a difference in their capabilities to predict borrowers' credibilities if looking at a small sample.
The model I would recommend to predict the credibility of loan borrowers is Model 2. Most scores are very similar between the two models except for their recall scores of high-risk loans, where Model 2 has an edge. A higher recall score indicates a higher rate of correctly labelling a case of a high-risk loan as a prediction as such. In this case, it is important that we predict the high-risk loans since reducing their occurrences would be ideal for both the borrower and the loaner financially.
