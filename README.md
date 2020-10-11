# Deep Learning Project Modulation Recognition
project for deep learning course 2020 TAU, the project is about Modulation Recognition. <br/>
In this document we will describe how to run the code, train the different models and present our results. <br/>

Have Fun!

prerequisite: 
1. you have access to a drive with the dataset pkl.
2. the folder project_203142260_305773673 is in your drive. <br/>
   if not: <br/>
   1. Right click on project_203142260_305773673 shared folder in your drive.  <br/>
   2. press Add shortcut to drive, choose “My Drive” than press ADD SHORTCUT.  <br/>
   3. This will enable google Colab to access the shared folder and the rootDir variable to be valid. <br/>

## Table of Contents  
[Notebook Description](#desc)  <br/>
[Train the Network](#train)<br/>
[Analyze the Network](#analyze_train)  <br/>
[Show Results](#results)<br/>
[Appendix A - dataset](#dataset)<br/>
[Authors](#authors)<br/>


## <a name="desc"/> Notebook Description
We have one notebook called "Training and Analysis.ipynb" for easy use.

The notebook is divided into parts:
  1.	Hyperparams – there you can set different parameters for running.
      1. action:
        1. "Training" - train the network
        2. "Analysis" - load trained network
  2. networkType:
      1. CNN2 - the architecture used in "Convolutional Radio Modulation Recognition
Networks 2016"
        2. CNN2_switch_kernels - the CNN2 architecture with switched kernel - from (1,3) (2,3) to (2,3) (1,3).
        3. CNN2_FFT - the CNN2 architecture with FFT and time samples as input.
        4. CNN2_ENSEMBLE - ensemble of the fft and time samples using CNN2 architecture
        5. VGG - the CNN architecture inspired by VGG.
        6. VGG_ENSEMBLE - ensemble of the fft and time samples using VGG architecture
      3. dataSet:
        1. 2016.04C.multisnr - the old data set used in "Convolutional Radio Modulation Recognition
Networks 2016"
        2. RML2016.10a_dict - the new data set that supersedes 2016.04C.multisnr
  2.  Imports and mount google drive - importing python modules we use and mount google drive. 
  3.  Dataset setup and FFT preprocess - read the dataset from the drive and preprocess the data.
  4.  Setting up the network - according to networkType and prints it contents.
  5.  Model Training - run logic to train models and save them for later analysis.
      1. Training helper functions - setup some helper functions in training.
      2. Network training loop - setup the actual training loop.
      3. Train network! - train the network, the action parameter should be set to "Training".
  6.  Evaluate and Plot Model Performance - there you can run logic to evaluate one model that was chosen using networkType.
      1. Confusion matrix helper functions - setup some helper functions for confusion matrix.
      2. Model analysis helper functions - setup some helper functions for accuracy analysis.
      3. Perform Single model analysis - analyze current dataset and networkType, show confusion matrix for each SNR, and plot accuracy graph.
  7.  Analyze all models' history, and compare models + data - there you can run several scripts that summarize your results
      1. Analyze all saved models at all epochs - we analyze each network type and dataset and plot accuracy graph.
      2. Compare models and data - show data summary for all of the networkTypes:
          * print sensitivity for each dataset
          * plot accuracy graph for each networkType containing the two dataset results
          * plot accuracy graph of all the network type for each dataset
      3. Plot data time + frequency samples, and modulations probabilities - plot the dataset time and frequency samples in high snr, and show the modulation probabilities for each data set 


## <a name="train"/> Train The Network
First in the Hyperparams you should config:
1.	action: "Training"
2.	networkType: your desired network type.
3.  dataSet: your desired dataset.
Once your configuration is set, run the following cells: 
1. Hyperparams -> Imports and mount google drive -> Dataset setup and FFT preprocess -> Setting up the network -> Model Training
After training is finished, your model is ready to be evaluated. To evaluate it run the following commands:
Evaluate and Plot Model Performance -> this will plot the confusion matrices and plot accuracy graph, as calculated on the entire test set.

## <a name="analyze_train"/> Analyze Trained Network
First in the Hyperparams you should set:
1.	action: "Analysis"
2.	networkType: your desired network type.
3.  dataSet: your desired dataset.
Once your configuration is set, run the following cells: 
1. Hyperparams -> Imports and mount google drive -> Dataset setup and FFT preprocess -> Setting up the network
This will result in having a configurable environment, so you can run:
Evaluate and Plot Model Performance -> will show confusion matrices and plot accuracy graph, as calculated on the entire test set.

## <a name="results"/> Show Summary of The Results
First in the Hyperparams you should set:
1.	action: "Analysis"
2.	networkType: your desired network type.
3.  dataSet: your desired dataset.
Once your configuration is set, run the following cells: 
1. Hyperparams -> Imports and mount google drive -> Dataset setup and FFT preprocess -> Setting up the network
This will result in having a configurable environment, so you can run all the cells under:
Analyze all models' history, and compare models + data -> will analyze calculate accuracies for all epochs, and show a summary of the results

## <a name="dataset"/> Obtaining the dataset
the datasets can be downloaded from: https://www.deepsig.ai/datasets <br/>
our simulation is suitable to: 2016.04C, 2016.10A datasets. <br/>
you should upload the "pkl" files into your drive and update the rootDir variable in hyper parameters.

## <a name="authors"/> Authors
Noam Miron & David Uzan
