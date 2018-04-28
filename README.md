# stocknet-dataset

A comprehensive dataset for stock movement prediction from tweets and historical stock prices.

## Dataset Overview
Two-year price movements from 01/01/2014 to 01/01/2016 of 88 stocks are selected to target, coming from all the 8 stocks in the Conglomerates sector and the top 10 stocks in capital size in each of the other 8 sectors. The full list of 88 stocks and their companies selected from 9 sectors is available in ***appendix\_table\_of\_target\_stocks.pdf***.

## Data Component
This dataset comprises two main components,

* ***./tweet***: tweet data
* ***./price***: price data  

Each component contain their raw data and preprocessed data organized by stocks,  

* ***./tweet/raw***
* ***./tweet/preprocessed***

and  

* ***./price/raw***  
* ***./price/preprocessed***

## Data Format

### Raw Tweet Data
Foramt: JSON  
Keys: see [Introduction to Tweet JSON](https://developer.twitter.com/en/docs/tweets/data-dictionary/overview/intro-to-tweet-json
)

### Preprocessed Tweet Data
Format: JSON  
Keys: 'text', 'user\_id\_str', 'created\_at'

### Raw Price Data
Format: CSV  
Entries: date, open price, high price, low price, close price, adjust close price, volume  

### Preprocessed Price Data
Format: TXT  
Entries: date, movement percent, open price, high price, low price, close price, volume  
Note: *open, high, low, close prices are normalized values.*