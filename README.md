# Module-14 - Algo Trading Bot

![image](https://user-images.githubusercontent.com/108433370/206271786-16ec52c9-2dc8-4cf5-be8e-07a194f73648.png)

## Background

For this Challenge, you’ll assume the role of a financial advisor at one of the top five financial advisory firms in the world. Your firm constantly competes with the other major firms to manage and automatically trade assets in a highly dynamic environment. In recent years, your firm has heavily profited by using computer algorithms that can buy and sell faster than human traders.

The speed of these transactions gave your firm a competitive advantage early on. But, people still need to specifically program these systems, which limits their ability to adapt to new data. You’re thus planning to improve the existing algorithmic trading systems and maintain the firm’s competitive advantage in the market. To do so, you’ll enhance the existing trading signals with machine learning algorithms that can adapt to new data.

====================================================================================================================

## What You're Creating

- > Implement an algorithmic trading strategy that uses machine learning to automate the trade decisions.

- > Adjust the input parameters to optimize the trading algorithm.

- > Train a new machine learning model and compare its performance to that of a baseline model.

### Establish a Baseline Performance

The provided CSV file contains open, high, low, close, and volume (OHLCV) data for a Morgan Stanley Capital International (MSCI)–based emerging markets exchange-traded fund (ETF) that iShares issued. Investments in emerging markets make up an important aspect of a well-diversified investment portfolio. That’s because the included equities have potentially higher long-term returns, even though they carry more risk.

1. Use the SVC classifier model from the SKLearn support vector machine (SVM) learning method to fit the training data and make predictions based on the testing data. Review the predictions.

2. Review the classification report that’s associated with the SVC model predictions.

3. Create a predictions DataFrame that contains “Predicted”, “Actual Returns”, and “Strategy Returns” columns.

4. Create a cumulative return plot that shows the actual returns vs. the strategy returns.

#### Default Parameters

months_offset = 3
short_win = 4
long_win = 100

### Tune the Baseline Trading Algorithm

In this section, you’ll tune, or adjust, the model’s input features to find the parameters that result in the best trading outcomes. (You’ll choose the best by comparing the cumulative products of the strategy returns.) To do so, complete the following steps:

1. Tune the training algorithm by adjusting the size of the training dataset. To do so, slice your data into different periods. Rerun the notebook with the updated parameters, and record the results in your README.md file.

2. Tune the trading algorithm by adjusting the SMA input features. Adjust one or both of the windows for the algorithm. Rerun the notebook with the updated parameters, and record the results in your README.md file.

#### Tuned Parameters
months_offset = 24
short_win = int(months_offset * 30 * 0.17)
long_win = int(months_offset * 30 * 0.35)

### Evaluate a New Machine Learning Classifier
1. Import a new classifier. AdaBoost was chosen.

2. Using the original training data as the baseline model, fit another model with the new classifier.

3. Backtest the new model to evaluate its performance.

====================================================================================================================

## RESULTS

Baseline SVM model

![image](https://user-images.githubusercontent.com/108433370/206272567-c31000d6-3408-4de7-baa0-f01a4b59b564.png)

Tuned SVM model

![image](https://user-images.githubusercontent.com/108433370/206272639-f30ff969-4315-43f5-9686-0c462b5fce5b.png)

Alternative model

![image](https://user-images.githubusercontent.com/108433370/206272685-ed8bebc3-de7a-44d6-b377-0794d58e0b56.png)




