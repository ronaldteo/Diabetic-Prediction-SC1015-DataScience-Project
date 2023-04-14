# Welcome to Diabetes Prediction Repository

## About
This is a Mini-Project for SC1015 (Introduction to Data Science and Artificial Intelligence) which focuses on whether a person suffers diabetes based on various attributes in a dataset originally from the [National Institutes of Diabetes and Digestive and Kidney Diseases](https://www.kaggle.com/code/khageshorgiri/diabetes-prediction). The dataset include 768 datas of individual suffering from diabetes and not.

Please refer to the dataset [here](https://github.com/ronaldteo/Data-Science-Project/blob/f269bc2ba948eacc60f2842d6da8dc7013ad3ab9/diabetes.csv).

For detailed walkthrough, please look through the README in this format:

1. [Problem Definition](https://github.com/ronaldteo/Data-Science-Project#problem-definition)
2. [Data Cleaning](https://github.com/ronaldteo/Data-Science-Project#diabetes-prediction-data-cleaning)
3. [Data Visualization & Analysis](https://github.com/ronaldteo/Data-Science-Project#diabetes-prediction-exploratory-analysis--data-visualisation)
4. [Modeling](https://github.com/ronaldteo/Data-Science-Project#diabetes-prediction-upsampling--models)
5. [Conclusion](https://github.com/ronaldteo/Data-Science-Project#conclusion)
6. [What we learnt](https://github.com/ronaldteo/Data-Science-Project#what-did-we-learn-from-this-project)
7. [References](https://github.com/ronaldteo/Data-Science-Project#references)

## Contributors
* Ronald Teo Boon Keat
* Tay Wei Yang
* Wong Zhen Wei Gabriel

## Video Presentation

This is the link to our Video Presentation. We are unable to upload on Github as the file is too big.
[https://drive.google.com/file/d/1psC_N_pjgUpRWYNCBUKMJ2qGNqkxsq6p/view?usp=share_link](https://drive.google.com/file/d/1psC_N_pjgUpRWYNCBUKMJ2qGNqkxsq6p/view?usp=share_link)

## Problem Definition
* Are we able to predict if a person suffers from diabetes based on the attributes?
* Which model is the best in predicting it?
* Problem Statement: "To devise a method for early detection of diabetes to prevent diabetic complications, using diagnostic measurements to predict whether an individual is likely to have diabetes."

## [Diabetes Prediction (Data Cleaning)](https://github.com/ronaldteo/Data-Science-Project/blob/53bae5b751e34c129782824ad7bdcaf7679523d2/Diabetes%20Prediction%20(Data%20Cleaning).ipynb)

After we defined our problem, we cleaned and prepped the dataset that will be used for Data Visualization and Analysis. After we visualize and analyze, we will do upsampling for our data to train our model more accurately. 

* Our preliminary exploration found that missing data for each attribute were filled with zeros.
* Hence, we replaced the zeros with NULL and counted the number of missing datas.
* We also replaced the NULL values for remaining attributes with its median.
* 30% of Skinthickness and Insulin attribute are missing. We also noticed that Skinthickness and Insulin has little correlation with outcome, so we dropped these columns.

## [Diabetes Prediction (Exploratory Analysis & Data Visualisation)](https://github.com/ronaldteo/Data-Science-Project/blob/53bae5b751e34c129782824ad7bdcaf7679523d2/Diabetes%20Prediction%20(Exploratory%20Analysis%20&%20Visualisation).ipynb)

Cleaning our data enables us to start visualizing and analyzing our data.

* Our count plot showed that most individuals are in the 20s.
* We created a boxplot for each attribute. These are our findings:
  1) The higher the glucose levels, the are more likely they are be at risk of diabetes.
  2) People with higher BMI are more likely to be at risk of diabetes. 50% of the diabetics individuals are have higher BMI as compared to the median of non-diabetic individuals for age and BMI.
  3) Blood pressure and DiabetesPredigreeFunction which measures for diabetes from genetics doesn’t seem to be good indicator of diabetes.
  4) The correlation tallies with our findings from the boxplot

After we plotted our graphs, we plotted the Linear Regression graphs, which looked at 2 attribute: BMI & Age Vs Glucose. We wanted to see if BMI & Age has any relationship with Glucose.

* After plotting our Linear Regression graphs, we found out that
  1) For BMI and Glucose, the correlation is a 0.23, which implies a slight positive correlation
  2) The correlation for Age & Glucose is 0.27, which also implies a slight positive correlation.
* Even though BMI and Age only has a slight positive correlation with Glucose, we can speculate that many such variables can all contribute to better predict if someone has diabetes. 

## [Diabetes Prediction (Upsampling & Models)](https://github.com/ronaldteo/Data-Science-Project/blob/main/Diabetes%20Prediction%20(Upsampling%20and%20Models).ipynb)

After researching and consulting our Teaching Assistant, we realised that our data has imbalanced classes, which affected the accuracy of our models. And so, we upsampled our data to train a more accurate model. These are the 3 models we used.
1. Decision Tree<br>
2. Random Forest<br>
3. K-Nearest Neighbors (KNN)<br>

**Decision Tree:**
* We started out with the Decision Tree that many of us are familiar with. With an initial test accuracy of 0.733, the accuracy of the decision tree increased to 0.81. This showed that upsampling improved our accuracy.

**Random Forest:**
* Random Forest combines several decision trees for classification and regression. It prevents overfitting due to bias and is more accurate in predictions. With an average accuracy of 0.96, it is by far the most accurate model that we plotted. By tuning the hyperparameters, we estimated that the optimal depth would be 14. So we used depth 5 and 14 to produce our Random Forest.

**K-Nearest Neighbors (KNN):**
* KNN is a simple algorithm that stores all the available cases and classifies the new data or case based on a similarity measure. However, the algorithm gets significantly slower as the number of independent variables increase. Our model produced the best accuracy when K = 1, where K represents the parameter that refers to the number of nearest neighbours that will be included in the majority of the voting process.

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
Afolabi, S. (2022, September 17). Here's what I've learnt about sklearn.resample. Medium. Retrieved April 14, 2023, from https://towardsdatascience.com/heres-what-i-ve-learnt-about-sklearn-resample-ab735ae1abc4 

Brownlee, J. (2021, January 21). Failure of classification accuracy for imbalanced class distributions. MachineLearningMastery.com. Retrieved April 14, 2023, from https://machinelearningmastery.com/failure-of-accuracy-for-imbalanced-class-distributions/ 

Harrison, O. (2019, July 14). Machine learning basics with the K-nearest neighbors algorithm. Medium. Retrieved April 14, 2023, from https://towardsdatascience.com/machine-learning-basics-with-the-k-nearest-neighbors-algorithm-6a6e71d01761 

Khageshor, G. (2023, April 7). Diabetes Prediction - Eda &amp; Prediction. Kaggle. Retrieved April 14, 2023, from https://www.kaggle.com/code/khageshorgiri/diabetes-prediction 

Yiu, T. (2021, September 29). Understanding random forest. Medium. Retrieved April 14, 2023, from https://towardsdatascience.com/understanding-random-forest-58381e0602d2
