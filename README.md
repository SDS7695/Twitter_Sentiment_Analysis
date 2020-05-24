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

| Algorithm | BOW F1 Score | TFIDF F1 Score | W2V_CBOW |
| --------- | ---------- | ------------------- | ----- |
| Logistic Regression | 0.5829383886255923 | 0.6 | 0.35772357723577236 |
| Naive Bayes |  0.502446982055465 | 0.55470737913486 | NA | NA |
| K Nearest Neighbor | 0.461139896373057 | 0.49370277078085645 | 0.47317073170731705 |
| SVM | 0.5392670157068064 | 0.5714285714285714 | 0.4804177545691906 |
| Decision Tree | 0.5294117647058822  | 0.5323383084577115 | 0.38493723849372385 |
| Random Forest | 0.5594059405940593 | 0.5298701298701298 | 0.4806629834254143 |
| XGBoost | 0.5203252032520326 | 0.5177111716621253 | 0.5416666666666666 |
| LightGBM | NA | NA | 0.510752688172043  |


### Public Leaderboard score

| Algorithm | BOW F1 Score | TFIDF F1 Score | W2V_CBOW |
| --------- | ------------ | -------------- | -------- |
| Logistic Regression | 0.5419968304278923 | 0.5344262295081966 | 0.3401109057301294 |
| Naive Bayes |  0.4826038159371493 |  0.5306799336650083 | NA | NA |
| K Nearest Neighbor | 0.4444444444444445 | 0.4958123953098827  | 0.4486571879936809 |
| SVM | 0.49544626593806923 | 0.5174825174825175 | 0.4253075571177504 |
| Decision Tree | 0.4816753926701571 | 0.4914089347079038 | 0.43556701030927836 |
| Random Forest |  0.5043782837127846 | 0.47755834829443444 | 0.48339483394833943 |
| XGBoost |  0.5274390243902439 | 0.5152979066022544 | 0.49735449735449727|
| LightGBM | NA | NA |  0.5008944543828264  |
