# TDT4173-project-group6
public repository for TDT4173 project, for political affiliation analysis for political tweets, discussed in the paper *Affiliation analysis of political tweets*. All the programing is done in google colab. The most important imported frameworks being; pandas, numpy,sklearn, gensim, and keras.

## PROJECT DESCRIPTION:
This paper presents the development and training of classifiers that based on a labeled trainingset of tweets identifies the party  of a US presidential candidate based on a tweet.

For  developing  and  training  such  a  classifier  we  will  be  working  with  real  life  tweets from the democratic and republican presidential candidates tweeted during the two most recentpresidential election years (2016 and 2020).

For  developing  the  classifier  we  will  be  using  the  supervised  learning  methods;Bag-of-words(BOW), its improved version-gram, and Convolutional neural networks (CNN). Bag-of-words, and n-gram. All three methods are supervised learning methods, which means they  will  be  using  a  dataset  of  labeled  data  to  train. In addition,  we  will  be  using  the  method Word2Vec, which is used to translate words into vectors in the CNN.

For our methods we want have real life tweets, with the candidate name, tweet, year (of tweet)and party.  All these values are saved in a comma-seperated values (csv) (TweetDatabase_2016.csv and TweetDatabase_2020.csv). In total we have 12 826 unique tweets(51.2% Democrat). The tweets are separated into three different datasets. The 2016 dataset only contains tweets from 2016 (6979 tweets, 54.1% Democrat).  The 2020 dataset(47.6% Democrat) only contains tweets from 2020 (5847 tweets).  The 2016-20 dataset is the union of the two other datasets.

## HOW TO RUN THE METHODS:

Before running any of the code, the csv files TweetDatabase_2016.csv and TweetDatabase_2020.csv need to be uploaded to colab. 

### Running logistic regression


### Running CNN

### Running 

In addition, for training the word2vec model in ML_project_(CNN).ipynb, the 'reddit_worldnews_start_to_2016-11-22.csv' need to be downloaded and uploaded to colab from https://www.kaggle.com/rootuser/worldnews-on-reddit. This file was too large to be directly uploade to the git repository. 

1) Data analytics, of the dataset is done in the file ML_project_(data_analysis). 
     <br/>1.1) Remember to upload TableIt.py to colab (in addition to TweetDatabase_2016.csv and TweetDatabase_2020.csv) to print out the tables.

2) Running logistic regression using bag-of-words and n-gram is done in the file ML_project_(BOW).ipynb.
    <br/>2.1) Remember to upload TableIt.py to colab (in addition to TweetDatabase_2016.csv and TweetDatabase_2020.csv) to print out the tables.

3) Running the CNN is done in the file ML_project_(CNN).ipynb. 
    <br/>3.1) Under retrieve data, you need to set df_all equal to the dataset which you intend to use, (tweets2016_df, tweets2020_df, or tweets2016_2020_df)
    <br/>3.2) the dimension of the word2vec embedding is defined in the variable word2vec_dim, which is set to 350
    <br/>3.3) the number of epochs, and batch size is defined under "train the CNN", which are set to 40 and 400 respectively. 
    
