# Challenge_20_NeuralNetworks

##Analyzing Alphabet Soup Applicants

The purpose of this analysis is to create a neural network model that predicts whether applicants will be successful if funded by Alphabet Soup. The goal is for this analysis to create a model that has a predictive accuracy that is higher than 75%.

##Results
 * Data Preprocessing
    * Since the goal of this analysis/model is to predict if an applicant is successful, the IS_SUCCESSFUL field is the target variable
    * All other variables are featured in this model to help the model predict applicant success except for the variables listed below. Variables to help the model predict success are Application type, affiliation, classification, organization type, income, special considerations, and how much the applicant is asking for.
    * EIN and Name are just unique identifiers and have no value as variables to the model, so they've been dropped.
 I needed to encode the categorical variables such as application type and classification. A screenshot of my preprocessed dataframe is below:
 
 
 * Compiling, Training, and Evaluating the Model
    * The initial model in Deliverable 2 had me create a model with 4 layers: the input and output layers with 2 hidden layers. The first hidden layer had 80 nodes and used the relu activation function, the second hidden layer had 30 nodes and used the relu activation function, and the output layer used the sigmoid activation function.
    * I tried three different models to figure out the best way to exceed the 75% predictive accuracy goal. However, I was unable to achieve this goal.
    * In my attempt to create a model that exceeds 75% predictive accuracy, I created a keras tuner to find the best model. The tuner provided the following:
    
      * Considering the tuner recommended I use the tanh activation function, 6 layers, and various single digit neurons in each layer I completed the following:
          * 
