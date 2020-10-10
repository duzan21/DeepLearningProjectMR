# DeepLearningProjectMR
project for deep learning course 2020 TAU, the project is about Modulation Recognition.<br/>
In this document we will describe how to run the code, train the different models and present our results.

## Table of Contents  
[Notebook Description](#desc)  <br/>
[Train the Network](#train)<br/>
[Analyze the Network](#analyze_train)  <br/>
[Show Results](#results)<br/>

<a name="desc"/>
## Notebook Description
We have one notebook called "Training and Analysis.ipynb" for easy use.

The notebook is divided into parts:
  1.	Hyperparams – there you can set different parameters for running.
  2.  Imports and mount google drive - importing python modules we use and mount google drive. 
  3.  Dataset setup and FFT preprocess - read the dataset from the drive and preprocess the data.
  4.  Setting up the network - there we setting up the network according to networkType and prints it contents.
  5.  Model Training - there you can run logic to train models and save them for later analysis.
      1. Training helper functions - setup some helper functions in training.
      2. Network training loop - setup the actual training loop.
      3. Train network! - train the network, the action parameter should be set to "Training".
  6.  Evaluate and Plot Model Performance - there you can run logic to evaluate one model that was chosen using networkType.
      1. Confusion matrix helper functions - setup some helper functions for confusion matrix.
      2. Model analysis helper functions - setup some helper functions for accuracy analysis.
      3. Perform Single model analysis - analyze current dataset and networkType, show confusion matrix for each SNR, and plot accuracy graph.
  7.  Analyze all models' history, and compare models + data - there you can run several scripts that summeries our results
      1. Analyze all saved models at all epochs - we analyze each network type and dataset and plot accuracy graph.
      2. Compare models and data - show data summary for all of the networkType:
          * print sensativity for each dataset
          * plot accuracy graph for each networkType containing the two dataset results
          * plot accuracy graph of all the network type for each dataset
      3. Plot data time + frequency samples, and modulations probabilities - plot the dataset time and frequency samples in high snr, and show the modulation probabilities for             each data set 

<a name="train"/>
## Train The Network

<a name="analyze_train"/>
## Analyze Trained Network

<a name="results"/>
## Show Summary of The Results
