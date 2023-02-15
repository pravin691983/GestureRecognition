# Gesture Recognition

> In this assignment, want to develop a cool feature in the smart-TV that can recognise five different gestures performed by the user which will help users control the TV without using a remote using a custom convolutional neural network in TensorFlow.

## Table of Contents

- [Overview Business Understanding](#overview-business-understanding)
- [Problem Statement Business Objectives](#problem-statement-business-objectives)
- [Data in depth](#data-in-depth)
- [Approach](#approach)
- [Technologies Used](#technologies-used)
- [Conclusions](#conclusions)

<!-- You can include any other section that is pertinent to your problem -->

## Overview Business Understanding

Imagine you are working as a data scientist at a home electronics company which manufactures state of the art smart televisions. You want to develop a cool feature in the smart-TV that can recognise five different gestures performed by the user which will help users control the TV without using a remote.

The gestures are continuously monitored by the webcam mounted on the TV. Each gesture corresponds to a specific command:

- Thumbs up: Increase the volume
- Thumbs down: Decrease the volume
- Left swipe: 'Jump' backwards 10 seconds
- Right swipe: 'Jump' forward 10 seconds
- Stop: Pause the movie

Each video is a sequence of 30 frames (or images).

## Problem Statement Business Objectives

To build a CNN based model which can recognise five different gestures performed by the user which will help users control the TV without using a remote using a custom convolutional neural network in TensorFlow.

### Want to

- Build a want to develop a cool feature in the smart-TV that can recognise five different gestures performed by the user which will help users control the TV without using a remote using a custom convolutional neural network in TensorFlow.

## Data in depth

The training data consists of a few hundred videos categorised into one of the five classes. Each video (typically 2-3 seconds long) is divided into a sequence of 30 frames(images). These videos have been recorded by various people performing one of the five gestures in front of a webcam - similar to what the smart TV will use.

The data is in a zip file. The zip file contains a 'train' and a 'val' folder with two CSV files for the two folders. These folders are in turn divided into subfolders where each subfolder represents a video of a particular gesture. Each subfolder, i.e. a video, contains 30 frames (or images). Note that all images in a particular video subfolder have the same dimensions but different videos may have different dimensions. Specifically, videos have two types of dimensions - either 360x360 or 120x160 (depending on the webcam used to record the videos). Hence, you will need to do some pre-processing to standardise the videos.

Each row of the CSV file represents one video and contains three main pieces of information - the name of the subfolder containing the 30 images of the video, the name of the gesture and the numeric label (between 0-4) of the video.

## Approach

#### Understanding the Dataset

- Defining the path for train and test images

#### Generator Creation

- The generator should be able to take a batch of videos as input without any error. Steps like cropping, resizing and normalization should be performed successfully.

#### Visualize the Model History Result

- Visualize the Model History Result

#### Model Building & training

- Develop a model that is able to train without any errors which will be judged on the total number of parameters (as the inference(prediction) time should be less) and the accuracy achieved. As suggested by Snehansu, start training on a small amount of data and then proceed further.

#### Write up

- This should contain the detailed procedure followed in choosing the final model. The write up should start with the reason for choosing the base model, then highlight the reasons and metrics taken into consideration to modify and experiment to arrive at the final model.

<!-- You don't have to answer all the questions - just the ones relevant to your project. -->

## Conclusions

Based on our Experiment using generator with and without augmented data and our analysis:

We can see LSTM networks combat the RNN's vanishing gradients or long-term dependence issue. Gradient vanishing refers to the loss of information in a neural network as connections recur over a longer period. In simple words, LSTM tackles gradient vanishing by ignoring useless data/information in the network.

Here is the details result of CNN-LSTM Model:

- Total Params: 1,657,445
- Training Accuracy: 0.9604
- Validation Accuracy: 0.8300

Hence, we considered the CNN-LSTM model is the best model, with below given weight for model testing.

The best weights of CNN-LSTM: model-00020-0.14990-0.96003-0.64083-0.83000.h5 (20 MB).

## Technologies Used

- Python
- Numpy
- Panda
- Matplotlib
- Seaborn
- Augmentor
- Tensor
- Keras
- OpenCV
- Jupyter Notebook

<!-- As the libraries versions keep on changing, it is recommended to mention the version of library used in this project -->

## Contact

Created by [@pravin691983] - feel free to contact me!

<!-- Optional -->
<!-- ## License -->
<!-- This project is open source and available under the [... License](). -->

<!-- You don't have to include all sections - just the one's relevant to your project -->
