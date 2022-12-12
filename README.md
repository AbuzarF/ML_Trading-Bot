# Module 14: algo-trading

# Description

In this assignment we will be analyzing the price movement of a stock over the period 21 January 2015 to 22 January 2021. Our task is  to investigate the profiability by using different trading strategies, some of the strategies incorporated machine learning algorithms.

<br>


## Baseline Strategy
 In baseline strategy, we calculated percent change (returns) which generated a buy signal when the stock has a positive return for the current day and a sell signal when the stock has a negative return . Below is a graphical representation of the trategy returns.

![Baseline Strategy](https://github.com/AbuzarF/ML_Trading-Bot/blob/main/BaselineStrategy.PNG)

We can assess from the above that the asset performed well below par over the period considered.

<br>

## Support Vector Strategy with SMAs as the features
 We build our strategy by using the 4 day and 100 day rolling windows to calculate the Fast and Slow Simple moving average of prices respectively. The features were incorporated in X variables for Support vector classification model. And for y-variable we used the earlier strategy which generated a buy signal when the stock has a positive return for the current day and a sell signal when the stock has a negative return. The graphical reprewsentation of the strategy performance is shown below: 

![Baseline Strategy](Images/SVCresult.PNG)

The above graph shows the strategy performed slightly better than a benchmark buy and hold strategy. Now we looked at using alternative models to derive a better strategy return than the SVM model.

<br>

## Baseline Strategy with another classifier (Logistic Regression Model)
Using the same training and test inputs as the support vector machine model, we then ran these inpus through a Logistic Regression classification machine learning model. Graphical rewpresentation of the results for this strategy against the baseline buy and hold strategy is shown below:

![Baseline Strategy with LRM](Images\OriginalLRresult.PNG)

 The strategy performed very well until around mid 2020 then significantly underperformed for the rest of the period. Our next goal was to build on this and fine tune our model to produce higher returns.

<br>

## Tune-in Logistic Regression Model
We build our strategy by using the 21 day and 115 day rolling windows to calculate the Fast and Slow Simple moving average of prices respectively. We changed the training period to 36 months with the remaining period being used to test our strategy. New strategy returns versus the baseline buy and hold strategy is shown below:

![Base Strategy](Images/TuneinLRresult.PNG)

It is clear from the above graph, our tuned Logistic Regression model produced great results over the period considered and significantly outperformed the baseline straregy.
