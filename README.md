# Credit_Risk_Analysis

## Purpose

The purpose of this analysis is to use machine learning models to determine which model can best predict credit risk. Using credit card  data from LendingClub, I'll evaluate the performance of 6 models: oversampling, undersampling, SMOTE, SMOTEENN, Random Forest Classifier and Easy Ensemble Classifier.

## Results

Below are the results of 6 structured machine learning models. For each, I will assess the accuracy score, precision and recall scores. The combination of each of these scores will identify the best model.

Accuracy score is the number of correct predictions divided by the total number of predictions.

    Accuracy = (TP + TN) / (TP + TN + FP + FN)

Precision determines how accurate the positive predictions are.

    Precision = TP/(TP + FP)

Recall is the portion of samples from a class which are correctly predicted by the model.

    Recall = TP/(TP + FN)

### Oversampling

- Oversampling models add records to the minority group to balance the dataset to (hopefully) remove bias in the training set.

#### RandomOverSampler

![NaiveRandomOversampling](https://github.com/krockway/Credit_Risk_Analysis/blob/main/Images/NaiveRandomOversampling.png)

- This RandomOverSampler was 63.9% accurate, for low risk loans it was 100% precise and 69% sensitive, and for high risk loans it was 1% precise and 59% sensitive.

#### SMOTE

![SMOTEOversampling](https://github.com/krockway/Credit_Risk_Analysis/blob/main/Images/SMOTEOversampling.png)

- This SMOTE was xxx% accurate, for low risk loans it was xxx% precise and xxx% sensitive, and for high risk loans it was xxx% precise and xxx% sensitive.

### Undersampling

#### ClusterCentroids

![Undersampling](https://github.com/krockway/Credit_Risk_Analysis/blob/main/Images/Undersampling.png)
This XXXX was xxx% accurate, for low risk loans it was xxx% precise and xxx% sensitive, and for high risk loans it was xxx% precise and xxx% sensitive.

### Combination

#### SMOTEENN

![SMOTEENN](https://github.com/krockway/Credit_Risk_Analysis/blob/main/Images/SMOTEENN.png)
This XXXX was xxx% accurate, for low risk loans it was xxx% precise and xxx% sensitive, and for high risk loans it was xxx% precise and xxx% sensitive.

### BalancedRandomForestClassifier

![BalancedRandomForestClassifier](https://github.com/krockway/Credit_Risk_Analysis/blob/main/Images/BalancedRandomForestClassifier.png)
This XXXX was xxx% accurate, for low risk loans it was xxx% precise and xxx% sensitive, and for high risk loans it was xxx% precise and xxx% sensitive.

### EasyEnsembleClassifier

![EasyEnsembleAdaBoostClassifier](https://github.com/krockway/Credit_Risk_Analysis/blob/main/Images/EasyEnsembleAdaBoostClassifier.png)
This XXXX was xxx% accurate, for low risk loans it was xxx% precise and xxx% sensitive, and for high risk loans it was xxx% precise and xxx% sensitive.

## Summary

Summarize the results of the machine learning models, and include a recommendation on the model to use, if any. If you do not recommend any of the models, justify your reasoning.

From the support column, I can see that the high_risk figures are significantly outnumbered (87 vs 17,118).