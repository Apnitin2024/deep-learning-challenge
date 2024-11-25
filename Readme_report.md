# Deep Learning Model for Predicting Funding Success in Alphabet Soup Initiative

## Overview of the Analysis

The purpose of this analysis is to create a binary classification model using deep learning techniques to predict if an organization funded by Alphabet Soup will be successful in their venture. The model utilizes a dataset of over 34,000 organizations that have received funding from Alphabet Soup, containing metadata about each organization.

## Results

### Data Preprocessing

- **Target variable(s) for the model:** The target variable for the model is `IS_SUCCESSFUL`.
- **Feature variable(s) for the model:** The feature variables for the model include `APPLICATION_TYPE`, `AFFILIATION`, `CLASSIFICATION`, `USE_CASE`, `ORGANIZATION`, `STATUS`, `INCOME_AMT`, `SPECIAL_CONSIDERATIONS`, and `ASK_AMT`. 
- **Variable(s) removed from the input data:** The `EIN` and `NAME` columns were removed from the input data as they are identification columns and not useful as features or targets.

- **Feature variable** `NAME` has been brought back in the last model.

### Compiling, Training, and Evaluating the Model

- **Neurons, layers, and activation functions selected for the neural network model and rationale:** The model consists of three hidden layers with 80, 30, and 1 neurons, respectively, and ReLU activation functions. The output layer uses a sigmoid activation function for binary classification. The structure was chosen to provide a balance between complexity and the potential for overfitting, while maintaining the ability to learn complex patterns in the data.
This model did not achive desired accuracy of 75%.
The accuracy achived was 72.3%.

**In this project**, we tested four different models. The first three models in Starter_code.ipynb are excluded the EIN and NAME columns while applying different numbers of neurons, layers, and binning adjustments as follows:
****Attempt 1****: Kept the same structure but varied the number of neurons in each layer and increased the epochs from 50 to 100.
Accuracy increased slightly to 72.5%.
****Attempt 2****: Optimized the structure using Keras Tuner.
Allowed the activation function to choose between ReLU, sigmoid, and tanh.
Kept sigmoid as the activation function for the final layer.
Allowed the number of neurons to range from 6 to about 75.
Accuracy improved  to 73.14%.
****Attempt 3****: Used fewer neurons (less than the number of features) with a sigmoid activation function for non-input layers.
Accuracy decreased to 72.7%.


##### The details of the 3 first attempts are provided in the Starter_code.ipynb.
* Attempt4: the final attempt that can be find in the AlphabetSoupCharity_Optimisation.ipynb has the best accuracy of 78.56%.


Our **Feature variable(s) for the model:** The feature variables for the model include `APPLICATION_TYPE`, `AFFILIATION`, `CLASSIFICATION`, `USE_CASE`, `ORGANIZATION`, `STATUS`, `INCOME_AMT`, `SPECIAL_CONSIDERATIONS`, `NAME` and `ASK_AMT`. and 
**Target variable(s) for the model:** The target variable for the model is `IS_SUCCESSFUL`. The model consists of three hidden layers with 14, 7, and 1 neurons, respectively, The output layer uses a sigmoid activation function for binary classification and used Relu for other layers.


- **Achievement of the target model performance:** The model achieved a target accuracy of 78.5% on the fourth attempt. However, several optimization attempts were undertaken, involving adjustments to the input data, changes to the neural network architecture, and modifications to the training regimen.


- **Steps taken in attempts to increase model performance:** To increase model performance, the following steps were taken:

  -Eliminating additional non-essential columns from the input dataset.
  -Adjusting rare occurrences in columns by creating more bins and modifying the range of values within each bin.
  -Increasing the number of neurons in a hidden layer.
  -Modifying the network structure by adding or removing hidden layers.
  -Experimenting with different activation functions for the hidden layers.
  -Tweaking the training process by increasing or reducing the number of epochs.


### Summary

The deep learning model successfully attained an accuracy of 78.56% in predicting the success of organizations supported by Alphabet Soup. This outcome was achieved through various optimization strategies, such as improving data preprocessing and modifying the neural network architecture.

