# Machine Learning

***Description of preliminary data preprocessing***

- The data was cleaned and filtered to display the three primary consoles for this analysis. 
Data from two other sources were combined in order to create the database and add additional data points. 


***Description of preliminary feature engineering and preliminary feature selection, including their decision-making process***

- Once in python, the global and other countries categories were combined in order to create one. In order to 
conduct the analysis of genre and sales by country, dummy variables were generated to change the 
object data type to numeric. A heat map and scatter plot were developed in order to determine the relationship if any 
existed between the desired test variables. 


***Description of how data was split into training and testing sets***

- Ultimately, the primary goal was to create a sales projection based on genre and region. In order to do this
the data was split into training variables by 0.4. This decision was based on research from different 
sales analysis conducted and our own data set. The reminder of the data points were used for the testing model.


***Explanation of model choice, including limitations and benefits***

- For this analysis linear regression was the model choice selected. It is a supervised machine learning model that allows for target prediction of the independent variable. Since this model can determine if a specific genre of game will sale better in a different region this model a good choice for this analysis. One of the 
main limitations of this model is the reliance on linear relationships. It is based on the assumption that the relationships at their core are linearly connected, however this may not truly be the case.

***Description of how they have trained the model thus far, and any additional training
that will take place**** 

- To keep consistent the data was split as shown below:
X_train, X_test, y_train, y_test = train_test_split(X, y, train_size = 0.7, test_size = 0.3, random_state = 100)
This means that the test size was 30% of the data. No additional training will be conducted in the future. 

***Description of current accuracy score***

- Currently the accuracy scores for each prediction are as follows:
Na Sales: 0.092
EU Sales: 0.056
JP Sales: 0.045
GS Sales: 0.075

This does however mean that the accuracy is weaker than would be liked. 

 

