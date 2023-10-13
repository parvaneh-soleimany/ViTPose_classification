# ViTPose_classification
This repository provides a classification model on ViTPose data for the Machine learning Intern Assignment for Body.Scratch.

The purpose of this assignment is to classify the different poses based on the 17 key points of the body.

## Libraries Required

The following Python libraries are required to run this project:

- tensorflow
- sklearn
- numpy
- matplotlib

In order to install the packages you can use the command bellow:
pip install tensorflow numpy scikit-learn matplotlib 

## Input
Input is the list of numpy arrays which stored heatmap which is the output of [ViTPose](https://github.com/ViTAE-Transformer/ViTPose). The shape of each numpy file is [1, 17, 64, 48] which corresponds to 17 key points in the body. All numpy files in the same folder belong to the same class. There are a total of 17 classes (action_down, action_inside, action_new, ….). 

## Installation
