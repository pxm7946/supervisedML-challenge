# supervisedML-challenge

The purpose of this homework assignment was to predict whether receiving a loan from LendingClub will become a high risk for the client or not. Supervised machine learning was used to determine this prediction by training and testing data, along with creating a linear regression and random forest classifiers to verify the data. More details on how to do so can be found below. 


After importing the files for the homework, which covered the years of 2019 and 2020, we were asked to convert the categorical data into numeric data. Specifically, the column "loan_status" needed to be dropped from the x training data, and isolated into the y training value. The same thing was done for the testing data. One thing that was considered was that the amount of columns in the training dataset may not be the same as the amount of columns in the testing dataset, which is the reason why a "for loop" was created to balance the datasets. This can be found in line 6 in the "Credit Risk Evaluator.ipynb" file. After separating the target feature, taking advantage of the "get_dummies()" function, and adding the missing columns to the testing dataset, the Linear Regression models and Random Classifier models were shown for both scaled and unscaled training data.


Let's start with the unscaled training data: Based on the screenshot below, after performing the required tests, we were able to see only a 53% of accuracy in the Linear Regression model and an increase of 10% accuracy in Random Forest Classifier model. What does this mean? The Random Forest Classifier model is definitely more reliable with unscaled training data, however, it does not give us a definite answer to determine whether the client is at a credit risk when accepting a loan. It may not be the ideal percentage, but we can conclude that with unscaled training data, there is a slight risk for the client.

![Screen Shot 2022-02-12 at 10 55 25 PM](https://user-images.githubusercontent.com/72631173/153741165-933eb769-9af8-44a9-98e3-14295a6c5357.png)

By using the StandardScaler library from sklearn.preprocessing, we were able to scale the data. The ".fit()" and " .transform()" functions were utilized for this task. The scaled training data is what was used for the second run through of the models. 


We can notice that the same functions were used for this section, however, scaled training data and y training were the points for the " .fit()" function. Below is a screenshot of the findings. 

![Screen Shot 2022-02-12 at 10 55 47 PM](https://user-images.githubusercontent.com/72631173/153741442-4cc551cd-7d1e-4810-bf86-213c8ad87f08.png)

We can notice that there was an increase in percentage for the Logistic Regression model, with a total of 57% risk, and a decrease in the Random Forest Classifier model percentage from the previous time. Although there was a change in each percentage for either model, I am unable to make an inference based on the percentages. Each of them are in the 50%-60% range, causing there to be a 50/50 conclusion on the prediction that was attempted to be made. 


In conclusion, supervised machine learning helped us classify the data and provide us with a percentage that helped us determine whether the client was, in fact, in a credit risk because of a loan. By scaling the training data, we were able to see a more accurate answer, however, it did not give a clear prediction. Overall, credit risk can go either way for the client. It is recommended for the client to continuously look over their credit scores, and create a budget plan in order to pay those loans off and avoid it to harm their credit score.

The code can be found under the "Credit Risk Evaluator.ipynb" file.
