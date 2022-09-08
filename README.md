# Stock Market Prediction using LSTM and tweets.

This repository contains codes to extract tweet using a search query, find their sentiment, get relevant stock data and use LSTM or other neural network to get predictions. This should not be used in real life trading. 

## Dataset

The Stock Data for the study is Apple Inc which was collected using [snscrape](https://github.com/JustAnotherArchivist/snscrape).
Tweets were extracted using twitter from 27 September 2022 to 31 August 2022. A total of 25000 tweets were extracted.

## Tweet preprocessing
Timestamp was reformatted to be more suited with stock date and basic preprocessing was done for the tweets. Afterwards polarity score was found for each tweet.
Next was to group them together by date and aggreate the sum of polarity by date counts.

## Stock data
After this stock data was extracted using yahoo finance and merged with clean data containing polairty and tweet counts after grouping them by day.

## Training 
A Simple LSTM layer was then used for training with dropouts. Adam was the optimizer and  MSE was the loss function

## Evaluation

RMSE and R-Squared was the metric used for the evaluation.


![alt text](https://github.com/wanderer799/scaling-octo-fiesta/blob/main/bokeh_plot.png?raw=true)

