# Credit_Risk_Analysis

## Purpose

The purpose of this analysis is to use machine learning models to determine which model can best predict credit risk. Using credit card  data from LendingClub, I'll evaluate the performance of 6 models: oversampling, undersampling, SMOTE, SMOTEENN, Random Forest Classifier and Easy Ensemble Classifier.

## Results

Below are the results of 6 structured machine learning models. For each, I will assess the accuracy score, precision and recall scores. The combination of each of these scores will identify the best model.

Accuracy score is the number of correct predictions divided by the total number of predictions.

    Accuracy = (TP + TN) / (TP + TN + FP + FN)

Precision determines how accurate the positive predictions are.

    Precision = TP/(TP + FP)

Recall (or sensitivity) is the portion of samples from a class which are correctly predicted by the model.

    Recall = TP/(TP + FN)

### Oversampling

- Oversampling models add records to the minority group to balance the dataset to (hopefully) remove bias in the training set.

#### RandomOverSampler

![NaiveRandomOversampling](https://github.com/krockway/Credit_Risk_Analysis/blob/main/Images/NaiveRandomOversampling.png)

- The RandomOverSampler method was 63.9% accurate, for low risk loans it was 100% precise and 69% sensitive, and for high risk loans it was 1% precise and 59% sensitive.

#### SMOTE

![SMOTEOversampling](https://github.com/krockway/Credit_Risk_Analysis/blob/main/Images/SMOTEOversampling.png)

- The SMOTE method was 62.2% accurate, for low risk loans it was 100% precise and 66% sensitive, and for high risk loans it was 1% precise and 59% sensitive.

### Undersampling

#### ClusterCentroids

![Undersampling](https://github.com/krockway/Credit_Risk_Analysis/blob/main/Images/Undersampling.png)
This ClusterCentroids method was 51% accurate, for low risk loans it was 100% precise and 43% sensitive, and for high risk loans it was 1% precise and 59% sensitive.

### Combination

#### SMOTEENN

![SMOTEENN](https://github.com/krockway/Credit_Risk_Analysis/blob/main/Images/SMOTEENN.png)
This SMOTEENN method was 64.1% accurate, for low risk loans it was 100% precise and 55% sensitive, and for high risk loans it was 1% precise and 74% sensitive.

### Ensemble Classifiers

#### BalancedRandomForestClassifier

![BalancedRandomForestClassifier](https://github.com/krockway/Credit_Risk_Analysis/blob/main/Images/BalancedRandomForestClassifier.png)
This BalancedRandomForestClassifier method was 78.7% accurate, for low risk loans it was 100% precise and 91% sensitive, and for high risk loans it was 4% precise and 67% sensitive.

#### EasyEnsembleClassifier

![EasyEnsembleAdaBoostClassifier](https://github.com/krockway/Credit_Risk_Analysis/blob/main/Images/EasyEnsembleAdaBoostClassifier.png)
This EasyEnsembleAdaBoostClassifier method was 92.5% accurate, for low risk loans it was 100% precise and 94% sensitive, and for high risk loans it was 7% precise and 91% sensitive.

## Summary

Overall, each model was very precise at identifying low risk loans; but were quite imprecise at identifying high risk loans, which defeats the purpose of our research, we want to identify high risk loans. 

Because of the imbalance of the dataset, accuracy is not a valuable measure in any of the models.  

The EasyEnsembleClassifier method was best at identifying high risk loans (91% recall) and should be used moving forward; but a close eye should be kept on future data points, as overfitting may be an issue.