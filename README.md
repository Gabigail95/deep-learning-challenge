# deep-learning-challenge

# Overview of the Analysis
The purpose of this analysis is to develop a neural network model to predict the success of applications for funding by Alphabet Soup, a nonprofit foundation. The goal is to use machine learning techniques to identify patterns and factors that influence whether an application is successful. This will help the organization make data-driven decisions to improve their application evaluation process.

# Results

Data Preprocessing
-	Target Variable(s):
  IS_SUCCESSFUL: This variable indicates whether an application for funding was successful (1) or not (0).
-	Feature Variable(s):
  All other columns after one-hot encoding except EIN and NAME, which include various categorical and numerical data related to the application.
-	Removed Variable(s):
  EIN: Employer Identification Number, a unique identifier for organizations.
  NAME: The name of the organization. These variables are not predictive of the success of an application and are therefore removed from the dataset.

Compiling, Training, and Evaluating the Model
-	Neurons, Layers, and Activation Functions:
- Model 1:
    Layers: 3
    Dense layer with 80 neurons, ReLU activation
    Dense layer with 30 neurons, ReLU activation
    Dense output layer with 1 neuron, Sigmoid activation
- Optimized Model:
    Layers: 4
  	Dense layer with 80 neurons, ReLU activation
    Dropout layer with 0.2 rate
    Dense layer with 30 neurons, ReLU activation
    Dense output layer with 1 neuron, Sigmoid activation
- The ReLU activation function is used for hidden layers to introduce non-linearity, and Sigmoid activation is used in the output layer for binary classification.
-	Model Performance:
    Original Model:
      Loss: 0.5603
      Accuracy: 0.7302
    Optimized Model:
      Loss: 0.5616
      Accuracy: 0.7264
-	Steps to Increase Performance:
  Introduced a Dropout layer to prevent overfitting.
  Used EarlyStopping to monitor validation loss and stop training when the model stops improving.
  Implemented ModelCheckpoint to save the best model during training.

# Summary
The deep learning model developed for predicting the success of charity applications achieved an accuracy of approximately 73% in the original model and slightly lower accuracy in the optimized model. The use of optimization techniques such as dropout layers, early stopping, and model checkpointing did not lead to significant performance improvement.

