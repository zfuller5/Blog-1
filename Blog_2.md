# Flip or Flop - Ames, IA
## Taking a look at whether to renovate a home, sell, or rent a home in Ames, Iowa

### Description
---
Do you love HGTV? Have you thought about trying your hand at renovating and flipping a home? What about just making passive income with real estate? This data science deep dive into housing data from Ames, Iowa will allow us to predict whether or not you should buy, sell, renovate or rent a residential home in Ames, Iowa.


### Why is this important?
---
Real estate as a means of investing and setting up retirement is an age old method. Think of every wealthy person you know or maybe that person who retired early. It is most likely they have acrued, used, and profitted from real estate to create their financial independence. In this study, We will be providing a prediction on sales price for housing in Ames, Iowa. With this prediction, we will be seperating the housing marketing into 6 groups: homes under 1,000 sqft, between 1,000 and 2,000 sqft, between 2,000 and 3,000 sqft, between 3,000 and 4,000 sqft, between 4,000 and 5,000 sqft, and over 5,000 sqft. Based on predictive accuracy in these groups, we can recommend to any type of investor which home size tier they should target for the first or next investment property.


### How do we do this?
---
We will be exploring Regression metrics to make our predictions on the home sale price. These include a Linear Regression with a look at Ridge and LASSO Regression. The data will be cleaned and null values removed, and several feature engineering processes will be analyzed including scaling, creating interaction terms via polynomial features, and creating dummy variables to more accurate analyze binary results. All analysis will be compared the baseline score of a simple null model or average predictive price to confirm that we have designed a model that outperforms a simple average of sales price versus home square footage.


### What did we find?
---
After cleaning and analyzing the housing data, we found that we did not have usable data above 5,000 sqft (only 2 data points), between 4,000 and 5,000 sqft (no data points), and between 3,000 and 4,000 (only 13 data points). Thus, our conclusions were limited to the bottom three groups of housing sizes. Ultimately, our predictions can be broken down in the following table:

| Housing Tier | R2 Score (Explained Variance) | RMSE (Average error in Sale Price) |
| --- | --- | --- |
| **Under 1,000 sqft** | *We can explain 64.3% of the variance in Sales price based on our features* | *Sale Price can be off by $13,074 on average for a median price of $114,407* |
| **Between 1,000 and 2,000 sqft** | *We can explain 79.4% of the variance in Sales price based on our features* | *Sale Price can be off by $25,754 on average for a median price of $178,411* |
| **Between 2,000 and 3,000 sqft** | *We can explain 78.8% of the variance in Sales price based on our features* | *Sale Price can be off by $49,745 on average for a median price of $284,303* |


### You decide your future!
---
Do you have your own HGTV show? Oh really? Well, you should definitely go big or go home for better ratings. Don’t have your own HGTV show? Let me recommend tier 3 size between 3,000 and 2,000 sqft with the 2nd highest variability score of 78.8%. This option would be great for a flip or to set up for rent for local Cyclone students as multi-room, multi-income passive income. Don’t have an appetite for risk? Start out in tier 1 size under 1,000 sqft with a variability score of 64.3% and average price of $114,407. This entry price is perfect for first time investors. Are you kinda in between? Well, tier 2 size is for you between 2,000 sqft and 1,000 sqft with the highest variability score of 79.4% and pricing prediction error of only 14.4%. This tier has the best trade-offs of the three considered.


### Dictionaries
---
**Code Dictionary:**

| File Name | Description |
| --- | --- |
| **01_eda_kaggle.ipynb** | *Notebook for running eda and Linear Regression for Kaggle Submission* |
| **02_eda_model.ipynb** | *Notebook for testing various EDA and prediction models on training data* |
| **03_eda_ppt.ipynb** | *Notebook for running final model analysis on problem statement* |


**Datasets Dictionary:**

| File Name | Description |
| --- | --- |
| **sample_sub_reg.csv** | *Example format for Kaggle submission (supplied data)* |
| **test.csv** | *Test data set minus 'SalePrice' (supplied data)* |
| **train.csv** | *Train data set used as working data set (supplied data)* |


**Submissions Dictionary:**

| File Name | Description |
| --- | --- |
| **send_it.csv** | *Kaggle submission from 01_eda_kaggle.ipynb notebook* |
| **final_train.csv** | *Cleaned train dataset from 02_eda_model.ipynb notebook* |
