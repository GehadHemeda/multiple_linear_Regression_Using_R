# multiple_linear_Regression_Using_R
Using R programming, I apply stepwise regression to the Lung Capacity data set from the Kaggle website(https://www.kaggle.com/datasets/radhakrishna4/lung-capacity)
Dataset features:
     LungCap: It’s the lung capacity(closingcapacity) of the person
     Age: It’s how old is the person
     Height: It’s how tall is the person
     Smoke: If the person smokes or doesn’t smoke
     Gender: If are male or female
     Cesarean: If they’re born by Cesarean
steps of analysis:
      Exploratory Data Analysis(EDA).
      Identifying Potential Predictors and estimating the final model.
      Check assumptions(evaluating the validity of the model).
      Forecasting.

I applied EDA for linear regression to understand how the features of the data are related to one another, such as:
  A command called summary gives you the basic statistics of your dataset like mean, median, 1st quartile, 2nd quartile etc.
  boxplots to check outliers .
  histogram to check the distribution of our data.
  Visualizing the Relationships in the Data using pairs function in R.
  
Identifying Potential Predictors usig stepwise procedure
  Step1:Regress each predictor on y separately. 
  The predictors with a p-value lower than the entering threshold(0.1) will be added to the final model. 
  If no variable has a p-value lower than the entering threshold, then the algorithm stops, and you have your final model with a constant only.
  
  Step2: Use the predictor with the lowest p-value and adds separately one variable. 
  You add to the stepwise model, the new predictors with a value lower than the entering threshold. 
  If no variable has a p-value lower than 0.1, then the algorithm stops, and you have your final model with one predictor only. 
  You regress the stepwise model to check the significance of the step 1 best predictors. 
  If it is higher than the removing threshold, you keep it in the stepwise model. Otherwise, you exclude it.
 
  Step3: You replicate step 2 on the new best stepwise model. 
  The algorithm adds predictors to the stepwise model based on the entering values and excludes predictor from the stepwise model if it does not satisfy the excluding threshold.
  ****
  The algorithm keeps on going until no variable can be added or excluded.

finally, i analysed the residuals of the fitted model and found this model is valid for forecasting.














