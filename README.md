# stocknet-dataset

This repository releases a comprehensive dataset for stock movement prediction from tweets and historical stock prices. Please cite the following paper [[bib](https://aclanthology.info/papers/P18-1183/p18-1183.bib)] if you use this dataset,  

Yumo Xu and Shay B. Cohen. 2018. [Stock Movement Prediction from Tweets and Historical Prices](http://aclweb.org/anthology/P18-1183). In Proceedings of the 56st Annual Meeting of the Association for Computational Linguistics. Melbourne, Australia, volume 1.
> Stock movement prediction is a challenging problem: the market is highly *stochastic*, and we make *temporally-dependent* predictions from *chaotic* data. We treat these three complexities and present a novel deep generative model jointly exploiting text and price signals for this task. Unlike the case with discriminative or topic modeling, our model introduces recurrent, continuous latent variables for a better treatment of stochasticity, and uses neural variational inference to address the intractable posterior inference. We also provide a hybrid objective with  temporal auxiliary to flexibly capture predictive dependencies. We demonstrate the state-of-the-art performance of our proposed model on a new stock movement prediction dataset which we collected.

You might also be interested in [our code](https://github.com/yumoxu/stocknet-code) for stock movement prediction. 

Should you have any query please contact me at [yumo.xu@ed.ac.uk](mailto:yumo.xu@ed.ac.uk).

## Dataset Overview
Two-year price movements from 01/01/2014 to 01/01/2016 of 88 stocks are selected to target, coming from all the 8 stocks in the Conglomerates sector and the top 10 stocks in capital size in each of the other 8 sectors. The full list of 88 stocks and their companies selected from 9 sectors is available in **StockTable**, a facsimile of the paper appendix **appendix\_table\_of\_target\_stocks.pdf**.

## Data Component
This dataset comprises two main components,

* **./tweet**: tweet data from [Twitter](https://twitter.com/)
* **./price**: price data from [Yahoo Finance](http://nance.yahoo.com/) 

Each component contains their raw data and preprocessed data organized by stocks,  

* **./tweet/raw**
* **./tweet/preprocessed**

and  

* **./price/raw**  
* **./price/preprocessed**

## Data Format

### Raw Tweet Data
Format: JSON  
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

