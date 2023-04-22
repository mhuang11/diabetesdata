# Diabetes Data Analysis

## 1. About The Data

The dataset can be downloaded from [here](https://www.kaggle.com/datasets/uciml/pima-indians-diabetes-database).

It is originally from the National Institute of Diabetes and Digestive and Kidney Diseases. The objective of this dataset is to diagnostically predict whether or not a patient has diabetes, based on certain diagnostic measuresments included in the dataset. All patients here are females at least 21 years old of Pima Indian heritage.

This  dataset consist of several medical predictor (independent) variables and one target (dependent) variable, `outcome`.  Independent variables include the number of pregnancies the patient has had, their BMI, insulin level, age, and so on.

## 2. Exploratory Data Analysis

From these distribution graphs, Age and Pregnancies are not in normal distribution as expected, since the underlying population should not be normally distributed, either. Glucose level and BMI are following a normal distribution. 

![image](https://user-images.githubusercontent.com/78035136/233787222-45c623e1-ee54-4f74-b829-71cf452b41cd.png)

I chose to go deeper in the analysis with the impact of glucose on diabetes:
![image](https://user-images.githubusercontent.com/78035136/233787296-80f1c483-b7f7-47ca-99e9-e71bec34d0c8.png)

After conducting a Welch's Two-Sample t-Test, the p-value came out to be less than the critical value of 0.05, so we can say that we are 95% confident that the average glucose levels for individuals with diabetes is less than the people without diabetes.

![image](https://user-images.githubusercontent.com/78035136/233787336-86c8eada-1775-4fda-a66b-6f3c3bceedf1.png)

In Plot 2 further confirms our results, showing that the distribution is shifted towards the left for those without diabetes. This indicates those without diabetes generally have a lower blood glucose level.

## 3. Correlation Plot Variance

To explore the correlation between all of the variables, I made a scatter matrix:

![image](https://user-images.githubusercontent.com/78035136/233787397-ac05478f-6539-45ba-b7ba-59d4ded4e2a8.png)

Pregnance with Age, and Insulin with Skin Thickness have higher correlation in relevance to presence of diabetes.
