# credit-risk-classification

## Overview of the Analysis

This repository reviews techniques to train and evaluate a model based on loan risk. The dataset represents the historical lending activity from a peer-to-peer lending services company. 
To identify the creditworthiness of borrowers I have trained the Logistic Regression Model on 2 different data: the Original Data and the Resampling Training Data. 

## Results

* Prediction with the Logistic Regression Model using the Original Training Data:
  * Balanced Accuracy Score = 0.944
  * Accuracy level = 0.99
  * Precision and Recall on healthy loans = 1.0
  * Precision and Recall on high-risk loans = 0.87 and 0.89

* Prediction with the Logistic Regression Model using the Resampled Training Data:
  * Balanced Accuracy Score = 0.989
  * Accuracy level = 0.99
  * Precision and Recall on healthy loans = 1.0
  * Precision and Recall on high-risk loans = 0.87 and 0.98
## Summary

The accuracy level in both cases is high, the model prediction is correct in 99% of the cases. But because the classes are very much imbalanced (about 97% vs 3%) - Accuracy is not a very good indicator. The precision on the high-risk loans is much lower than on healthy loans as well as the recall metric. When using the Original Training Data, the Model detected 89% of high-risk loans and the model is 87% correct on flagging the high-risk loans.
The RandomOverSampler balances out the pull of training data (about 83% vs 17%) and the training of Resampled data increases the model performance. The Balance Accuracy Score increases from 0.944 to 0.989. We can also observe the significant improvement in recall metric, this time the model detected 98% of the high-risk loans with the same precision of 87%.

The recall appears to be the important metric in this case the identification of the low repay potential decreases lander's risk.

