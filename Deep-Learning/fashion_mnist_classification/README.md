## Project Description

In this project we used Keras’s Fashion MNIST dataset, alternatively we can obtain it from [Kaggle](https://www.kaggle.com/datasets/zalando-research/fashionmnist), to build and evaluate several CNN neural network architectures to classify the images into cloth categories.
We first implemented the original LeNet-5 model and evaluated it against the testing set and then we implemented another variation of the LeNet-5 model in which we searched for the hyperparameters for the last fully-connected dense layers using Keras tuner.
The best model corresponding to the optimal hyperparameters found by Keras tuner to find the best hyperparameters was then implemented and evaluated using 5-fold cross validation.
Lastly, we tried transfer learning using two models trained on ImageNet dataset namely InceptionV3 and MobileNet. At the end we conclude by a comparison of these different architectures.
