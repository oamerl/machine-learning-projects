## Project Description

In this project we used [Kaggle’s leaf classification dataset](https://www.kaggle.com/c/leaf-classification/data) to build a MLP neural network model consisting of 3 layers, one input layer, one output layer and one hidden layer to classify the type of the leaf using the mentioned tabular dataset.
We first used Keras tuner to find the best hyperparameters from the provided search space and we then fitted twelve models that corresponds to the best twelve combinations of the hyperparameters, and we plotted their training and validation metrics during training against the number of epochs. Lastly, we plotted a final graph that compares the performance of the twelve fitted models on both the training and the validation sets.

