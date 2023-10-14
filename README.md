# ViTPose_classification
This repository provides a classification model on ViTPose data for the Machine learning Intern Assignment for Body.Scratch.

The purpose of this assignment is to classify the different poses based on the 17 key points of the body.

## Libraries Required

The following Python libraries are required to run this project:

- tensorflow
- sklearn
- numpy
- os


## Getting Started

To get started with this project, follow these steps:

### Clone Repository

To clone this repository to your local machine, use the following command:

git clone https://github.com/username/repository.git

### Install Packages

In order to install the required packages you can use the following command:

pip install tensorflow numpy scikit-learn matplotlib 

## Input
Input is the list of numpy arrays which stored heatmap which is the output of [ViTPose](https://github.com/ViTAE-Transformer/ViTPose). The shape of each numpy file is [1, 17, 64, 48] which corresponds to 17 key points in the body. All numpy files in the same folder belong to the same class. There are a total of 17 classes (action_down, action_inside, action_new, ….). 

## The Choice of Model

In this task I tried to implement a simple vesion of **CNN** which is particularly effective for tasks that involve image data. CNNs are designed to capture the spatial hierarchical structure in data and this feature has made it suitable for the task of pose classification in which the spatial arrangement of the key points in the body is crucial for understanding different poses.

After fitting the model, it showed a perfect accuracy of 1.00 on the training data which could be a sign of overfitting. But the accuracy on the test set was also equal to 1.00 and it shows excellent generalization, that means the model effectively learned the patterns of the data rather than memorizing noise from the training set.

## Model Deploy

To deploy the implemented model for predictive analysis, follow these steps in the provided order:

- Ensure that all necessary dependencies are installed. 

- Ensure that the Unseen Data is organized in a directory structure. This directory should contain .npy files representing the data samples.

- Open the 'prediction.ipynb' notebook in which you should modify the 'data_dir' variable to specify the path to the directory containing the unseen data.

- Run the notebook from the scratch (be sure the model file 'trained_model.h5' is included in the current folder) and at the last cell you can see the predicted class of your unseen data.

## Limitations and Improvements

Speaking of the CNN limitations, I can mention CNNs typically require large amounts of labeled training data (thousands of images for each class) to perform well. Acquiring and labeling large datasets can be expensive and time-consuming, especially for specific domains. In our experiment we could feed reasonable amount of input data to the model but it is not always the case.
In scenarios where obtaining a large labeled dataset is challenging, techniques such as transfer learning, data augmentation, and semi-supervised learning can be employed to make the most of the available data and improve the model's performance. 

One of the limitation of the code provided is that it does not explore hyperparameter tuning. Adjusting parameters like learning rate, batch size, and the number of epochs could significantly impact the model's performance. For further improvement of the model we can use some tuning packages like KerasTuner.

The code evaluates the model based on simple accuracy. While accuracy is a useful metric, for imbalanced datasets or when different misclassification errors have different costs, other metrics such as precision, recall, and F1-score are crucial that can improve the comprehensiveness of assessment.

Consequently, in the code just one classification method is hired which does not allow to compare different methods and choose the best one that fits the problems well. One improvement of the code provided can be implementing different methods.

Consequently, the current code employs a single classification method, limiting the ability to compare various approaches and select the best one for addressing the specific issue at hand. An improvement to the existing code could involve the implementing of multiple methods for a comprehensive evaluation.


