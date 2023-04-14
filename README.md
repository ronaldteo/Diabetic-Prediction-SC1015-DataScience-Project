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

## Video Presentation
[https://drive.google.com/file/d/1psC_N_pjgUpRWYNCBUKMJ2qGNqkxsq6p/view?usp=share_link](https://www.google.com)

## Problem Definition
* Are we able to predict if a person suffers from diabetes based on the attributes?
* Which model is the best in predicting it?
* Problem Statement: "To devise a method for early detection of diabetes to prevent diabetic complications, using diagnostic measurements to predict whether an individual is likely to have diabetes."

## Data Cleaning

After we defined our problem, we cleaned and prepped the dataset that will be used for Data Visualization and Analysis. After we visualize and analyze, we will do upsampling for our data to train our model more accurately. 

* Our preliminary exploration found that missing data for each attribute were filled with zeros.
* Hence, we replaced the zeros with NULL and counted the number of missing datas.
* We also replaced the NULL values for remaining attributes with its median.
* 30% Skinthickness and Insulin attribute are missing. We also noticed that Skinthickness and Insulin has little correlation with outcome, so we dropped these columns.

## Data Visualization & Analysis

* Our count plot showed that most individuals are in the 20s.
* We created a boxplot for each attribute. These are our findings:
* 1) The higher the glucose levels, the are more likely they are be at risk of diabetes.
* 2) People with higher BMI are more likely to be at risk of diabetes. 50% of the diabetics individuals are have higher BMI as compared to the median of non-diabetic individuals for age and BMI.
* 3) Blood pressure and DiabetesPredigreeFunction which measurement for diabetes from genetics doesn’t seem to be good indicator of diabetes.
* 4) The correlation tallies with our findings from the boxplot

After we plotted our graphs, we plotted the Linear Regression, which looked at 2 attribute: BMI & Age Vs Glucose. We wanted to see if BMI & Age has any relationship with Glucose.
* After plotting our Linear Regression graphs, we found out that
* 1) For BMI and Glucose, the correlation is a 0.23, which implies a slight positive correlation
* 2) The correlation for Age & Glucose is 0.27, which also implies a slight positive correlation.
* Even though BMI and Age only has a slight positive correlation with Glucose, we can speculate that many such variables can all contribute to better predict if someone has diabetes. 

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
