# Report: Predict Bike Sharing Demand with AutoGluon Solution
#### NAME HERE

## Initial Training
### What did you realize when you tried to submit your predictions? What changes were needed to the output of the predictor to submit your results?
TODO: That few negative values ​​have come out, so I didn't have to change few values ​​to zero.
In order to use the predict method, the train and the test must have the same columns and the same data type.

### What was the top ranked model that performed?
TODO: 
The best model was the model in which I increased the time limit and excluded KNN-type models with a score of 0.462.

## Exploratory data analysis and feature creation
### What did the exploratory analysis find and how did you add additional features?
TODO: 
I found large values, which could be normalized. But first I tried increasing the features by adding hours, days and months. I have also changed the data type of the weather and seasons. Which worked fine.

### How much better did your model preform after adding additional features and why do you think that is?
TODO: The score decreased from 1.8 to about 0.7. I think this is because taking weather and seasons as categories is more representative. and the hour, day and month may be related to the demand for bicycle rental.

## Hyper parameter tuning
### How much better did your model preform after trying different hyper parameters?
TODO: With a few small changes it improved almost halfway. It went from 0.71 to 0.46.

### If you were given more time with this dataset, where do you think you would spend more time?
TODO: 
Changing hyperparameters and evaluating features.

### Create a table with the models you ran, the hyperparameters modified, and the kaggle score.
|model|hpo1|hpo2|hpo3|score|
|--|--|--|--|--|
|initial|root_mean_squared_error|600|best_quality|1.81067|
|add_features|root_mean_squared_error|600|best_quality|0.71120|
|hpo|root_mean_squared_error|1200|best_quality|0.45231|

### Create a line plot showing the top model score for the three (or more) training runs during the project.

TODO: Replace the image below with your own.

![model_train_score.png](/project/model_train_score.png)

### Create a line plot showing the top kaggle score for the three (or more) prediction submissions during the project.

TODO: Replace the image below with your own.

![model_test_score.png](/project/model_test_score.png)

## Summary
TODO: Using the auto Gluon library can be a step to know which model can perform better with the data. It is a useful and effective tool, but you have to know its outputs and how to adjust its parameters to obtain better results.
