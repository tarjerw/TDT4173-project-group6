# TDT4173-project-group6
public repository for TDT4173 project, for political affiliation analysis for political tweets, discussed in the paper *Affiliation analysis of political tweets*. All the programing is done in google colab. The most important imported frameworks being; pandas, numpy,sklearn, gensim, and keras.

## PROJECT DESCRIPTION:
This paper presents the development and training of classifiers that based on a labeled trainingset of tweets identifies the party  of a US presidential candidate based on a tweet.

For  developing  and  training  such  a  classifier  we  will  be  working  with  real  life  tweets from the democratic and republican presidential candidates tweeted during the two most recentpresidential election years (2016 and 2020).

For  developing  the  classifier  we  will  be  using  the  supervised  learning  methods;Bag-of-words(BOW), its improved version-gram, and Convolutional neural networks (CNN). Bag-of-words, and n-gram. All three methods are supervised learning methods, which means they  will  be  using  a  dataset  of  labeled  data  to  train. In addition,  we  will  be  using  the  method Word2Vec, which is used to translate words into vectors in the CNN.

For our methods we want have real life tweets, with the candidate name, tweet, year (of tweet)and party.  All these values are saved in a comma-seperated values (csv) (TweetDatabase_2016.csv and TweetDatabase_2020.csv). In total we have 12 826 unique tweets(51.2% Democrat). The tweets are separated into three different datasets. The 2016 dataset only contains tweets from 2016 (6979 tweets, 54.1% Democrat).  The 2020 dataset(47.6% Democrat) only contains tweets from 2020 (5847 tweets).  The 2016-20 dataset is the union of the two other datasets.

## HOW TO RUN THE METHODS:

NB: Before running any of the code, the csv files TweetDatabase_2016.csv and TweetDatabase_2020.csv need to be uploaded to colab. 

A more detailed description of how to run the code is also available within each colab file. Here we also link the code to relevant sections in the paper.   

### Running logistic regression (ML_project_(BOW).ipynb)


### Running CNN (ML_project_(CNN).ipynb)

The 'reddit_worldnews_start_to_2016-11-22.csv' need to be downloaded and uploaded to colab from https://www.kaggle.com/rootuser/worldnews-on-reddit before running. This file was too large to be directly uploade to the git repository. 

1) Run */Imported libraries*
2) Run */Data retrival*, 
     <br/>2.1) Here you also need to define which dataset to run the code on (df_all = tweets2016_df, tweets2020_df or tweets2016_2020_df)
3) Run */Creating a word embedding using word2vec*, 
     <br/>3.1) Here you can also change the dimension of the word2vec (word2vec_dim), currently set to 350
4) Run */Data preproccesing and data split*,
     <br/>4.1) Under */Data Split*, test_size you can define the share of data used for testing
5) Run */Creating the CNN architecture*
     <br/>5.1) Here you can change the architecture of the CNN
6) Run */Training the CNN on the training data*
     <br/>6.1) Here you can change the batch size, epochs and validation share
7) Run */Testing the CNN on the test data*, outputs the results on the test data (accuracy, recall and test data split)

NB: When running the code on a new dataset steps 2, 3, 4, 5, 6 and 7 need to be repeated! 

### Running data analysis (ML_project_(data_analysis))



NB: If you have trouble running any of the code, feel free to reach out at tarjerw@stud.ntnu.no :)
