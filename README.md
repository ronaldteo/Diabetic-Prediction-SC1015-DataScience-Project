# Welcome to Diabetes Prediction Repository

## About
This is a Mini-Project for SC1015 (Introduction to Data Science and Artificial Intelligence) which focuses on whether a person suffers diabetes based on various attributes in Kaggle dataset. The dataset include 768 datas of individual suffering from diabetes and not.

Please refer to the dataset here [insert dataset]

For detailed walkthrough, please view the source code in order from:

1.
2.
3.
4.
5.

## Contributors
* Ronald Teo Boon Keat
* Tay Wei Yang
* Wong Zhen Wei Gabriel

## Problem Definition
* Are we able to predict if a person suffers from diabetes based on the attributes?
* Which model is the best in predicting it?

## Models Used
1. Linear Regression<br>
2. Decision Tree<br>
3. Logistic Regression<br>
4. Random Forest<br>

## Conclusion
* Glucose has the highest correlation to whether a person has diabetes and the decision tree also concludes that glucose is the most importnat factor in determining diabetic outcome by being the root node.
* Upsampling imbalanced data improved the model performance especially on the non-diabetic class.
* Decision tree for an upsampled data has a higher accuracy.
<br>
|    | Normal Decision Tree  | Upsampled Decision Tree |
| ------------- || ------------- | ------------- |
| Train Data| 83%  | 64%  |
| Test Data | 81%  | 78%  |
<br>
* Random forest tree would be the best classifier to determine whether a person is likely to have diaebetes with an accuracy of 97%.
* Hence, it is possible to predict if a person is likely to suffer from diabetes using random forest with the high accuracy.

## What did we learn from this project?
..

## References
