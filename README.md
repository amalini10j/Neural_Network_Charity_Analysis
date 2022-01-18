# Neural_Network_Charity_Analysis
Repository to create a neural network model and to optimize the same


# Overview of the analysis
The knowledge of machine learning and neural networks, the features in the provided dataset will be used to create a binary classifier that is capable of predicting whether applicants will be successful if funded by Alphabet Soup. The model will also be optimized to get the best possible accuracy.

# Results

## Data Pre Processing 

- What variable(s) are considered the target(s) for your model? - **IS_SUCCESSFUL** is the target variable as the aim is to predict if the investment will be successful or not

- What variable(s) are considered to be the features for your model? - The features used for making the predictions are: **APPLICATION_TYPE, AFFILIATION, CLASSIFICATION, USE_CASE, ORGANIZATION, STATUS, INCOME_AMT, SPECIAL_CONSIDERATIONS, ASK_AMT**. The features will be grouped and encoded to be fed into the model

- What variable(s) are neither targets nor features, and should be removed from the input data? - The variables **EIN** and **NAME** have no impact on the model and are neither features not targets

## Compiling, Training, and Evaluating the Model

#### How many neurons, layers, and activation functions did you select for your neural network model, and why?
- For deliverable 1, two layers were used with 80 and 30 neurons respectively. The activation function used was RELU for the input layers and SIGMOID for the output layer.
- The Keras sequential model was used

#### Were you able to achieve the target model performance? 
- The target model performance of >75% could not be achieved but stayed around 72%

#### What steps did you take to try and increase model performance?

Three attempts were made to increase the model performance but the performance stayed close to 73% and could not be moved to 75%
 
- Attempt 1 : The neurons were increased for the input layers to 90 and 40 (Accuracy - 72.5%)
- Attempt 2 : Two variables, USE_CASE_Other and CLASSIFICATION_Other were dropped and epoch was reduced to 25 (Accuracy - 72.7%)
- Attempt 3 : Retained original feature list as in original deliverable 1 and add one additional hidden layer i.e. total of 3 hidden layers with neurons as 90, 40, 20. Increased epoch from 25 in Attempt 2 to 50 in Attempt 3. (Accuracy - 72.5%)

# Summary

The accuracy of around 72% is not too good but just about acceptable. Anything above 75% would be more reliable. Attempts maybe made to increase the accuracy as follows:

- Keep testing by dropping one variable at a time and checking the accuracy
- The USE CASE variables could be a good candidate to try and see if they are adding noise to the dataset
- The INCOME_AMT variable group could also be considered for eliminating noise
- RELU seems to be the best activation method to be used here as this is a classification problem






