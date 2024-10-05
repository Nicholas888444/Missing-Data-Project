# DBProject2
Created by Brian Butzen and Nicholas Thomson

## How to run the program
Please ensure that input.data is located in the same folder as db.ipynb.
### Running the program from an IDE
You can open the file in any IDE that supports a Jupyter Lab (ipynb) file.

## How to use the GUI
To generate a report simply select which report you would like to create and then click the Generate Report button.
<br>The row will change the display to white when it is selected and a light blue when it is not selected.
<br>To close and end the program just push the Cancel button or close out the window in the traditional manner.

## Project Tasks:
1. Implement methods to handle missing data using the following techniques:
* Substitution with mean for numeric attributes.
* Substitution with median for numeric attributes.
* Substitution with mode for categorical attributes.
* Predictive modeling-based imputation for numeric attributes.

2. Test Missing Data Handling Methods:
* Apply each implemented method to the sample dataset input.data
* Display the original dataset and the modified datasets after applying each handling method for verification.

3. Construct Missing Values Report:
* Develop a method to create a report listing missing values in the dataset.
* Include the count of missing values in each attribute and any relevant statistics about the missingness.

4. Design Graphical User Interface (GUI):
* Develop a user-friendly GUI to interact with the application.
* Include options to choose handling methods and display results.

## Instructions for Handling Missing Data:
* Substitution with Mean (Numeric Attributes):
    * Replace missing values in numeric attributes with the mean of non-missing values in the respective attribute.
* Substitution with Median (Numeric Attributes):
    * Replace missing values in numeric attributes with the median of non-missing values in the respective attribute.
* Substitution with Mode (Categorical Attributes):
    * Replace missing values in categorical attributes with the mode (most frequent value) of non-missing values in the respective attribute.
* Predictive Modeling-Based Imputation:
    *Use a predictive model to estimate missing values in numeric attributes based on non-missing values and other attributes.

You have the flexibility to design your predictive modeling-based imputation method, this can include techniques such as k-nearest neighbors, linear regression, or other algorithms.
Example: Train a linear regression model using non-missing values to predict missing Age values.


All tasks are performed in db.ipynb
Task 1: 
All methods take in a pandas dataframe from a csv file and return a pandas dataframe with updated entries.

These are the methods implemented for Task 1:
* ReplaceNumericalMean handles substitution with mean for numeric attributes.
* ReplaceNumericalMedian handles substitution with median for numeric attributes.
* ReplaceCategoricalMode handles substitution with mode for categorical attributes.
* PredictiveModeling handles Predictive modeling-based imputation for numeric attributes.
* MakeCSV makes a csv file from the pandas dataframe

Task 2: 
Task 2 is performed within the create_report method when the appropriate button is selected and the Generate Report button is pressed.
For each replacement method requested the original dataframe is printed to the console followed by the updated dataframe.
A CSV is created for each replacement method as well for easier viewing. The name of the CSV is displayed in the GUI.

Task 3: 
Task 3 is performed within the create_report method when the appropriate button is selected and the Generate Report button is pressed.
Missing.txt is created which displays the following information:
* The number of missing elements within each column.
* The data types of each column.
* The number of missing values in each row.
* The total number of missing values in the dataset

Task 4:
The GUI will run when db.ipynb is run.

