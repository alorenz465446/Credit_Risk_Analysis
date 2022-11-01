# Credit_Risk_Analysis

## Overview

Credit risk is an inherently unbalanced classification problem, as good loans easily outnumber risky loans. Different techniques will be employed to train and evaluate models with unbalanced classes. The client has asked me to use imbalanced-learn and scikit-learn libraries to build and evaluate models using resampling.

Using the credit card credit dataset from LendingClub (peer-to-peer lending services company) I will oversample the data using the RandomOverSampler and SMOTE algorithms, and undersample the data using the ClusterCentroids algorithm. Then, I will use a combinatorial approach of over- and undersampling using the SMOTEENN algorithm. Next, I'll compare two new machine learning models that reduce bias, BalancedRandomForestClassifier and EasyEnsembleClassifier, to predict credit risk. Lastly, I will evaluate the performance of these models and make a written recommendation on whether they should be used to predict credit risk.



### Results
#### Oversampling

Oversampling (naive and SMOTE) **did not** produce a useable model for the prediction of bad loans. </br>
* Naive oversampling resulted in a precision score of 0.03 and recall of 0.82. F1 score of 0.06 reflected a low precision score. </br>
* SMOTE oversampling gave a precision score of 0.04 and a similiar recall of 0.82, and a F1 score of  0.07. </br>
<img width="528" alt="naive oversampling" src="https://user-images.githubusercontent.com/107652317/199300526-22cc6fb3-cb22-4a56-8126-1853e9007164.PNG"> </br>
<img width="514" alt="SMOTE oversampling" src="https://user-images.githubusercontent.com/107652317/199300759-5fca06d8-4a13-43c3-93a1-200686e9ee93.PNG"> </br>

#### Undersampling
Undersampling gave the same poor outcomes, with a precision score of  0.02, recall of 0.88, and F1 score of  0.04. </br>
<img width="505" alt="Undersampling" src="https://user-images.githubusercontent.com/107652317/199300816-5a4f3538-cec4-4fe2-a7dc-18fb38a0c71b.PNG"> </br>


#### Combination (Over & Under)
Combination sampling gave a precision score of 0.02  and recall of 0.88, and a F1 score of 0.04. This mod,el was no better than the other models. </br>
<img width="493" alt="COMBO" src="https://user-images.githubusercontent.com/107652317/199300876-1d4c8df9-e65e-4bbb-a7b7-294a544f1fa1.PNG"> </br>

#### Balanced Random Forest Classifier
The balanced random forest classifier's precision is 0.04. This means that 4 out of 100 loan applications were flagged to be bad loan applications. The model's recall/sensitivity is 0.67 This means that it noticed 67% were bad loan applications. The F1 score was at 0.07. This was due to the other low scores.

#### Easy Ensemble AdaBoost Classifier
The random forest classifier with AdaBoost, while achieving better results, still suffered from inadequate predictive power. Its precision score is 0.09 and its recall 0.92. The F1 score, again, is skewed low at 0.16 by the low precision score.


### Summary

The oversampling models and combination model are insufficient at giving solid predictions. </br>

The random forest classifier (with and w/o AdaBoost) did not reach useable performance. </br>

The performances of both models are insufficient for commercial application.


## Resources 

* Jupyter Notebook
* csv file
