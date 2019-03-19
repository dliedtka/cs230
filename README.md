Stanford University CS 230 Final Project 
Authors: David Liedtka and Dane Hankamer
Title: Headline Generator

Based on Generating News Headlines with Recurrent Neural Networks by Konstantin Lopyrev, available at https://arxiv.org/pdf/1512.01712.pdf.

Using code base available at https://github.com/udibr/headlines.

Our data pre-processing is done in the dataset/ directory.  We did not upload our data files, as they are rather than large, but the dataset we used is available at https://components.one/datasets/#all-the-news.  That CSV should be placed in the dataset/ directory.  Run generate_pkl.py, which will output data.py in the dataset/ directory.

The notebooks we run are stored in the notebooks/ directory.  With data.pkl in the dataset/ directory, vocabulary-embedding.ipynb will generate embedding files in the notebooks/data directory.  train.ipynb will train for 500 iterations (with each iteration taking approximately 50 minutes on AWS p2.8xlarge instance) and will generate .hdf5 weight files in the notebooks/data directory.  predict.ipynb will make predictions on single manually entered inputs, and it also has the framework for generating heat maps.  Finally, test.ipynb will output BLEU and Levenshtein scores for a testing set.  This testing set will be from the training set if TESTTRAIN is set to True, from the test set if TESTING is set to True, and from the validation set otherwise.  You can toggle the input type between first 50 words, first 25 and last 25 words, first 50 words and last 25 words, etc., by changing the value of MODE (explained in the notebook).

We found that running these notebooks is frequently subject to a lost connection, so we recommend converting them to traditional Python scripts and if running on another server, configuring SSH to keep the server alive.

Our poster and final report will be linked when they are available online.

