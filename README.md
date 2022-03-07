# Sentiment Analysis of Cricket Data
Foundations of Data Analytics (CSE3505) J Component

## Steps to be followed:
#### 1. Loading required tools and packages:
Load the required packages in RStudio, namely rtweet, dplyr, tidyr, tidytext, textdata, ggplot2, purrr, reshape2, and wordcloud.
#### 2. Data Extraction from Twitter:
Twitter has made the task of analyzing tweets posted by users easier by developing an API that we can use to extract tweets and underlying metadata. It helps obtain twitter data in a very structured format that can then be cleaned and processed further for analysis. Once the Twitter application is created, we get the Consumer Key (API Key), Consumer Secret (API Secret), Access Token, Access Token Secret keys, and tokens. These keys and tokens are used to extract data from Twitter in R.
#### 3. Initial Data Exploration:
Data exploration aims to get all information and insight from Twitter data. We've pulled the tweets for hashtag #INDvNZ and saved them into a data frame. We looked at the variables favoriteCount (no of likes) and retweetCount (no of retweets) to find out about engagement. We then analyzed the ratio of replies, retweets, and organic tweets that would help to gain more insight into the type of data and users corresponding to the given hashtag. We also found out when the users have tweeted the most on a 24-hour basis and interpreted graphically.
#### 4. Data Preprocessing:
Data cleaning refers to recognizing incomplete, inaccurate, or irrelevant data parts and then replacing, modifying, or removing the dirty or coarse data. We use pre-processing text transformations to clean up the tweets; this includes stemming words. Additional pre-processing includes converting all words to lowercase, removing links to web pages, and removing punctuation and stopwords. The text package contains a list of over 1,000 stopwords in  English that do not help determine the overall sentiment of the body of the text. So words such as "I", "myself", "themselves", "being" and "have" should be excluded. We use the tidytext package with an anti-join to remove the stop words from the extracted tweets.
#### 5. Evaluating the sentiment in text:
The tidytext package provides access to several sentiment lexicons. The three general-purpose lexicons are AFINN, bing, and NRC which are based on unigrams, i.e., single words. These lexicons contain many English words, and the words are assigned scores for positive/negative sentiment. The bing lexicon categorizes words in a binary fashion into positive and negative categories. The AFINN lexicon assigns words with a score that runs between -5 and 5, with negative scores indicating negative sentiment and positive scores indicating positive sentiment. We will be using bing to get the sentiment.
