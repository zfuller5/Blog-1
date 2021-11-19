# Heisman Trophy Predictor
## Using Data Modeling to predict the Heisman Trophy Winner - Paul, Tab, and Zach

### Description
---
The Heisman Trophy is the penultimate award for NCAA college football that supposedly is awarded to the best football player of the year. Which players are in the running is a common topic of discussion in the sports media and online forums. This project seeks to use data related to player statistics, specifically passing, rushing and receiving data and college team data to predict which College football player is mostly likely going to win the Heisman Trophy.


### Why is this important?
---
As with anything in the sports world, there is a sports betting aspect to the Heisman Trophy winner. So being able to predict the winner provides value to the sports betting industry. Aside from this, the Trophy is a prestigious award that generates millions in ad revenue and eventual life changing fame and marketing revenue for the winner. Media outlets cover and provide projections throughout the season, so tracking, following, and predicting the Heisman winner is very relevant to the College Football season.


### How did we do this?
---
The data we used for this project was web scraped from the website Sports Reference. Because defensive players are rarely represented in the Heisman top ten, we decided to exclude them from our data set and not consider defensive statistics. Additionally, we decided to focus on only the last twenty years of data (2000 - 2020) both due to time constraints and also because comparing years more than 20 years apart might affect the model due to changes in the game of college football. 

On Sports Reference, player data is divided into three sections: top players for passing, rushing, and receiving. The amount of players in each section varies by year, usually between 100-500 players per section. We used a request to scrape the data from the website and created a function to parse through the html and formulate it into a dataframe. In addition to player data, we also scraped team win-loss records and Hesiman voting results per year. Heisman trophy winners are elected through a voting process with the top ten players being displayed on the website. We scraped this data as our target variable. We concated all data until we had one data set per year and a data set with all the years. Some player names had a star next to them indicating if their data included postseason games so we removed the star with the replace function. We also converted all the data types to numeric data as it was originally all object data type. 


### What did we find?
---
We decided to predict 3 years to test the accuracy of our models. From our research we know that 2019 was the easiest year to predict because the winner won the award by the largest margin in the 86 year history of the Heisman Trophy. In 2020 the winner was a Wide Receiver where only 4 WR have won the award in the 86 year history of the Heisman Trophy and the last time a WR won was 1991 (almost 30 years). Lastly, we will attempt to predict the future 2021 winner based on up to date statistics after games were completed on October 23rd. Thus, we will be predicting the easiest year, the hardest year, and the unknown future year.

We explored the data using various Machine Learning models. We grouped these models into 3 categories: Linear Regression/Ridge/LASSO, KNN/Random Forrest/Boosting, and Neural Networks. For 2019, the LASSO, AdaBoost, and Neural Network models were able to predict the winner. For 9 offensive players in the 2019 top 10, LASSO could only predict 4 of the top 9 offensive voted players, AdaBoost could only predict 7 of the top 9, and Neural Network could only predict 7 of the top 9. For 2020, the LASSO, AdaBoost, and Neural Network models were not able to predict the winner with any model with Neural Networks and LASSO able to predict the winner as finishing 3rd place. For 10 offensive players in the 2020 top 10, LASSO could only predict 5 of the top 10 offensive voted players, AdaBoost could only predict 9 of the top 10, and Neural Network could only predict 6 of the top 10. For 2021, only the LASSO model was able to predict the player with the best projected odds through October 23rd. For the players with the 10 best odds at winning the 2021 Heisman Trophy, LASSO could only predict 3 of the top 10 players, AdaBoost could only predict 4 of the top 10, and Neural Network could only predict 3 of the top 10.

We have a model that can accurately predict the winner for a year when the winner won by the largest margin like 2019 with all considered models. When the front runner is a Wide Receiver like 2020 the best we can do is place him 3rd with a Neural Network and LASSO. For predicting the future winner in 2021 we can predict the current best odds player with a LASSO model.


### We have a winner! Kind of...
---
Overall the models performed better than expected. Although we weren’t able to account for player personalities and marketing or voter bias by region and conference, the player stats were able to carry the models to some degree. We originally sought to utilize classification but ultimately chose regression as our predictor due to data limitations. AdaBoost, Neural Networks, and Random Forest were our best performing ML models. 

We were only able to do minimal optimization and analysis of the features. This would improve our model scores. This can be achieved through grid search. Adding a running back and wide receiver rating would also potentially improve our predictions. Lastly, as a part of follow up analysis we hope to create a dashboard tool that generates our predictions with player stat inputs. 


### Software Requirements
---
Web scraping: requests, lxml, beautiful soup and pandas 
Modeling: pandas, tensorflow, keras, matplotlib, sklearn, and numpy


### Dictionaries
---
**Code Dictionary:**

|File Name|Folder|Description|
|---|---|---|
|Passing|code|Notebook for web scraping player passing data| 
|Rushing|code|Notebook for web scraping player rushing data|
|Receiving|code|Notebook for web scraping player receiving data|
|Standing|code|Notebook for web scraping team standings data|
|Voting|code|Notebook for web scraping Heisman voting data|
|Year|code|Notebook for concating yearly data|
|Linear_Modeling|code|Notebook for modeling with Linear Regression, Ridge, and LASSO|
|DecTree_Modeling|code|Notebook for modeling with KNN, Ada boost and K nearest neighbors|
|NN_Modeling|code|Notebook for modeling with Neural Networks|


**Dataset Dictionary:**

|Folder Name|Description|
|---|---|
|Heisman Voting|Top 10 Heisman voting results by year|
|Passing|Passing data by year|
|Receiving|Receiving data by year|
|Rushing|Rushing data by year|
|Standings|Complete standings data for each team by year|
|Year|All voting, passing, receiving, rushing, and standings data compiled by year|

