# SP500-Direction-Predictor-A-Machine-Learning-Approach-with-Backtesting
This is an end-to-end project where I develop and backtest a machine learning model that aims to predict the direction of the S&P 500 index. Leveraging Python, I fetch historical price data, perform data cleaning, and apply the RandomForestClassifier from sklearn for model training and prediction. The repository contains a complete walkthrough of the process, which includes data visualization, feature engineering, model evaluation, and backtesting system construction. And I welcome any suggestions for improvements or questions about the project.

## Introduction
Hello everyone! I've created a GitHub repository to share my work on an exploratory project where I attempted to predict the direction of the S&P 500 index using a machine learning model. Specifically, the project aims to forecast whether the S&P 500 index would go up or down on a particular day based on historical data. The main model used for this prediction is a RandomForestClassifier from the sklearn.ensemble module.

### This project includes various tasks such as:

Importing and cleaning data

Visualization of time-series data

Feature engineering for machine learning

Model training and prediction

Model evaluation

Backtesting the model

I used Python as my primary programming language and utilized libraries such as yfinance, sklearn, and plotly.

## Detailed Explanation
Firstly, we use yfinance to download the historical price data of the S&P 500 index. The S&P 500 index, represented as "^GSPC" in the code, is a market-capitalization-weighted index of 500 of the largest publicly traded companies in the U.S.

We clean and visualize the data using plotly.graph_objects. plotly is a Python graphing library that makes interactive, publication-quality graphs. The line graph represents the closing prices of the S&P 500 index over time.

Next, we remove unnecessary columns ("Dividends" and "Stock Splits") and create a new column, "Tomorrow," which contains the closing price of the next day. This is achieved by shifting the "Close" column up by one row using the .shift(-1) method. Then, we create a "Target" column, which contains binary data: 1 (the price went up) or 0 (the price went down).

We use the RandomForestClassifier from sklearn.ensemble to train our model. We split our data into a training set and a test set. The model is trained on the training data and is then used to predict the values for the test data.

We evaluate the model's precision using the precision_score from sklearn.metrics. Precision is the ratio of correctly predicted positive observations to the total predicted positives. It is a good measure to determine, when the costs of False Positive are high.

Finally, we create a backtesting system to assess the model's performance over different periods. We make use of a rolling window methodology to train and test our model and check its accuracy in different time frames.

By the end, we enhance our feature set with new indicators computed from rolling averages and trends over different horizons. We also adapt our prediction threshold to improve the precision of our model.

## Note: 

Please note that this is a simplified predictive model, and like all predictive models, it's not always accurate. It should not be used for real-world trading without further refinement and understanding of the financial markets.
