
## **Housing Prediction with Machine Learning**


1. Overview
-----------
In this project, I applied a decision tree model to predict housing price in the Boston area based on a public housing data set provided by UCI (https://archive.ics.uci.edu/ml/datasets/Housing). This dataset has been included in the sklearn package (http://scikit-learn.org/stable/), so you don't need to download it separately. 


2. Results
--------------
***2.1 Decision Tree Regressor Learning Performances***

![alt tag](https://cloud.githubusercontent.com/assets/17630430/13905240/19d58276-ee88-11e5-839c-7bba73413dd5.png "Decision Tree Errors")

The testing and training errors changes with difference max_depth parameter. 

 - With max_depth = 1. the model is under-fit with high bias
 - With max_depth = 10. the model is over-fit with high variance


***2.2 Decision Tree Regressor Complexity Performance***

![alt tag](https://cloud.githubusercontent.com/assets/17630430/13905246/4a5f5cd2-ee88-11e5-8d00-48ab73350785.png "Decision Tree Complexity Performance")  

- training error decreases steadily as the max depth increases
- testing error decreases until a max_depth = 5 before a slow increase
- suggesting over-fitting after max_depth = 5


***2.3 Housing Price Predicting***

- The features of a client's house as input for the model
- The predicted housing price is 21.63 (in $1000), close to the median housing price in the Boston area.


3. Steps
-------------
**3.1 Read the Data Set. **
The following is a summary of the the Boston Housing dataset.

-  Total number of houses: 506
- Total number of features: 13
- Mean/Median house price: 22.53/21.20 (in $1000's) (so cheeeeeep!)

**3.2 Data Preparation**. 

- Randomly shuffle the data X and target labels (housing values) y
- Split the data into training (70%) and testing (30%) subsets

**3.3 Model Development**. 

- Perform a total error calculation (mean squared error, MSE) between the true values of y (y_true) and the predicted values of the y (y_predict)
- Create a scoring function using MSE
- Build a grid search model using regressor

**3.4 Model Evaluation**. 

- Evaluate the performances of the decision tree regressor
- Find out the optimal parameters (max depth) for the model

**3.5 Housing Price Prediction**. 

- Collect the features of a client's house 
- Predict the best selling price based on the optimized model







