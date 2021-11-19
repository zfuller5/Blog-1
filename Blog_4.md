# Box Office Predictor
## Attempting to predict box office success
-By Zach Fuller

### Description
---
Based on historical data on box office movies, can we predict the financial success. This model will examine appropriate features to determine if we can improve on the baseline accuracy.


### Why is this important?
---
Production companies know making a movie can be a losing game, but how can we give them confidence that the right recipe will ensure success? Let's come up with a predictive model that can be used to give these executives confidence to foot the big for their next project.


### How do we do this?
---
We will be exploring Regression metrics to make our predictions on box office revenue. These include a Linear Regression with a look at Ridge and LASSO Regression. The data will be cleaned and null values removed, and several feature engineering processes will be analyzed including scaling, creating interaction terms via polynomial features, and creating dummy variables to more accurate analyze binary results. All analysis will be compared the baseline score of a simple null model or average predictive price to confirm that we have designed a model that outperforms a simple average of box office revenue.


### What did we find?
---
After cleaning and analyzing the box office data, I found that our features gave us a pretty low score (Train: 63.1%, Test: 59.4%) even on scaled data, so I wanted to look at a simplified feature set. By removing all of my dummy features, I saw my model performing in a similar range but with better score between train and test (Train: 60.6%, Test: 59.5%). I further looked at using Polynomial Features, Ridge and LASSO Regularization Models. I saw predictive performance drop off with Polynomial features (Train: 64.4%, Test: 55.1%) while Ridge (Train: 60.6%, Test: 59.6%) and LASSO (Train: 60.6%, Test: 59.5%) performed very similar to non-regularized data.


### Conclusions?
---
With production cost in the tens of millions of dollars, I would rate a succesfull model as being able to predict within 10%. My model's RMSE was $84,819,156 which was actually worse than the null model of $73,385,336. Thus, I would not use this model and simply use average revenue value.


### Dictionaries
---
**Code Dictionary:**

| File Name | Description |
| --- | --- |
| **01_eda.ipynb** | *Notebook for running eda on the training data set* |
| **02_models.ipynb** | *Notebook for testing various models on training data* |


**Datasets Dictionary:**

| File Name | Description |
| --- | --- |
| **clean_train.csv** | *Cleaned training data* |
| **test.csv** | *Test data set minus 'revenue' (supplied data)* |
| **train.csv** | *Train data set used as working data set (supplied data)* |
