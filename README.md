# Melanoma Detection Assignment

> In this assignment, you will build a multiclass classification model using a custom convolutional neural network in TensorFlow.

## Table of Contents

- [Overview Business Understanding](#overview-business-understanding)
- [Problem Statement Business Objectives](#problem-statement-business-objectives)
- [Data in depth](#data-in-depth)
- [Approach](#approach)
- [Technologies Used](#technologies-used)
- [Conclusions](#conclusions)

<!-- You can include any other section that is pertinent to your problem -->

## Overview Business Understanding

Melanoma is a type of cancer that can be deadly if not detected early. It accounts for 75% of skin cancer deaths. A solution that can evaluate images and alert dermatologists about the presence of melanoma has the potential to reduce a lot of manual effort needed in diagnosis.

## Problem Statement Business Objectives

To build a CNN based model which can accurately detect melanoma.

### Want to

- Build a multiclass classification model using a custom convolutional neural network in TensorFlow.

## Data in depth

The dataset consists of 2357 images of malignant and benign oncological diseases, which were formed from the International Skin Imaging Collaboration (ISIC). All images were sorted according to the classification taken with ISIC, and all subsets were divided into the same number of images, with the exception of melanomas and moles, whose images are slightly dominant.
The data set contains the following diseases:

- Actinic keratosis
- Basal cell carcinoma
- Dermatofibroma
- Melanoma
- Nevus
- Pigmented benign keratosis
- Seborrheic keratosis
- Squamous cell carcinoma
- Vascular lesion

## Approach

#### Understanding the Dataset

- Defining the path for train and test images

#### Dataset Creation

- Create train & validation dataset from the train directory with a batch size of 32. Also, make sure you resize your images to 180\*180

#### Dataset visualisation

- Create a code to visualize one instance of all the nine classes present in the dataset

#### Model Building & training

- Create a CNN model, which can accurately detect 9 classes present in the dataset. While building the model, rescale images to normalize pixel values between (0,1).
- Choose an appropriate optimiser and loss function for model training
- Train the model for ~20 epochs
- Check if there is any evidence of model overfit or underfit.

#### Model Building & training using Data augmentation strategy to resolve underfitting/overfitting

- Model Building & training on the augmented data
- Create a CNN model, which can accurately detect 9 classes present in the dataset. While building the model, rescale images to normalize pixel values between (0,1).
- Choose an appropriate optimiser and loss function for model training
- Train the model for ~20 epochs
- Check if there is any evidence of model overfit or underfit.

#### Model Building & training on the rectified class imbalance data

- Rectify class imbalances present in the training dataset with Augmentor library.
- Model Building & training on the augmented data
- Handling class imbalances
- Create a CNN model, which can accurately detect 9 classes present in the dataset. While building the model, rescale images to normalize pixel values between (0,1).
- Choose an appropriate optimiser and loss function for model training
- Train the model for ~20 epochs
- Check if there is any evidence of model overfit or underfit.

<!-- You don't have to answer all the questions - just the ones relevant to your project. -->

## Conclusions

Based on our analysis choose a best multiclass classification model using a custom convolutional neural network in TensorFlow.:

- The class rebalance helped in reducing overfititng of the data and thus the loass is beng reduced But it reduced the Acurracy very low
- Initially we tried without the ImageDataGenerator which created data to over fit at high ratio
- Then we introduced dropout and ImageDataGenerator which reduced the over fit

### At last we tried Batch Normalization and Augumentation which really helped in carry forward.

<!-- You don't have to answer all the questions - just the ones relevant to your project. -->

## Technologies Used

- Python
- Numpy
- Panda
- Matplotlib
- Seaborn
- Augmentor
- Tensor
- Keras
- Jupyter Notebook

<!-- As the libraries versions keep on changing, it is recommended to mention the version of library used in this project -->

## Contact

Created by [@pravin691983] - feel free to contact me!

<!-- Optional -->
<!-- ## License -->
<!-- This project is open source and available under the [... License](). -->

<!-- You don't have to include all sections - just the one's relevant to your project -->
