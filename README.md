# Welcome to Diabetes Prediction Repository

## About
This is a Mini-Project for SC1015 (Introduction to Data Science and Artificial Intelligence) which focuses on whether a person suffers diabetes based on various attributes in a dataset originally from the [National Institutes of Diabetes and Digestive and Kidney Diseases](https://www.kaggle.com/code/khageshorgiri/diabetes-prediction). The dataset include 768 datas of individual suffering from diabetes and not.

Please refer to the dataset [here](https://github.com/ronaldteo/Data-Science-Project/blob/f269bc2ba948eacc60f2842d6da8dc7013ad3ab9/diabetes.csv).

For detailed walkthrough, please view the source code in order from:

1. Problem Definition
2. Data Cleaning
3. Data Visualization & Analysis
4. Modeling
5. Conclusion
6. References

## Contributors
* Ronald Teo Boon Keat
* Tay Wei Yang
* Wong Zhen Wei Gabriel

## Problem Definition
* Are we able to predict if a person suffers from diabetes based on the attributes?
* Which model is the best in predicting it?
* Problem Statement: "To devise a method for early detection of diabetes to prevent diabetic complications, using diagnostic measurements to predict whether an individual is likely to have diabetes."

## Data Cleaning
* Our preliminary exploration found that missing data for each attribute were filled with zeros.
* Hence, we replaced the zeros with NULL and counted the number of missing datas.
* We also replaced the NULL values for remaining attributes with its median.
* 30% Skinthickness and Insulin attribute are missing. We also noticed that Skinthickness and Insulin has little correlation with outcome, so we dropped these columns.

## Data Visualization & Analysis
* 

## Models Used
1. Linear Regression<br>
2. Decision Tree<br>
3. Logistic Regression<br>
4. Random Forest<br>

## Conclusion
* Glucose has the highest correlation to whether a person has diabetes and the decision tree also concludes that glucose is the most importnat factor in determining diabetic outcome by being the root node.
* Upsampling imbalanced data improved the model performance especially on the non-diabetic class.
* Decision tree for an upsampled data has a higher accuracy.
* Logistic regression has the lowest accuracy score of 72% compared to other models.
* Random forest tree would be the best classifier to determine whether a person is likely to have diaebetes with an accuracy of 97%.
* Hence, it is possible to predict if a person is likely to suffer from diabetes using random forest with the high accuracy.

## What did we learn from this project?
* We learnt how to utilize the data science pipeline to guide us in the project.
* Resampling method to make the data balanced.
* Selecting the right visualisation that can give the best representation and tells the most about the data.
* Logistic regression and random forest tree whereby we understand the model and implement them in dataset.
* How to interpret and gather insights based on the results.
* Collaborating in GitHub
* Get to experience first-hand of teamworking in a data science project which replicates what it may be like in the working industry.

## References
https://www.kaggle.com/code/khageshorgiri/diabetes-prediction </br>
https://towardsdatascience.com/machine-learning-basics-with-the-k-nearest-neighbors-algorithm-6a6e71d01761
https://www.datacamp.com/tutorial/random-forests-classifier-python
