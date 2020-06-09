# COVID-19_Sentiment_Analysis
Sentiment Analysis of tweets by Indian users related to COVID-19
COVID-19 has become the talk of the town. With increasing number of case and lockdowns back to back,people's concerns and emotions have scattered. The aim of the project is to analyze tweets tweeted by Indian users regarding COVID-19 and lockdown.<br>

# Data collection
Tweet data was collected using Optimized and Modified version of GetOldTweets3. GetOldTweets3 is a Python package that can be used to scrape historical data from Twitter.This package overcomes the limitations posed by the Twitter API<br>

*python GetOldTweets3.py --querysearch "#IndiaFightsCorona" --lang en -since 2020-03-23 --until 2020-04-01  --maxtweets 1000*<br>

The above command was used to obtain tweets from the API.Trending hashtags in India were used in the querysearch to keep it target specific.<br>

Tweets published within the period of 22nd March to 1st June were taken into account.About 30,000 tweets were mined.<br>

# Data Preprocessing
Basic data preprocessing was performed using pandas library and removal of URLSs,whitespaces,mentions,etc. were performed using regular expressions. Further text processing including tokenization,removing contractions and stopwords,lemmatization were done using NLTK library functions.<br>

# Deploying machine learning model 
VADER Sentiment Analyzer was used on the dataset to obtain sentiment scores.This sentiment score is the target variable.<br>
The approaches included:<br>- Multinomial Naive Bayes with CountVectorizer<br>- CountVectorizer with Logictic Regression<br>- TfidfVectorizer with Logistic Regression<br>- CountVectorizer with SVM<br>- TfidfVectorizer with SVM.<br>
The maximum accuracy was attained using CountVectorizer with SVM (81%).<br>

# Lexicon and rule based approach using TextBlob<br>
TextBlob package was used to determine the polarity and subjectivity scores. These were used for creating insightful visualizations.<br>

# References<br>
- Optimized and Modified GetOldTweets3: https://github.com/marquisvictor/Optimized-Modified-GetOldTweets3-OMGOT
- VADER Sentiment Analyzer: https://github.com/cjhutto/vaderSentiment
- TextBlob: https://textblob.readthedocs.io/en/dev/
