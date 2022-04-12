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

## Under Sampling
### Results
![Under Sampling](../main/Resources/under_sampling.png)

## SMOTEENN 
### Results
![SMOTEEN](../main/Resources/smoteenn.png)

## Balanced Random Forest Classifier 
### Results
![Random_Forest](../main/Resources/random_forest.png)

## Easy Ensemble AdaBoost Classifier 
### Results
![Easy Ensemble](../main/Resources/easy_ensemble.png)

# Summary
