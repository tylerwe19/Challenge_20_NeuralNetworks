# Challenge_20_NeuralNetworks

## Analyzing Alphabet Soup Applicants

The purpose of this analysis is to create a neural network model that predicts whether applicants will be successful if funded by Alphabet Soup. The goal is for this analysis to create a model that has a predictive accuracy that is higher than 75%.

## Results
 * Data Preprocessing
    * Since the goal of this analysis/model is to predict if an applicant is successful, the IS_SUCCESSFUL field is the target variable
    * All other variables are featured in this model to help the model predict applicant success except for the variables listed below. Variables to help the model predict success are Application type, affiliation, classification, organization type, income, special considerations, and how much the applicant is asking for.
    * EIN and Name are just unique identifiers and have no value as variables to the model, so they've been dropped.
 I needed to encode the categorical variables such as application type and classification. A screenshot of my preprocessed dataframe is below:
 
 
 * Compiling, Training, and Evaluating the Model
    * The initial model in Deliverable 2 had me create a model with 4 layers: the input and output layers with 2 hidden layers. The first hidden layer had 80 nodes and used the relu activation function, the second hidden layer had 30 nodes and used the relu activation function, and the output layer used the sigmoid activation function.
    * I tried three different models to figure out the best way to exceed the 75% predictive accuracy goal. However, I was unable to achieve this goal.
    * In my attempt to create a model that exceeds 75% predictive accuracy, I created a keras tuner to find the best model. The tuner provided the following:
 
    * Considering the tuner recommended I use the tanh activation function, 7 layers, and various single digit neurons in each layer I completed the following:
     * My first adjusted model had 7 layers (input, output, and 5 hidden layers). It felt drastic to go from 80 and 30 neurons in the model from deliverable 2 to a model that has single digit neurons. So I started with double digit neurons and gradually decreased neurons as we went into additional hidden layers. I used 23 neurons in the first hidden layer, 12 in the second hidden layer, 7 in the third, 5 in the fourth, and 3 in the fifth. I also alternated between sigmoid and tanh activation functions. This first model didn't improve from the original model in deliverable 2 as seen below:



     * In the second model I aligned it with exactly what the keras tuner stated was the best model. This model had 7 layers, the 4 hidden layers had 7,7,7,3, and 5 neurons respectively. The second model didn't improve from the original or the model above. The results are below:




      * Lastly, I created a third model based on a subset of the original cleaned dataframe. This dataframe has the Application types, classification types, income amounts, and special considerations variables to predict the success of the applicant. This model's performance in terms of predictive accuracy drastically diminshed. See below:



## Summary
   I was unable to create a deep learning model that has a predictive accuracy of 75% or greater. A logistical regression is another option to determining whether an applicant is successful or not. Gathering more data points to beef up the amount of inputs can be helpful in building a model with a better predictive accuracy.
   
 --- 
