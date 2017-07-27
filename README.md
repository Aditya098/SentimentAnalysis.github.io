## What is sentiment analysis?

Sentiment Analysis is the process of ‘computationally’ determining whether a piece of writing is positive, negative or neutral. It’s also known as opinion mining, deriving the opinion or attitude of a speaker.

## Why Sentiment Analysis ?
  * **Sentiment Analysis of Business**
            As we know, Twitter is a reservoir for a vast amount of data. This data can be extremely useful for business decisions, new product research and deciding on what content to share with your audience. Pre social media you know what we relied on? Instinct. This is kind of risky when it’s being used to determine where the money moves.

As valuable as workshops, user testing groups and customer surveys are, they take up time, effort and money that sentiment analysis on social media platforms can provide in minutes.


* **Sentiment Analysis of Politics**
             In political field, it is used to keep track of political view, to detect consistency and inconsistency between statements and actions at the government level. It can be used to predict election results as well!



## Twitter Sentiment Analysis

This topic covers the sentiment analysis of any topic by parsing the tweets fetched from Twitter using Python.
### Steps Involved
* *Installation*
  1.Tweepy: tweepy is the python client for the official Twitter API.
Install it using following pip command
```
pip install tweepy
```
  2. TextBlob: textblob is the python library for processing textual data.
Install it using following pip command:
```
pip install textblob
```
* *Authentication*
  1.In order to fetch tweets through Twitter API, one needs to register an App through their twitter account. 
    
    Steps
    1. Go to [Twitter Developer](https://apps.twitter.com) and select Create New App option
    2. Fill the application details.
    3. Once the app is created Open the ‘Keys and Access Tokens’ tab. Copy ‘ConsumerKey’, ‘Consumer Secret’, ‘Access token’ and ‘Access Token Secret’.
  
  2. To Plot nice interactive Graphs we use Plotly
    1.Create a [Plotly](https://plot.ly) account 
    2.Go to [API Settings](https://plot.ly/settings/api) and note the api key.
    


### Here is how the final result will look like
     ```
     Positive tweets percentage: 37 %
     Negative tweets percentage: 2 %
     Neutral tweets percentage: 61 %
     ```
     
   ![Sentiment_Analysis](/images/sentiment_analysis_OnePlus.png)
   [Link](https://plot.ly/~adityac564/40/#plot)for an interactive plot in plotly.
   [Link](https://github.com/Aditya098/Sentiment-Analysis/blob/master/sentiment_analysis.py)for the Code.
     
### We follow these 3 major steps in our program:

* Authorize twitter API client.
* Make a GET request to Twitter API to fetch tweets for a particular query.
* Parse the tweets. Classify each tweet as positive, negative or neutral.





