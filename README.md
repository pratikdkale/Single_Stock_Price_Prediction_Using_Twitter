
# Stock Price Prediction Using Twitter Sentiment

This project aims to predict the stock price of **Reliance Industries Limited (RIL)** using **Twitter sentiment analysis**. By combining social media signals with historical stock prices, we attempt to explore the impact of public sentiment on market behavior.

## Overview

The project pipeline includes:
- Collecting tweets relevant to Reliance
- Performing sentiment analysis on tweets
- Merging sentiment scores with historical RIL stock data
- Building a predictive model (Linear Regression)
- Visualizing the effect of sentiment on stock prices

## Datasets Used

1. **Tweets.csv**: Contains raw tweets about Reliance.
2. **RIL.csv**: Historical stock price data of Reliance Industries.
3. **Twitter_Dataset.pkl**: Pickled version of the preprocessed tweet dataset.

## Methodology

### 1. Preprocessing Tweets
- Clean tweet texts by removing mentions, URLs, emojis, and special characters
- Convert to lowercase and remove stopwords
- Perform tokenization and lemmatization

### 2. Sentiment Analysis
- Each tweet is assigned a polarity score using TextBlob
- Tweets are labeled as Positive, Neutral, or Negative

### 3. Feature Engineering
- Daily sentiment scores are averaged
- Resulting features include daily average sentiment and counts of each sentiment class

### 4. Data Merging
- Stock price data is merged with daily sentiment scores
- Final dataset includes stock closing prices and aggregated sentiment data

### 5. Predictive Modeling
- A linear regression model is trained to predict next-day closing prices
- Features used: sentiment polarity, sentiment counts

### 6. Evaluation
- Performance is evaluated using Mean Squared Error (MSE)
- Visual plots compare predicted vs actual stock prices

## Results

The model shows that Twitter sentiment holds weak but noticeable predictive power for RIL stock movements. The results validate that sentiment data can enhance traditional price forecasting.

## Dependencies

- pandas
- numpy
- matplotlib
- seaborn
- textblob
- sklearn

Install them using:

```bash
pip install -r requirements.txt
```

## How to Run

1. Clone the repository or download the `.ipynb` file
2. Ensure all datasets (`RIL.csv`, `Tweets.csv`) are in the same directory
3. Open the notebook and run all cells in order

## Credits

This project is developed as part of a stock prediction research case study using NLP and sentiment-driven market signals.
