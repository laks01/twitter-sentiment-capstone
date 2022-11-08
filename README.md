# Capstone Project - Twitter Sentiment Analysis using Classification Models

In this capstone project, a customer will learn a company sentiment based on tweets with company hashtag. For example, #TWTR/#TSLA trending positive or negative based on tweets. It allows companies to observe their reputation based of the customers tweets. The tweets provide some insights into where they should be focusing to improve their reputation.

## Business Objectives
This application is built based on the CRISP-DM Framework. The following are the business objective of the application:

1. Identify social media reputation for a given company hashtag. 
2. Identify whether company sentiment is positive or negative
3. Summarize and provide future recommendations

## Data Collection

For this project, I collected tweets with hashtag #TWTR to observe the sentiment for last 7 days. I used the Twitter APIs to collect the data. Free version allows to collect the data for last 7 days. I used search tweets using Tweepy client library to access it. Here is the [Twitter API V2](<https://developer.twitter.com/en/docs/twitter-api/tweets/search/quick-start/recent-search>)

 ### Tweet: 
 <li> id </li>
      <li> text </li>
      <li> author_id </li>
      <li> created_at </li>
  
  

## Data Preparation

For this project I focused on tweet sentiment, I collected a minimal data such as id, text, author_id, created_at from Twitter API V2.
Data needs to be pre-processed before used by models. I completed these preprocessing steps:

### Preprocessing Steps
<li> Deleted the missed rows </li>
<li> Lowercase </li>
<li> Remove punctuations, urls,name </li>
<li> Remove stop words </li>
<li> Stemming/ Lemmatization </li>
<li> Tokenize Sentences </li>
</br>

    
Visualized the #TWTR Tweets to learn what's trending.
<center>
    <img src = images/wordcloud.png width = 100%/>
</center>
You can check the code in this notebook

## Model Training 

To train the models I collected the labeled data from [Sentiment Data](http://cs.stanford.edu/people/alecmgo/trainingandtestdata.zip). Training dataset has 1 million records. A sample dataset:

<center>
    <img src = images/sample_training_data.png width = 60%/>
</center>

### Logistics Regression Model

The training data and test data vectorized and split into 70/30 to train the models. I used below metrics to evaluate the moder Performance.

#### Confusion Matrix:


<center>
    <img src = images/log_confustion_matrix.png width = 60%/>
</center>

</br>

### Metrics

 <table> 
    <tr>
        <th>Precision</th>
        <th>Recall</th>
        <th>F1 Score</th>
        <th>AUC</th>
    <tr>
    <tr>
        <td>0.790</td>
        <td>0.809</td>
        <td>0.799</td>
        <td>0.796</td>
    </tr>
  </table>
  
 