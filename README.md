![](https://github.com/SDS7695/Images/blob/master/Twitter%20Sentiment%20Analysis.png)

# Twitter_Sentiment_Analysis

The objective of this task is to detect hate speech in tweets. For the sake of simplicity, we say a tweet contains hate speech if it has a racist or sexist sentiment associated with it. So, the task is to classify racist or sexist tweets from other tweets.

Formally, given a training sample of tweets and labels, where label '1' denotes the tweet is racist/sexist and label '0' denotes the tweet is not racist/sexist, your objective is to predict the labels on the test dataset. 

## Motivation

Hate  speech  is  an  unfortunately  common  occurrence  on  the  Internet.  Often social media sites like Facebook and Twitter face the problem of identifying and censoring  problematic  posts  while weighing the right to freedom of speech. The  importance  of  detecting  and  moderating hate  speech  is  evident  from  the  strong  connection between hate speech and actual hate crimes. Early identification of users promoting  hate  speech  could  enable  outreach  programs that attempt to prevent an escalation from speech to action. Sites such as Twitter and Facebook have been seeking  to  actively  combat  hate  speech. In spite of these reasons, NLP research on hate speech has been very limited, primarily due to the lack of a general definition of hate speech, an analysis of its demographic influences, and an investigation of the most effective features.

 
## Data
Our overall collection of tweets was split in the ratio of 65:35 into training and testing data. Out of the testing data, 30% is public and the rest is private.

## Data Files

Source: https://datahack.analyticsvidhya.com/contest/practice-problem-twitter-sentiment-analysis

- train.csv - For training the models, we provide a labelled dataset of 31,962 tweets. The dataset is provided in the form of a csv file with each line storing a tweet id, its label and the tweet.
There is 1 test file (public)

- test_tweets.csv - The test data file contains only tweet ids and the tweet text with each tweet in a new line.
 
## Evaluation Metric:
The metric used for evaluating the performance of classification model would be F1-Score.

# Solution Details:
I have used various techniques for Feature Extraction and then applied different Machine Learning Algorithms to categorise the tweets between racist & non-racist. Below are the Feature Extraction techniques used:
- Bag of Words approach
- TF-IDF approach
- Word2Vec Continuous Bag of Words approach
- Word2Vec Skipgram approach

Below mentioned are the Machine Learning Algorithms used to create model:
- Logistic Regression
- Naive Bayes
- K Nearest Neighbor
- Support Vector Machines
- Decision Tree
- Random Forest
- XGBoost
- LightGBM

# Model Performance: 

### Model Score

| Algorithm | BOW  | TFIDF  | W2V_CBOW | W2V_SG | GloVe |
| --------- | ---------- | ------------------- | ----- | ------ | ----- |
| Logistic Regression | 0.583| 0.600 | 0.358 | 0.597 | 0.591 |
| Naive Bayes |  0.503 | 0.555 | NA | NA | NA |
| KNN | 0.461 | 0.493 | 0.473 | 0.562 | 0.614 |
| SVM | 0.539 | 0.571 | 0.480 | 0.598 | 0.571 |
| Decision Tree | 0.529  | 0.532 | 0.385| 0.479 | 0.449 |
| Random Forest | 0.559 | 0.530 | 0.481 | 0.572 | 0.509 |
| XGBoost | 0.520 | 0.518 | 0.542 | 0.607 |  0.595 |
| LightGBM | NA | NA | 0.511  | 0.591 | 0.618 |


### Public Leaderboard score

| Algorithm | BOW  | TFIDF  | W2V_CBOW | W2V_SG | GloVe |
| --------- | ---- | ------ | -------- | ------ | ----- |
| Logistic Regression | 0.542 | 0.534 | 0.340 | 0.514 | 0.531 |
| Naive Bayes |  0.483 |  0.531 | NA | NA | NA |
| KNN | 0.444 | 0.496  | 0.449 | 0.547 | 0.601 |
| SVM | 0.495 | 0.517 | 0.425 | 0.526 | 0.512 |
| Decision Tree | 0.482 | 0.491 | 0.436 | 0.498 | 0.378 |
| Random Forest |  0.504 | 0.478 | 0.483 | 0.564 | 0.459 |
| XGBoost |  0.527 | 0.515 | 0.497| 0.620 | 0.556 |
| LightGBM | NA | NA |  0.501  | 0.578 | 0.565 |
