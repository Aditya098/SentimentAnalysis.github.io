## What is Sentiment analysis?

*Sentiment Analysis* is the process of ‘computationally’ determining whether a piece of writing is positive, negative or neutral. It’s also known as opinion mining, deriving the opinion or attitude of a speaker.

## Why Sentiment Analysis ?
###  __Sentiment Analysis of Business__
  As we know, Twitter is a reservoir for a vast amount of data.This data can be extremely useful for business decisions, new product research and deciding on what content to share with your audience. Pre social media you know what we relied on? Instinct. This is kind of risky when it’s being used to determine where the money moves.

###  __Sentiment Analysis of Politics__
   In political field, it is used to keep track of political view, to detect consistency and inconsistency between statements and actions at the government level. It can be used to predict election results as well!



## Twitter Sentiment Analysis

This topic covers the sentiment analysis of any topic/query by parsing the tweets fetched from Twitter using Python.
### Steps Involved
### *Installation*
1.Tweepy: tweepy is the python client for the official Twitter API.Install it using following pip command
```pip install tweepy```

2. TextBlob: textblob is the python library for processing textual data.Install it using following pip command:
```pip install textblob```

### *Authentication*
* In order to fetch tweets through **_Twitter API_**, one needs to register an App through their twitter account. 
    *Steps*
    1. Go to [Twitter Developer](https://apps.twitter.com) and select Create New App option
    2. Fill the application details.
    3. Once the app is created Open the ‘Keys and Access Tokens’ tab. 
    4. Copy ‘ConsumerKey’, ‘Consumer Secret’, ‘Access token’and ‘Access Token Secret’.

* To Plot nice interactive Graphs we use  **_Plotly_**
    1. Create a [Plotly](https://plot.ly) account 
    2. Go to [API Settings](https://plot.ly/settings/api) and note the api key.
    


### Here is how the final result will look like
     ```Positive tweets percentage: 37 %
        Negative tweets percentage: 2 %
        Neutral tweets percentage: 61 %```
     
 ![Sentiment_Analysis](/sentiment_analysis_OnePlus.png)
 
* [Link](https://plot.ly/~adityac564/40/#plot) for an interactive plot in plotly.

* [Github Link](https://github.com/Aditya098/SentimentAnalysis.github.io/blob/master/Sentiment_Analysis.py) for the Code.
     
### We follow these 3 major steps in our program:

* Authorize twitter API client.
* Make a GET request to Twitter API to fetch tweets for a particular query.
* Parse the tweets. Classify each tweet as positive, negative or neutral.

 
First of all, we create a _TwitterClient class_. This class contains all the methods to interact with __Twitter API__ and parsing tweets. We use **_init_** function to handle the authentication of API client.
In __*get_tweets function*__, we use:
```python
fetched_tweets = self.api.search(q = query, count = count)
```
to call the Twitter API to fetch tweets.

In __*get_tweet_sentiment*__ we use textblob module.
```python
analysis = TextBlob(self.clean_tweet(tweet))
```

We use _sentiment.polarity_ method of __TextBlob__ class to get the polarity of tweet between -1 to 1.
Then, we classify polarity as:
```python
if analysis.sentiment.polarity > 0:
       return 'positive'
elif analysis.sentiment.polarity == 0:
       return 'neutral'
else:
       return 'negative'
```
Then, we can do various type of statistical analysis on the tweets. For example, in our program, we tried to find the percentage of positive, negative and neutral tweets about a query.


## References
https://textblob.readthedocs.io/en/dev/quickstart.html#sentiment-analysis

http://textblob.readthedocs.io/en/dev/_modules/textblob/en/sentiments.html

