# TDT4173-project-group6
public repository for TDT4173 project, for political affiliation analysis for political tweets. All the programing is done in google colab. The most important imported frameworks being; pandas, numpy,sklearn, gensim, and keras.

## PROJECT DESCRIPTION:
This paper presents the development and training of classifiers that based on a labeled trainingset of tweets identifies political affiliation of a US presidential candidate based on a new,  single tweet.

For  developing  and  training  such  a  classifier  we  will  be  working  with  real  life  tweets  (strings)from the democratic and republican presidential candidates tweeted during the two most recentpresidential election years (2016 and 2020).

For  developing  the  classifier  we  will  be  using  the  supervised  learning  methods;Bag-of-words(BOW), its improved versionn-gram, andConvolutional neural network (CNN). Bag-of-words, and n-gram, develops a dictionary of known words (and phrases) and detect their presencein different settings.  It’s core idea is that things are similar if they have similar content (e.g., verymany republican tweets uses the phrase ”sleepy Joe” or ”crocked Hillary”).  CNN on the otherhand, uses a deep neural network with convolutional layers to detect features in the data, whichcan be used for classification.  All three methods are supervised learning methods, which meansthey  will  be  using  a  dataset  of  labeled  data  to  train.   In  addition  we  will  be  using  the  method Word2Vec, which is used to translate words into vectors, in which the distance between vectorssignify the similarity between their corresponding words.

For our methods we want to have real life tweets, with the candidate name, tweet, year (of tweet)and party, as seen in figure 1.  All these values are saved in a comma-seperated values (csv) (TweetDatabase_2016.csv and TweetDatabase_2020.csv).  In addition each tweet is also assigned a unique ID. In total we have 12 826 unique tweets(51.2% Democrat).

## HOW TO RUN THE METHODS:

To run the files the two csvs TweetDatabase_2016.csv and TweetDatabase_2020.csv need to be uploaded to colab. In addition, for training the word2vec model in ML_project_(CNN).ipynb, the 'reddit_worldnews_start_to_2016-11-22.csv' need to be downloaded and uploaded to colab from https://www.kaggle.com/rootuser/worldnews-on-reddit. This file was too large to be directly uploade to the git repository. 

1) Data analytics, of the dataset is done in the file ML_project_(data_analysis). 
     <br/>1.1) Remember to upload TableIt.py to colab (in addition to TweetDatabase_2016.csv and TweetDatabase_2020.csv) to print out the tables.

2) Running logistic regression using bag-of-words and n-gram is done in the file ML_project_(BOW).ipynb.
    <br/>2.1) Remember to upload TableIt.py to colab (in addition to TweetDatabase_2016.csv and TweetDatabase_2020.csv) to print out the tables.

3) Running the CNN is done in the file ML_project_(CNN).ipynb. 
    <br/>3.1) Under retrieve data, you need to set df_all equal to the dataset which you intend to use, (tweets2016_df, tweets2020_df, or tweets2016_2020_df)
    <br/>3.2) the dimension of the word2vec embedding is defined in the variable word2vec_dim, which is set to 350
    <br/>3.3) the number of epochs, and batch size is defined under "train the CNN", which are set to 40 and 400 respectively. 
    
