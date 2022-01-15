# NLP & Unsupervised Learning Project MVP

## What people talk about Dr. Robert Malone? -- NLP Analysis after his ban by twitter

This project is to find what people are talking about Dr. Robert Malone on twitter recently.
Who is Dr. [Robert Malone](https://en.wikipedia.org/wiki/Robert_W._Malone)? He is a virologist and immunologist. I never heard about him until his recent remarks about warning parents to be prudent to decide if to give their children Covid_19 shots. And later one of his interviews went virus, which caused his ban from Twitter. I would like to know that when people mention Robert Malone and the ban, what  their main topics are? Positive or Negative?


### Solution Path
I use Twitter API Tweepy help pull related tweets from Twitter, with search phrase "Robert Malone" and "Dr Malone". I am able to obtain over 20k tweets, each includes info of twitter username, ID, user description, tweet text, retweet number and etc. Different NLP techniques will be used, like NLP preprocessing, sentiment analysis, vectorization, dimensionality reductions, top modeling and clustering.


### Work Completed

Tweets has been pulled and transformed into data frame. During preprocessing, I removed all url link and tags. Sentiment analysis is used for finding out people's attitude towards Dr. Robert Malone.

I also created a few baseline models using TfidfVectorizer, with an LSA topic modeler ( topic number is 10)


### Recent Findings

Most people hold a neutral attitude when their tweets revolves around Dr. Robert Malone, according to compound score proved by SentimentIntensityAnalyzer.



<img src="https://github.com/PurpleGrace/Metis_NLP_DR_ROBERT_MALONE_Github/blob/main/Compund%20score.png" alt="Compund Score Histogram">


The Baseline top modeling shoes a initial topics like the following:
<img src="https://github.com/PurpleGrace/Metis_NLP_DR_ROBERT_MALONE_Github/blob/main/Baseline%20topic%20modeling.png">

### Moving Forward

- Try do analysis for people hold different attitude by using their location and author description.
- Try to use different vectorization and topic modeling algorithm with tuning hyper parameters to find topics more interpretable.
- Using clustering techniques to find users with similar opinion/attitude towards Dr. Robert Malone.
