# Deep Learning Challenge

## Overview
The objective of this analysys is to develop a neural network model to predict if future applicants funded by the Alphabet Soup Charity organisation will be successful. To achieve this goal, a dataset of slightly more than 34,000 organizations that have received funding in the past was used to train and test the model.

The Model consisted of one base model and three optimisation models to try and achieve an accuracy target score of 75% or higher.

## Results
### Data Preprocessing:
* The target variable used in the model was "IS_SUCCESSFUL".
* The Feature variables used in the model were:
  * APPLICATION_TYPE
  * AFFILIATION
  * CLASSIFICATION
  * USE_CASE
  * ORGANIZATION
  * STATUS
  * INCOME_AMT
  * SPECIAL_CONSIDERATIONS
  * ASK_AMT
 * The variables which were dropped from the dataset were "EIN"	and "NAME"
 
 ### Compiling, Training, and Evaluating the Model:
* Base Model:
  * created bins for the APPLICATION_TYPE and CLASSIFICATION variables
  * 10 neurons per layer
  * 2 layers total
  * activation functions used were 'relu" for hidden layers and "sigmoid" for output layer
  
  The base model gave a result of Loss: 0.5601314306259155 and Accuracy: 0.7278425693511963. This did not meet the target of at least 75% accuracy.

* Optimisation attempt 1:
  * created more bins for the APPLICATION_TYPE and CLASSIFICATION variables
  * 10 neurons per layer
  * 2 layers total
  * activation functions used were 'relu" for hidden layers and "sigmoid" for output layer
  
  Creating more bins did not seem to have much of an effect in the outcome.
  Loss: 0.5543999075889587, Accuracy: 0.7291545271873474

* Optimisation attempt 2:
  * dropped the 'SPECIAL_CONSIDERATIONS' and 'STATUS' variables also 
  * 10 neurons per layer
  * 2 layers total
  * activation functions used were 'relu" for hidden layers and "sigmoid" for output layer
  
  Reducing the number of variables did not increase the accuracy either. Loss: 0.5548793077468872, Accuracy: 0.7275510430335999 

* Optimisation attempt 3:
  * increase neurons to 27 per layer
  * added 2 extra layers so total of 4 layers
  * increased epochs to 200
  * activation functions changed to 'tanh" for hidden layers and "sigmoid" for output layer
  
  Even changing multple Hyperparameters did not increase the accuracy. Loss: 0.5642755031585693, Accuracy: 0.7236151695251465
  
## Summary
Having tried multiple methods to try to reach the target score of at least 75% accuracy I have come to the conclusion that a completely different machine learning algorithm such as Random Forest may increase the accuracy score, It is an ensemble learning method that combines multiple decision trees to improve the accuracy and robustness of the model. 



