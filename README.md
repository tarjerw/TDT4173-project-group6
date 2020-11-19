# TDT4173-project-group6
Public repository for TDT4173 project, for political affiliation analysis for political tweets, discussed in the paper **Affiliation analysis of political tweets**. All the programming was done in google colab. The most important imported frameworks being; pandas, numpy, sklearn, gensim, and keras.

## PROJECT DESCRIPTION:
This research presents the development and training of 2 different classifiers that based on a labeled training set of tweets identify the party of a US presidential candidate given a new incoming tweet.

We worked with real tweets from the democratic and republican presidential candidates tweeted during the two most recent presidential election years (2016 and 2020).

We used the supervised learning methods logistic regression and convolutional neural network (CNN) in the development of the classifiers:

Before training the data with the logistic regression classifier, the datasets were processed using two NLP methods: Bag-of-words (BOW), and its improved version n-gram, that develop dictionaries of known words and their frequency. Thereafter, logistic regression created coefficients for each word in the dictionary, indicating if its presence in a tweet strengthened the chances of that tweet being republican or democrat. The core idea was that tweets are similar if they had similar content.

CNN on the other hand, used a deep neural network with convolutional layers to detect features in the data. These features were later used for classification. In addition, for CNN, we used the method word2vec to translate words into vectors. 

Both machine learning methods are supervised learning methods, meaning that they use a labeled data set to train.

When fetching tweets, we saved the candidate name, tweet, year (of tweet) and party in csv files (TweetDatabase_2016.csv and TweetDatabase_2020.csv). In total we have 12 826 unique tweets (51.2% Democrat).The tweets were separated into three different datasets. The 2016 dataset only contains tweets from 2016 (6979 tweets, 54.1% Democrat).  The 2020 dataset(47.6% Democrat) only contains tweets from 2020 (5847 tweets). The 2016-20 dataset is the union of the two other datasets.

## HOW TO RUN THE METHODS:
**NB:** Before running any of the code, the csv files `TweetDatabase_2016.csv` and `TweetDatabase_2020.csv` need to be uploaded to colab. 
A more detailed description of how to run the code is also available within each colab file. Here we also link the code to relevant sections in the paper.   
### Running logistic regression - ML_project_(BOW).ipynb

The 3rd party file `TableIt.py` present in the git repository, must be uploaded to colab before running (in addition to the two .csv files). This file was used to display python resuls in tables in a clear and simple manner, while minimizing the amount of unnecessary code. 

1. Run `/Imported libraries` to import all libraries,
2. Run `/Data retrieval` to retrieve data from CSV files and create 3 datasets, 
3. Run `/Splitting data` to split data into train and test sets, 
     1. Here you can alter the test set size (default is 20%) and see the distribution of tweets into the different sets
4. Run `/Transforming/Creating BOW model` to transform the data with the BOW method,
5. Run `/Transforming/Creating N-Gram model` to transform the data with the N-Gram method
     1. Here you can change the min and max length of tokens (default is 1 to 4 words)
6. Run `/Logistic regression using BOW` to train and test a logistic regression on the transformed BOW data 
     1. In `cd /Tunning hyperparameter C` you see how the models' accuracies flucutuate with different C values
     2. In `cd /Accuracy results` you see the models' accuracies given a fixed regularization value C for all 3 datasets
7. Run `/Logistic regression using N-Gram` to train and test a logistic regression on the transformed N-Gram data 
     1. Same as in step 6 but for N-Gram
8. Run `/Cross validation on both models` to verify the level of overfitting in the data
     1. Here you can alter the number of folds in the cross validation function
9. Run `/Confusion matrix` to see additional results, that are discussed in the paper


### Running CNN - ML_project_(CNN).ipynb

The `'reddit_worldnews_start_to_2016-11-22.csv'` need to be downloaded and uploaded to colab from https://www.kaggle.com/rootuser/worldnews-on-reddit before running. This file was too large to be directly uploade to the git repository. 

1. Run `/Imported libraries`
2. Run `/Data retrieval`, 
     1. Here you also need to define which dataset to run the code on (`df_all` = `tweets2016_df`, `tweets2020_df` or `tweets2016_2020_df`)
3. Run `/Creating a word embedding using word2vec`, 
     1. Here you can also change the dimension of the word2vec (`word2vec_dim`), currently set to 350
4. Run `/Data preproccesing and data split`,
     1. Under `/Data Split`, `test_size` define the share of data used for testing
5. Run `/Creating the CNN architecture`
     1. Here you can change the architecture of the CNN
6. Run `/Training the CNN on the training data`
     1. Here you can change the batch size, epochs and validation share
7. Run `/Testing the CNN on the test data`, outputs the results on the test data (accuracy, recall and test data split)

**NB:** When running the code on a new dataset steps **2, 3, 4, 5, 6 and 7** need to be repeated! 

### Running data analysis - ML_project_(data_analysis)

1. Run `/Imported libraries`
2. Run `/Data retrieval`, 
3. Run `/Number of democrat and republican tweets`, 
4. Run `/Number of tweets per candidate`,
5. Run `/Comparing frequency of words between parties`
    1. Here you can run the function `WordtoFrequency()` that counts the number of occurences of a given word in republican and democrat tweets.




**NB:** If you have trouble running any of the code, feel free to reach out at tarjerw@stud.ntnu.no :)
