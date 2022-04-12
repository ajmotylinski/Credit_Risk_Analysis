# Overview
Evaluating credit risk can be challenging since it is a unbalanced classification problem. With this type of problem, it is necessary to look at multiple models to determine which one fits best. The fact that good loans significantly outnumber the risky loans is the reason why the additional time should be taken to evaluate this. The cost of a bad loan is also very high which is why this is an important issue to tackle.

# Results
Six models were evaluated to deterine which one that provides the best at predicting if a loan will default or not. Below is a brief summary of the model and how it performed. The same data set was used for each of the models. To evaluate each model, the data set was split into a training data and test data. The training data was used to predict the outcome of the test data. The are three measures that were used to determine how successful the model was at predicting the riskly loans.


#### Precsion
Also referred to the positive predictive value. This measure looks at the actual positive divided by the total predicted positive.

#### Recall
Also referred as the sensitivity. This measure looks at correct positive preditions and takes into account any false negative predictions. This looks at how accurate a positive outcome was predicted. In cases where there is significant impact of a false negative, we would want the model to have a high recall, which means there are few false negatives.

#### Balanced Accuracy Score
Blends together the precision and recall to get an overall metric.

## Naive Random Sampling
Since our dataset is heavily weighted towards the good loans we want to scale the risky loans up to be proportional. With the naive random sampling, we just do this by replicating samples until risky loans are equivolent to good loans.
### Results
The results below show a balanced accuracy score of 62.9%.
The recall for a high risk loan being 57%
The precision is 1%.

![Naive Sampling](../main/Resources/naive_sampling.png)

## SMOTE Oversampling
Synthetic minority oversampling technique (SMOTE) is another way to bring parity between the categorizes. In this case, new data points are generated based on data from the minority group.
### Results
The results below show a balanced accuracy score of 62.9%.
The recall for a high risk loan being 62%
The precision is 1%.

![SMOTE](../main/Resources/smote.png)

## Undersampling
Undersampling is the converse of oversampling. In this situation, the majority data is scaled down to match the number of samples of the minority class. In our case, the low risk loans are scaled down to the same number of risky loans.
### Results
The results below show a balanced accuracy score of 59.9%.
The recall for a high risk loan being 61%
The precision is 1%.

![Under Sampling](../main/Resources/under_sampling.png)

## Combination (Over and Under) Sampling 
Combining both over and under sampling is also referred to SMOTEENN since it combines oversampling the minority class with SMOTE but then undersampling with Edited Nearest Neighbors(ENN)
### Results
The results below show a balanced accuracy score of 64.1%.
The recall for a high risk loan being 70%
The precision is 1%.

![SMOTEEN](../main/Resources/smoteenn.png)

## Balanced Random Forest Classifier
Random forest model creates utilized decision trees to help predict the outcome. This model creates many small and simple decision trees and then aggregates the results to predict the outcome. 
### Results
The results below show a balanced accuracy score of 67.8%.
The recall for a high risk loan being 36%
The precision is 95%.

![Random_Forest](../main/Resources/random_forest.png)

## Easy Ensemble AdaBoost Classifier 
Adaboost is also referred to Adaptive Boosting. This creates an inital model and then a second model is run giving more weight to the errors from the first model. This is essentially the second model learning from the mistakes of the first model.
### Results
The results below show a balanced accuracy score of 93.1%.
The recall for a high risk loan being 92%
The precision is 9%.

![Easy Ensemble](../main/Resources/easy_ensemble.png)

# Summary
After reviewing all six of the models, Easy Ensemble AdaBoost Classifier model provided the best results with an accuracy rate of 93.1% and a precision of 9% when predicting high risk loans. The recall was 92% which also proved to be the highest among the models. This model is the one that should be used if the only focus is identifying high risk loans. A different model may be used if we were only looking at low risk loans. With the ease of running these models, it might prove useful to utilize multiple models.
