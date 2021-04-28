# Disaster Tweets Classification

## About
An NLP classification project. Using machine learning to create models and identify text-based tweets that talks about real disaster from a mixture of tweets with varying topics and fake disaster tweets. 
Our priority will be on the target variable which is the disaster tweets. Additionally, we want to identify words that are strong predictors for our model.

## Data
The data consist of a training and a testing datasets that include location, target, text, and keyword. The location indicates where the tweet was sent from. A lot of the tweets do not have their location identified. In cases where they are, the locations varies too greatly in each tweets. The target classifies disaster tweets as 1 and others as 0. The text of the tweet. Could include website links, emoji, and typos. For keyword, a particular keyword from the tweet. This could be blank for some tweets.

## EDA

### Keywords
Keywords have a huge range of impacts. Some keywords are common within both tweets which means they are not great predictors, but some are also clear indications that the tweet is talking about real disaster (or not a disaster).
For example, derailment, debris, and wreckage are keywords used only in real disaster tweets, and the word aftershock is not contained within any real tweet. Additionally, these words occur often.

### Text
Word Distributions
The distributions of the characters are nearly the same. Note that 120 to 140 characters in tweets are common in both. This indicate that the length of the tweet won't help to determine our outcome
The distribution of the number of words in a tweet is similar in both types of tweets. They both follow a bell curve and peak and aroud 13 to 18 words per tweet.

Word Occurrence
We see a lot of letters that are not formed into words. From this we also conclude that http, com, co, and all other indication of a website should be remove as they occur regularly in both types of tweets. As usual, stop words will be removed as well. However, they will be used to create new features which may increase the over all performance of the models
Trigrams definitly shows a huge different between the phrases used in each tweet types. It can be safely assume that trigram will perform better than unigram and bigrams when optimizing the model.

## Feature Engineering
Feature used:
Word count, unique word count, stop word count, url count, mean word lenght, character length, punctuation count, hashtag count, mention count, text, location,and keyword.

## Conclusion
Overall all the models have roughly 80% accuracy after the texts have been preprocessed. However, the logistic Regression model was able to correctly identify around 74% of all of the disaster tweets which is the highest of all the models. This model associate topic words such as, Suicide, Storm, Wildfire, Hiroshima, Bombing, and Fire with disaster tweets and descriptive words like New, You, Body, Bag, My, and Full with other types of tweets.

