# Naira-Dolllar-Market-Price-Predictions
-Import yfinance library
-Assign the 'USDNGN' currency pair to the naira variable
-Retrieve available naira data history for data cleaning and analysis
-Feature engineering: delete expendable columns
-Assign  a backward shift version of 'Close' to 'Tomorrow' for price comparism
-Assign binary values to 'Target' column to help determine movement
-Train data woth RandomForrstClassifier model using selected columns and calculate precision score
-Convert predictions to series and concatenate target and predictions
-Fit specified model to training data, make predictions on the test data, convert prediction to series format, concatenate target values from test set with predictions and return combined dataframe containing necessary parameters
-Loop through the dataset from start and increase with defined steps. Use predict function to generate predictions based on training and test. Concatenate all predictions to a single dataframe and return it
-Perform backtest on the naira dataset using specified model and predictors
-Calculate precision score for predictions
-Use the rolling average function on the 'Close' column over the specified horizon. Create new columns that represents the ratio of current 'Close' price to the rolling average and for the trend based on the sum of the target values over the specified horizons. Add created columns to the list of new predictors
-Train model with new specified hyperparameters using RandomForestClassifier
-Fit model to the training data uing the predictors. Generate probability predictions for the positive class of the test set. Use thresholding to convert probabilities to binary predictions. Convert prediction to series format. Combine actual target value from test set with predictions. Return the combined dataframe containing actual target and predictions
-Perform another backtest on new predictors
-Calculate the precision score for the predictions made in the backtest 
