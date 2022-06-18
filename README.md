# Cervical_cancer_detection_using_ML
# Introduction
According to World Health Organisation (WHO), when detected at an early stage, cervical cancer is one of the most curable cancers. Hence, the main motive behind this project is to detect the cancer in its early stages so that it can be treated and managed in the patients effectively. 

# Flow of project is as explained below:
This project is divided into 5 parts:
1. Data Cleaning      
2. Exploratory Data Analysis      
3. Baseline model: Logistic Regression      
4. Ensemble Models: Bagging with Decision Trees, Random forest and Boosting      
5. Model Comparison and results 

# Refer below for References:
Link to basic information regarding cervical cancer : https://www.cdc.gov/cancer/cervical/basic_info/index.htm
The dataset for tackling the problem is supplied by the UCI repository for Machine Learning.
Link to Dataset : https://archive.ics.uci.edu/ml/datasets/Cervical+cancer+%28Risk+Factors%29
The dataset contains a list of risk factors that lead up to the Biopsy examination. The generation of the predictor variable is taken care of in part 2 (Exploratory data analysis) of this report. We will try to predict the 'biopsy' variable from the dataset using Logistic Regression, Random Forest, Bagging with Decision Trees and Boosting with XGBoost Classifier.

# Results: 
Based on our Base model and The Ensemble Models we used, we observed -
1. After the entire process of training, hyperparameter tuning and tackling class imbalance was complete , we obtained the results as depicted through the graphics.
2. We observe that Bagging and Random Forest gives the highest accuracy and precision of  97.09 and 80% resp.
3. Plotting the Confusion matrix showed us that Random Forest using upsampling and class weights gives us 2 false positives and 3 false negatives with auc of 0.87

# Why random forest is the best model??
1. So as we see, while comparing all of  our models,RF has maximum f1_score and accuracy  along with Bagging i.e. 76.2 n 97.09% resp. 
2. And it also produces the same amount of false negatives with a recall of 72.73% just like all the other models.
3. But we still consider RF better coz of its added advantage that, the decision trees are decorrelated as compared to bagging leading to lesser variance and greater ability to generalize.

# Conclusion:
On observing the feature importance of the best model i.e random forest, we can see that the most important features are Schiller, Hinselmann, HPV, Citology, etc. 
This also makes sense because Schiller and Hinselmann are actually the tests used to detect cervical cancer. 

# Problems Faced:
A major problem encountered while training the model was that it had too little data to train. On collaborating with all the hospitals in India, we can have enough data points to train a model with a higher recall, thus making the model better.

# Scope of Improvement
As next steps I would want to do exactly that, to deploy the model and refine it. 
We may also modify the number of the predictor variables, as it may well turn out that there are other predictors which may not be present in our current dataset. This can only be found by practical implementation of our predictions.
