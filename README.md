# TDT4173-project-group6
Public repository for TDT4173 project, for political affiliation analysis for political tweets, discussed in the paper **Affiliation analysis of political tweets**. All the programming was done in google colab. The most important imported frameworks being; pandas, numpy, sklearn, gensim, and keras.

## PROJECT DESCRIPTION:
This research presents the development and training of 2 different classifiers that based on a labeled training set of tweets identify the party of a US presidential candidate given a new incoming tweet.

We worked with real tweets from the democratic and republican presidential candidates tweeted during the two most recent presidential election years (2016 and 2020).

We used the supervised learning methods logistic regression and convolutional neural network (CNN) in the development of the classifiers:

Before training the data with the logistic regression classifier, the datasets were processed using two NLP methods: Bag-of-words (BOW), and its improved version n-gram, that develop dictionaries of known words and their frequency. Thereafter, logistic regression created coefficients for each word in the dictionary, indicating if its presence in a tweet strengthened the chances of that tweet being republican or democrat. The core idea was that tweets are similar if they had similar content.

CNN on the other hand, used a deep neural network with convolutional layers to detect features in the data. These features were later used for classification. In addition, for CNN, we used the method word2vec to translate words into vectors. 

Both machine learning methods are supervised learning methods, meaning that they use a labeled data set to train.

When fetching tweets, we saved the candidate name, tweet, year (of tweet) and party in a comma-seperated values (csv) (TweetDatabase_2016.csv and TweetDatabase_2020.csv). In total we have 12 826 unique tweets (51.2% Democrat).The tweets were separated into three different datasets. The 2016 dataset only contains tweets from 2016 (6979 tweets, 54.1% Democrat).  The 2020 dataset(47.6% Democrat) only contains tweets from 2020 (5847 tweets).  The 2016-20 dataset is the union of the two other datasets.

## HOW TO RUN THE METHODS:
**NB:** Before running any of the code, the csv files `TweetDatabase_2016.csv` and `TweetDatabase_2020.csv` need to be uploaded to colab. 
A more detailed description of how to run the code is also available within each colab file. Here we also link the code to relevant sections in the paper.   
### Running logistic regression - ML_project_(BOW).ipynb
### Running CNN - ML_project_(CNN).ipynb

The `'reddit_worldnews_start_to_2016-11-22.csv'` need to be downloaded and uploaded to colab from https://www.kaggle.com/rootuser/worldnews-on-reddit before running. This file was too large to be directly uploade to the git repository. 

1) Run `/Imported libraries`
2) Run `/Data retrival`, 
     <br/>2.1) Here you also need to define which dataset to run the code on (`df_all` = `tweets2016_df`, `tweets2020_df` or `tweets2016_2020_df`)
3) Run `/Creating a word embedding using word2vec`, 
     <br/>3.1) Here you can also change the dimension of the word2vec (`word2vec_dim`), currently set to 350
4) Run `/Data preproccesing and data split`,
     <br/>4.1) Under `/Data Split`, `test_size` define the share of data used for testing
5) Run `/Creating the CNN architecture`
     <br/>5.1) Here you can change the architecture of the CNN
6) Run `/Training the CNN on the training data`
     <br/>6.1) Here you can change the batch size, epochs and validation share
7) Run `/Testing the CNN on the test data`, outputs the results on the test data (accuracy, recall and test data split)

**NB:** When running the code on a new dataset steps **2, 3, 4, 5, 6 and 7** need to be repeated! 

### Running data analysis - ML_project_(data_analysis)
**NB:** If you have trouble running any of the code, feel free to reach out at tarjerw@stud.ntnu.no :)
