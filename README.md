# Neural_Network_Charity_Analysis

## Overview
Using Machine Learning and Neural Networks for this project, I used the features in the dataset to create a binary classifier that will help to predict if the applicants that will be funded by a Charitable organization called Alphabet Soup will be successful. For this analysis we had a dataset containing various measures on 34,000 organizations that have been funded by Alphabet Soup. This project compromised of the following 3 steps:

Preprocessing the data for the neural network
Compile, Train and Evaluate the Model
Optimizing the model

## Results
### Data Preprocessing
- Variable that was considered as the target for my model: IS_SUCCESSFUL Column
- Variables that were considered features for my model: Every Column except for IS_SUCCESSFUL which is our target and the ones we will drop
- Variable that were neither targets or features for the dataset: Columns that I dropeed are EIN, NAME because they will have little to no impact om our outcome

### Compiling, Training and Evaluating the Model

The number of neurons, layers, and activation functions I selected for my neural network model:

- For my neural network model I had 2 hidden layers. My first layer had 80 neurons, the second has 30 there is also an output layer. The first and second hidden layer have the "relu" activation function and the activation function for the output layer is "sigmoid."

<img width="749" alt="Screen Shot 2022-07-17 at 10 44 48 PM" src="https://user-images.githubusercontent.com/100812308/179438096-4996f396-4f05-417a-8023-f1204d6fc322.png">

Was the model able to achieve the target model performance?

- The model was not able to reach the target 75%. The accuracy for my model was 69%.

<img width="561" alt="Screen Shot 2022-07-17 at 10 46 44 PM" src="https://user-images.githubusercontent.com/100812308/179438266-8b2004d2-c41f-47cd-80b8-3489d702c9d7.png">

The steps taken to try and increase model performance

Attempt 1: Removed additional feature, that is the 'USE_CASE' column. Rest of the model components stayed the same, however model accuracy went down to 63%.

<img width="541" alt="Screen Shot 2022-07-17 at 10 48 17 PM" src="https://user-images.githubusercontent.com/100812308/179438464-2899ebc2-4d47-48f6-8ff5-5a348015ea0b.png">

<img width="583" alt="Screen Shot 2022-07-17 at 10 48 53 PM" src="https://user-images.githubusercontent.com/100812308/179438475-c389b859-01aa-438c-a1ad-4742c2c01266.png">


Attempt 2: Adding Additional neurons to hidden layers and additional hidden layers are added. The accuracy went down again, this time it was 52%.

<img width="635" alt="Screen Shot 2022-07-17 at 10 50 20 PM" src="https://user-images.githubusercontent.com/100812308/179438548-5c98de64-3ae6-44ab-839b-ce27b9bf902a.png">

Attempt 3: Changing activation function of output layer from "sigmoid" to "tanh." The accuracy of the model went down even more to 46%.

<img width="610" alt="Screen Shot 2022-07-17 at 10 51 21 PM" src="https://user-images.githubusercontent.com/100812308/179438631-8ec4ec46-5c83-4e02-acc4-b7d07ec46d7e.png">

## Summary
The model ended up with the accuracy score of 50% after optimization. The initial neural network had a accuracy score of 69%. This loss in accuracy can be explained from the fact that the model overfitted. Furthermore, we could further also optimize our neural network by removing more features or simply adding more data to the dataset to increase accuracy. Since our accuracy score was not particularly up to the standard with neural networks, we could have used the Random Forest classifiers. This is because random forest is a robust and accurate model due to their sufficient number of estimators and tree depth. Also the random forest models have a faster performance than neural networks and could have avoided the data from being overfitted.
