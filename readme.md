# Layoffs as an alternative data

## Module requirements

1. pandas
2. numpy
3. tensorflow
4. sklearn
5. statsmodels
6. xgboost
7. matplotlib
8. Jupyter
9. Python3

## Steps to run the program

1. It is a iPython notebook, can be run directly in jupyter or colab. Just have to run Project.ipynb file
2. To run from command line, convert iPython notebook to python script to run the program, using below commands
```
jupyter nbconvert --to python Project.ipynb
 ```
 ```
python3 Project.py
 ```

### Things to check/remember

1. 'Historical Data' directory, 'Processed Data' directory, 'Project.ipynb', 'layoffs.csv' all of them should be in the same directory. ('Layoffs' in my case)
2. Datasets required are 'Historical Data' directory (contains historical data as csv files of all companies) and 'layoffs.csv' in the 'Project' directory file. Both are submitted in the same zip file.
3. Directory with the name 'Processed Data' should be present in the 'Project' directory, to store the preprocessed data. 'Processed Data' directory is also submitted (replaces the csv files inside 'Processed Data' directory everytime we run the code for a particular company). 
4. In 2nd cell of the notebook, company name as a string should be assigned to company_name. Deafult is 'Cisco'
5. 'Cisco', 'IBM', 'Salesforce' are some of the companies. Entire list of companies is present in the 3rd cell
6. In 2nd cell of the notebook, boolean variable close_price_as_predictive_column should be set to True if we want to test with close price as a predictive column, False for direction change as a predictive column,. Default is False
7. 4th cell does the granger causality tests between layoffs and close price and displays results.
8. 6th cell is testing with Xgboost regression model, and displays RMSE and R2 Score. Output column is always close price irrespective of close_price_as_predictive_column for this regression model
9. Preprocessed data is printed in the 7th cell for a selected company
10. 11th cell is training the LSTM model. 
11. 13th cell is predicting the output column using the trained lstm model for the test data, and it displays 'mean squared error'
12. 14th cell/last cell prints the classification report i.e precision, recall, and accuracy if output column is 'direction_change'. If output column is close price, it displays the graph of actual stock price, and predicted stock price for test data
13. Project.pdf is also submitted, screenshot/snapshot of all cells along with outputs with default values
