# Web APIs & Classification

## Problem Statement
The aim of this project is to classify posts from 2 different subreddits, [/r/depression](https://www.reddit.com/r/depression) and [/r/anxiety](https://www.reddit.com/r/anxiety).<br>
The motivation behind this classification is for reddit users who may be suffering from either depression or anxiety issues but not properly diagnosed.<br>
This will help them to post in the correct subreddit and be able to get more useful help from comments, since depression and anxiety displays similar symptoms but with varying solutions on tackling them.

## Executive Summary

### Contents:
- [Data Source](#Data-Source)
- [Evaluation](#Evaluation)
- [Conclusion](#Conclusion)

### Data Source
The following links are the source of the data used to classify the subreddits. <br>
r/depression: https://www.reddit.com/r/depression<br>
r/anxiety: https://www.reddit.com/r/anxiety

### Evaluation
Random Forest with TfidrVectorizer performs slightly better with a slightly more accurate result.<br>
2 reasons that the posts might be incorrectly classified:
1. The reddit user that posted it might have posted them to the incorrect subreddit. As mentioned earlier in the problem statement, both anxiety and depression do showcase similar symptoms which could be the reason for the incorrect posting.
2. There's also a chance that the post is related to both anxiety and depression, so the post can be classified in either subreddit.

### Conclusion
The Random Forest with TfidfVectorizer worked fairly well with an accuracy score of close to 85%, even though both subreddits were fairly similar in nature.<br>
Logistic Regression with TfidfVectorizer also works equally well as well with an accuracy score of 84% <br>
We can expand our scope to include the following to further improve the models:

- Include lemmatization, stemming and spell checks to have a general feel of the posts
- Include more subreddits (eg. bipolar) in our classification model. This may be further extended to be used as an initial diagnosis of any mental issues that the user might be suffering from.
- Tuning of parameters for random forest to get a better score. However, this requires a longer amount of time to tune to get the perfect parameters.
- Consider either boosting or bagging to get a more optimal outcome.
