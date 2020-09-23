# Text & Sentiment Analysis (NLP)
Public Opinion on Twitter about the US airlines in 2015

## Aim

***Sentiment Analysis*** is a branch of Natural Language Processing (NLP) that allows us to determine algorithmically whether a statement or document is “positive” or “negative”.

Sentiment analysis is a technology of increasing importance in the modern society as it allows individuals and organizations to detect trends in public opinion by analyzing social media content. As the airline industry become increasingly competitive, airline companies are always trying their best to satisfy customer experience. Through sentiment analysis, these companies can obtain information on customers’ overall satisfaction and adopt business strategies to address aspects with low satisfaction.

The purpose of this project is to compute the sentiment of text information - in our case, tweets posted in 2015 regarding US airlines - and answer the research question: ***“What can public opinion on Twitter tell us about the US airlines in 2015?”*** The goal is to essentially use sentiment analysis on Twitter data to get insight into the people’s opinions on US airlines.

## Methodology

### Data Cleaning with Natural Language Toolkit (NLTK)

The tweets, as given, are not in a form amenable to analysis -- there is too much ‘noise’. Therefore, the first step is to “clean” the data. A procedure is designed to prepare the Twitter data for analysis by satisfying the requirements below.

  •	All html tags and attributes (i.e., /<[^>]+>/) are removed.

  •	Html character codes (i.e., &...;) are replaced with an ASCII equivalent.

  •	All URLs are removed.

  •	All characters in the text are put in lowercase.

  •	All stopwords are removed.

  •	If a tweet is empty after pre-processing, it should be preserved as such.

### Exploratory Data Analysis

  •	A simple procedure is designed to determine the airline of a given tweet and apply this procedure to all the tweets in the US airline dataset. We look at relevant words and hashtags in the tweets that identify to certain airlines.
  
  •	Public sentiments about US airlines from Tweets are visualized in the form of Bar charts.
  
  •	A Word Cloud to visualize the collection of positive words is created (Text + Class).   


### Model Preperation

Generic Tweets dataset ([zip](https://github.com/danishanis/Text-and-Sentiment-Analysis/blob/master/SentimentAnalysisData.zip)) is randomly split into training data (70%) and test data (30%). The data is prepared for ***logistic regression*** where each tweet is considered a single observation. In the logistic regression model, the outcome variable is the sentiment value, which is either positive or negative. The independent variables or features of the model can be whatever we want.

The frequency of each word is used as features of the model. (Alternatively, one can first tag each n-gram by its part of speech and then use the frequency of each part of speech as the features of the model.)

### Model Implementation

A ***Multiclass Logistic Regression*** model is trained on the training data and applied to the test data to obtain an accuracy value. The same model is later evaluated on the US Airline Data. 

The ***negative tweets*** about US airlines are split into training data (70%) and test data (30%). once again, a ***Multiclass Logistic Regression*** model is trained to predict the reason for the negative tweets. There are 10 different negative reasons labelled in the dataset.

## Results

It can be seen that poeple have expressed more negative sentiments on twitter than positive ones. We count the various negative and positive tweets made about individual US airlines. As per the predictions on the US Airlines tweets, United Airlines has the highest number of the negative tweets. However, this is due to the fact that the total number of tweets of the US Airlines is the highest. The predicted percentage of the negative tweets for each airlines are as follows: United Airlines 63%, US Airways 69.5%, American Airlines 64.4%, Southwest Airlines 54.6%, jetBlue 48.9%, Virgin America 42.3%, Delta Airlines 50%. Thus, as per the predictions, US Airways has highest percentage of the negative tweets which is 69.5%.

### Receiver Operating Characteristic (ROC) Curve

The ROC curve obtained from this model concludes that since most of the curve depicted passes well above on the top left corner of the graph with higher *True Positive Rate* and lower *False Positive Rate*, the model has made accurate predictions.

### Failure to Predict Negative Tweets correctly

Based on the classification report, the precision of the Negative Reason as Damaged Luggage was 0.0. Which suggestes that all of its predictions were incorrect. The model was not able to predict this reason because the firstly, the model has very few number of the tweets with the negative reason as ***'Damaged Luggage'*** for it to learn from the model.  


P.S. The .txt file containing ***Generic Tweets*** exceeds 25MB to be allowed to upload. It can be found in the [zip](https://github.com/danishanis/Text-and-Sentiment-Analysis/blob/master/SentimentAnalysisData.zip) folder here.




