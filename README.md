# deep-learning-challenge
## week 21
# Overview  
Build a neural network to predict the outcome of campaigns for AlphabetSoup foundation using a CSV file as training data.  

# Results  
## Data Preprocessing  
Target variable: IS_SUCCESSFUL  
Feature variables: APPLICATION_TYPE, AFFILIATION, CLASSIFICATION, USE_CASE, ORGANIZATION, STATUS, INCOME_AMT, SPECIAL_CONSIDERATIONS, ASK_AMT
Variables to be removed because they are neither target nor features: EIN,NAME  

Number of neurons: 10, 5, 1  
Number of layers: 3  
Acitvation functions: relu, sigmoid  
Reason for choice: the input data is quite small around with 9 features and 34,300 rows, so we do not need a complicated model. And relu as the activation functions in the hidden layers because it helps to mitigate the vanishing gradient problem during backpropagation. signmoid is chosen for the activation function for the output layer because it is a good choice for binary classification problems, where the output can be interpreted as the probability of the input data belonging to the positive class.

I was not able to achieve the target model performance (75%) but only reached 73%.  

The steps i took to increase accuracy include:
<ol>
 <li>Removing outliers in ASK_AMT during preprocessing.</li>
 <li>Increasing the number of neurons in the hidden layer from 10 to 80.</li>
 <li>Increasing the number of epochs from 100 to 150.</li>
 <li>Adding one more hidden layer.</li>
</ol>

# Summary  
The model seems to reach a plateau accuracy of 73% as implementing all the steps above did not increase the accuracy much, however it increases the loss, meaning it could be overfitting. If we had more time, we may explore a model with 9 neurons in each hidden layer to match the number of features to see if it can increase the accuracy, because increasing the number of neuron does not seem to help so we should try decreasing it.
