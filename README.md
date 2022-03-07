# Neural_Network_Charity_Analysis

## Overview
In this challenge we'll use the features in the provided dataset to help Beks create a binary classifier that is capable of predicting whether applicants will be successful if funded by Alphabet Soup. We'll first create a basic neural network then use optimization techniques to try and get the accuracy score of our model as high as possible.

## Results
### Data Preprocessing
* What variable(s) are considered the target(s) for your model?
The target for our model is the IS_SUCCESSFUL variable
* What variable(s) are considered to be the features for your model?
The variables that are considered as the features for our model are: 
APPLICATION_TYPE, AFFILIATION, CLASSIFICATION, USE_CASE, ORGANIZATION, STATUS, INCOME_AMT, SPECIAL_CONSIDERATIONS, ASK_AMT.
* What variable(s) are neither targets nor features, and should be removed from the input data?
The variables that can be removed from our model because they are neither targets nor features are EIN and NAME because they only identify the data.
### Compiling, Training, and Evaluating the Model
* How many neurons, layers, and activation functions did you select for your neural network model, and why?
For our neural network model there is 1 input and 2 hidden layers(80 and 30 nodes respectfully). The activation functions that was used for our hidden layers is the ReLu function because it looks at positive nonlinear input data for classification or regression. The sigmoid function was used for the output layer because values are normalized to a probability between 0 and 1, which is ideal for binary classification.
![Picture 1](https://user-images.githubusercontent.com/41974323/157127046-61170fca-e3a7-4b80-913a-58085f559218.PNG)

* Were you able to achieve the target model performance?
Our target model performance was 75% accuracy but I was only able to get it up to 72.69%.
![Picture 2](https://user-images.githubusercontent.com/41974323/157127248-d032fb55-bdc9-4ac0-9a34-5ae8a2a84a07.PNG)

* What steps did you take to try and increase model performance?
Several attempts were made to try and increase model performance:
  * Removing an additional column (INCOME_AMT and ASK_AMT) to take away any noisy data.
  * Increasing the number of neurons in each hidden layer (several attempts ranging from 80 to 200)
  * Adding a third hidden layer to the neural network
  * Changing the activation function to see if there is any change in accuracy (changing either hidden layer or output layer resulted in lower scores)
  * Increasing number of epochs
  * Making changes to bins 
### Summary
The results of our analysis show that this may not be the best model to use with the current data, perhaps with more data we would be able to acquire a better accuracy.
With the current data my recommendation would be to use the random forest model because of how well it handles classification problems. Random forest models also have a high level of robustness and scalability that makes it easy to interpret while also being able to handle outliers and nonlinear data well.
