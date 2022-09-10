# Volkswagon Hackathon for Data Science - September 2022

Problem Statement
Socio-Economic Segregation on the basis of earnings is done by various government bodies across the world by doing a poll which can be
"door to door" or "online based" to identify/keep a check on the sections of society having lower levels of income.

Similarly in the US, it is a requirement for the federal bodies to be cognizant of people's income which falls under a 
threshold so that decisions taken on various fronts can be inclusive and without ambiguity. For this reason 
few federal bodies like the "Bureau Of Economic Analysis" outsource their masked data to 3rd party companies who are kept on contract to analyze the 
data to garner detailed insights and come up with different sets of best 
models to: 
  1) decide on a threshold value that can act as a good classification boundary condition.
  2) to classify the people in the database based upon this threshold value.

For that reason, you are hired by one such company and are provided with the threshold value 
which is decided to be $50k/year. The task expected from you is to :
  1) perform a detailed EDA to garner insights that can be helpful for the stakeholders.
  2) to classify all the people who earn more or less than $50k/year based upon their various demographical features
     by building a generalizable classification model.
   
## Approach

Basic EDA was done on the data.
Tried AutoML using autosklearn library to get base expected accuracy of about 64%.
Then the following ere done for Preprocessing:
  1. Missing vale Imputation: There were 9 columns with missing values. Two columns 'under18', 'unemp_reason' with more than 70% missing values were removed
     Missing vales were treated with mean and most frequent imputation. Other complex techniques were used, but no improvement.
  2. Encoding for categorical variables: One hot encoding was used and first category was dropped in case of binary columns.
  3. Scaling and Transformation: Power transformer along with normalization was done to support various ML models.
 
## ML Model
Task - Classification
Metric - Accuracy
Then neural network was built for classification. There were 3 hidden layers of sizes 32/16/24 with dropout layers in between to prevent overfitting.
ReLu was used for the activation function of hidden layers, and Sigmoid activation function was used for output layer as it was binary clasification.
The model was trained over 100 epochs and loss and accuracy were plotted to see for performance and overfiiting. It gave an accuracy of 66%.


## Rank
#### Public Leaderboard  :  -
#### Private Leaderboard : -
