# Cancer_Patients_Clasification
### Classifying cancer patient surviving chances 

"When you die, it doesn't mean you lose to cancer. You beat cancer by how you live, why you live and in the manner in which you live" Stuart Scott

We have all heard many heart warming cancer survivor stories. They give cancer patient hope and courage to fight. And with the right care and early diagnosis we can definitely have a better chances of survival. However, once someone is diagnosed the first question that comes to mind is "What are the changes of Survival". Doctors use statistics to give them a percent chance. However, They are tricky. 

## OBJECTIVE
I am trying to determine the 7-year survival of prostate cancer patients. A patient survived if they are still alive 7 years after diagnosis. This means that a patient is counted as dead whether or not the death was due to their cancer.

The set labeled ‘training_data’ has details of patients, the state of their cancer at time of diagnosis, and some information about the progression of their disease. I used those features to conduct my prognosis. 


"\n""\n"
## Conclusion

### Findings
1. If the Size of primary tumor 1 year after diagnosis is greater than 33.23 mm then chances are higher that he or she will die,
2. if Level of prostate-specific antigen in blood 1 year after diagnosis, is greator than 8.2 ng/mL then chances of survival is less.
3. While analyzing symptoms I found that death percentage increases if people are having symptom codes "S01, P01, P02 and P03". Where  as chances of survival is more if the person is having O11 as a symptom code.

"\n""\n"
## Model selection

### Part 1

1. Before selecting the model I had to do feature transformation. This was needed because symptoms columns were grouped together and for model to have an higher accuracy symptoms columns needed to be transformed via creating dummy variables.

2. Logistic Regression : Started with the simple model found that the model was not performing well on both test and training data. That meant model was suffering from high bias. To solve this issue I switched to more complex non linear model.

3. Support Vector Machine : I used various C and gamma values in rbf kernal with 10 fold cross validation to find the best model. But still the increase in Test accuracy was not significant.

4. Finally I tried ensemble families with different learning rate under Gradient Boosting Classifier. I found that the training error was significantly decreased and the accuracy was increase by 7% compared to Logistic regression model. Most importantly Area under the graph of ROC curve was decent that of 0.74 out of 1."\n"
"\n"
### Part 2

1. As the data challenge gave more importance to accuracy I subsetted the symptoms into another dataframe and plotted the importance of symptoms on survival rate.

2. Then I did my feature selection using the above informations and passed them to the model. 

3. Finally I selected the model with less features as it was performing same compared to the model with all features. Also the final features showed more than 95% variance in predicting the dependent variable. 
