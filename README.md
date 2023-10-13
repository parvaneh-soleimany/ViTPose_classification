# ViTPose_classification
This repository provides a classification model on ViTPose data for the Machine learning Intern Assignment for Body.Scratch.

The purpose of this assignment is to classify the different poses based on the 17 key points of the body.

## Libraries Required

The following Python libraries are required to run this project:

- tensorflow
- sklearn
- numpy
- matplotlib

## Getting Started

To get started with this project, follow these steps:

### Clone Repository

To clone this repository to your local machine, use the following command:

git clone https://github.com/username/repository.git

### Install packages

In order to install the required packages you can use the following command:

pip install tensorflow numpy scikit-learn matplotlib 

## Input
Input is the list of numpy arrays which stored heatmap which is the output of [ViTPose](https://github.com/ViTAE-Transformer/ViTPose). The shape of each numpy file is [1, 17, 64, 48] which corresponds to 17 key points in the body. All numpy files in the same folder belong to the same class. There are a total of 17 classes (action_down, action_inside, action_new, ….). 

## The choice of model

In this task I tried to implement a simple vesion of **CNN** which is particularly effective for tasks that involve image data. CNNs are designed to capture the spatial hierarchical structure in data and this feature has made it suitable for the task of pose classification in which the spatial arrangement of the key points in the body is crucial for understanding different poses.



