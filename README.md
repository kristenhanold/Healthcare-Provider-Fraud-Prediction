# Healthcare Provider Fraud Prediction in Georgia Hospitals

## Problem Statement

The goal of this project was to predict the likelihood of a healthcare provider committing a medical fraud in the state of Georgia based on claims filed among them. 
We will also explore variables such as age, race, and gender that may show a pattern of a provider committing fraudulent claims to understand future behaviors and patterns. 

### Data Source: https://www.kaggle.com/rohitrox/healthcare-provider-fraud-detection-analysis

One of the biggest problems medicare is facing is provider fraud. Over the years, medicare spending has been increasing exponentially due to fraudulent claims being made by providers. 
Medicare data has shown providers using an ambiguous diagnosis code to adopt the costliest procedures and drugs. These bad practices impact insurance companies the most, leading them to increase their insurance premiums to be able to cover these costly claims.
The definition of Healthcare fraud is organized crime which involves peers of providers, physicians, beneficiaries acting together to make fraud claims. Examples of healthcare fraud are: Billing for services that were not provided, duplicate submission of a claim for the same service, misrepresenting the service provided, and more.

### Overfitting Issue

“In statistics, overfitting is ‘the production of an analysis that corresponds too closely or exactly to a particular set of data, and may therefore fail to fit additional data or predict future observations reliably’".
After performing our machine learning models, we noticed the accuracy scores were incredibly low. Meaning the models we created were not able to understand the complexity of our datasets
Our dataset contained an overfitting issue, and when models were produced from this dataset, even more overfitting issues happened

Solution:
We performed K-Fold Cross Validation to provide a more accurate measure of the performance of our models 
Our data was partitioned into “folds”, then our data is trained on k - 1 folds, and these remaining “folds” are used as our test set
By doing this, we are keeping our test set separate as “true unseen data” for our final model, and avoiding overfitting
(https://www.edureka.co/blog/overfitting-in-machine-learning/)


### Our Prediction

Based on our prediction on the Random Forest Classifier, as the accuracy score was the highest for this model
From our data frame containing probabilities predicting either No Fraud or Potential Fraud, we pulled our “Potential Fraud” column for this visualization
There is a positive skew present and a slightly smaller amount of probabilities predicting “No Fraud”, thus, we can conclude that there is a higher likelihood that no healthcare fraud is being committed in hospitals within the state of GA

