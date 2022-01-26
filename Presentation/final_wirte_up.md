# NLP and Unsupervised Learning Project
## What people says about Dr. Malone

### Abstract
This project is to find what people are talking about Dr. Robert Malone on twitter recently.
Who is Dr. [Robert Malone](https://en.wikipedia.org/wiki/Robert_W._Malone)? He is a virologist and immunologist. I never heard about him until his recent remarks about warning parents to be prudent if to give their children Covid_19 shots. And later one of his interviews went virus, which caused his ban from Twitter. I would like to know that when people mention Robert Malone, what  their main topics are? Are they holding a positive or a negative attitude?

### Design
The project will use natural language processing and Unsupervised learning techiniques to do analysis on people't tweets which are pulled by using Tweepy API. User's self description give us a hint what that person values most, their personality, hobby, thought etc. Topic modeling are performed on those two group of text dataset. Also we use Vader to do sentiment analysis for people's attitude when they talk about something.

### Data

The dataset is obtained from Twitter by using Tweepy API, including 20k+ tweets, self descriptions, followers, following, retweets and etc. Due to limited access to twitter for my developer account, I am not able to pull data morn than 7 days earlier. So the analysis is only focus on the recent week people's subjects and topics related to Dr. Malone. The latest tweets was create at 2022-01-14 17:47:15+00:00 and earliest was at 2022-01-07 17:53:24+00:00. For this project, we put out attention on Tweets and self description text.


### Algorithms
- **Feature Engineering**
  - Transfering categorical features to binary dummy variables.
  - Dropping features with little importance to simplify models.

- **Models**  

k-nearest neighbors,Logistic regression, decision trees,naive bayes and various ensembling techiniques are used before choosing the strongest model for cross validation performance. After performing aformentioned basic models, we adopted the random forest model as our final model. We tuned the model by adjusting hyper paramters to optimizing and avoid overfitting.

- **Model Evaluation and Metric Selection**  


For this analysis, we would like to decrease both false positive and false negative rate. False positive happens when hotel incorrectly classifies on-cancelation booking as cancelation case, thus might leads to overbooking; on the other hand, false negative is the model incorrectly classifies cancled booking as non-cancelation case, which might lead to underbooking. Therefore, the project seeks to both good ```precison``` and ```recall measurement```, in this case, ```f1```score which combines both becomes the main metrics of our model.

- **Result**


### tools
- Numpy and Pandas for data manipulation.
- Scikit-learn for modeling.
- Matplotlib and Seaborn for plotting.
- plotly for geographic plots.

### Communications
A PPT presentation will be presented.
