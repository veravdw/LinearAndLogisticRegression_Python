# Wine Data Analysis

The dataset for this analysis is a sample of Portuguese vinho verde wines, and mainly consists of features representing physicochemical characteristics like acidity, sulphates etc, alcohol and a quality feature. The aim of this project is to create models to predict quality and alcohol content from the physicochemical features. 

## Format

The analysis is performed with python in a jupyter notebook, and partly in a Looker studio dashboard: https://lookerstudio.google.com/s/kyU3c0wCnuQ 

## Dataset

The dataset comes from a website called Kaggle, to be found in csv format via this url: https://www.kaggle.com/datasets/uciml/red-wine-quality-cortez-et-al-2009 
After some exploratory analysis we find the following: 
- The dataset consists of 1599 cases.
- There are 10 continuous physicochemical features plus a continuous feature for alcohol, and one ordinal categorical feature for quality.   
-	Correlations between features are ranging from 0-0.7
-	The 6 quality levels can be grouped into two categories based on the results of an Anova and independent samples t-test.

## Analysis

In this analysis we like to find out how we can predict quality of a vinho verde wine, and how we can predict alcohol% of a wine. 

Models created: 
-	Logistic regression with target variable quality
-	Linear regression with target variable alcohol

Main findings: 
- Quality category low/high can be predicted from alcohol with an accuracy of 72%. When adding 10 more features, this only increases slightly to 82%.
- 77% of the variance in alchohol content can be predicted by the physicochemical attributes in the dataset, after taking out outliers and features that are correlated, thus overlapping in what they measure.  

## Limitations

The quality categories used for logistic regression were imbalanced, thus we upsampled the smaller category, however when running the model on the imbalanced test data that was held out, precision was very poor. 
Expert knowledge would be needed to verify if the outcomes really make sense, and whether the chosen features have any practical value in predicting quality. 
Most features did not have a (strong) correlation with alcohol and neither with quality, the dataset might be missing components that could explain a significant part of the variance.  

