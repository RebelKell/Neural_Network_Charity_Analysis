# Neural Network Charity Analysis

## Overview
In this analysis we attempt to use neural networks to create a binary classifier that predicts whether applicants will be successful if they receive funds from Alphabet Soup.  

Using a dataset previous funded projects we preprocessed the data and ran it through various neural network models to test the model's accuracy at predicting successful investments. 


## Results

### Data Preprocessing
- <strong>What variable(s) are considered the target(s) for your model?</strong> <br />
Our target for this model is the 'IS_SUCCESFUL' column that indicates which projects ended up being successful after receiving funds from AlphabetSoup.
<br />
<br />
- <strong>What variable(s) are considered to be the features for your model?</strong><br />
The features of this model include APPLICATION_TYPE, AFFILIATION, CLASSIFICATION, USE_CASE, ORGANIZATION, STATUS, INCOME_AMT, SPECIAL_CONSIDERATIONS and ASK_AMT.
<br />
<br />
- <strong>What variable(s) are neither targets nor features, and should be removed from the input data?</strong><br />
The EIN and NAME columns were neither targets nor features so we removed them from our DataFrame prior to starting our analysis. 
<br />
<br />

### Compiling, Training, and Evaluating the Model
- <strong>How many neurons, layers, and activation functions did you select for your neural network model, and why?</strong><br />
We used two hidden layers with 80 nodes on the first layer and 30 on the second in order to match the rule of thumb: "The number of hidden neurons should be 2/3 the size of the input layer, plus the size of the output layer. The number of hidden neurons should be less than twice the size of the input layer."
<br />
<br />
- <strong>Were you able to achieve the target model performance?</strong><br />
The target model performance of 85% not achieved in the first pass with an accuracy score of 72.85%.

![Accuracy Score](/Resources/Images/LossAccuracy.png)

<br />
<br />
- <strong>What steps did you take to try and increase model performance?</strong><br />
In order to improve the accuracy we attempted a few different methods of optimization, including adding<br> 

  - Additional hidden layers
  ![added lyer](/Resources/Images/added_layer_accuracy.png)
  
  - Changing our activation functions
  ![added layer](/Resources/Images/tahn_activation_accuracy.png)
  - Rebinning some of the categorical information
   ![added layer](/Resources/Images/rebinned_accuracy.png)
  
  
  <br />  None of these were able to increase the accuracy of the model to the desired 85%.  
<br />
<br />

## Summary  
This model is not effective in being able to predict the success of a particular project. There could be a few reasons for this: not enough input data, not fully optimized model or possibly we are just using an incorrect model altogether for this analysis. 

To optimize our current model we could see if there is additional data we could add to our dataset to help train the model better or we could try to use some more traditional machine learning techniques like random forest classifier and compare the results. Figuring out which machine learning model will take some more trial and error before we land on the right one.  

