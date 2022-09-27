
# Final-Project_Group4

# Video Game Sales analysis based on Genre vs Region

![video game image](https://user-images.githubusercontent.com/96400887/189534618-4388068a-6e40-4902-b8b0-2374a65f5dd2.jpg)


 ## 1. Selected topic:

 
- we will be laying the foundation for our analysis by processing and exploring a large amount of data on video game sales.
- The dataset contains information regarding the sales of video games across various regions like North America, Europe, Japan and also globally, while also giving information regarding the Names, Publishers and Platforms. 


## 2. Reason why they selected their topic :

- The world is getting more connected every day, and more gaming trends and preferences are emerging around the globe. 
- We want to know which console is preferred the most based on different regions. 
- We will compile results from all over the world and determine if any regional trends might shape the gaming industry as a whole.
- It's great stress relief and some games are just so much fun to play , Enjoyment for all age people.

 ## 3. Description of Source Data
 
 - This dataset has been made available to Kaggle which is the home for many such datasets and competitions.
 - Our data is comprised from three different data sets found online. These datasets have video game titles, genres, console types, of games sold, dates, and region it   sold in.

## 4. Questions We Hope to Answer
- Given our data sets we hope to answer the following:

 1. What genre of game sells best?
 2. What seasons do games sell the best?
 3. What region games sell the best?
 4. Overall comparisons between genre, console types, dates sold, and regions sold in?

## Descriptions of the Communication Protocols

- We communicate our project related tasks through Slack and via zoom meetings.
- Each team member give their regular updates about the progress and changes via slack messages.

# Machine Learning

### Description of preliminary data preprocessing

- The data was cleaned and filtered to display the three primary consoles for this analysis. 
Data from two other sources were combined in order to create the database and add additional data points. 

### Description of preliminary feature engineering and preliminary feature selection, including their decision-making process and Description of how data was split into training and testing sets

- Once in python, the global and other countries categories were combined in order to create one. In order to 
conduct the analysis of genre and sales by country, dummy variables were generated to change the 
object data type to numeric. A heat map and scatter plot were developed in order to determine the relationship if any 
existed between the desired test variables. 

![data exploration sales and scatter plot](https://user-images.githubusercontent.com/103790879/191971560-293900ce-b05a-4073-afa0-00153c326f0f.png)

The scatter plot above shows that there is a linear relationship.

![exploration heatmap](https://user-images.githubusercontent.com/103790879/191971596-0b8abd50-f4c5-436b-ac25-cda98cf8d3ed.png)

The heat map helps to serve as further evidence that there is a relationship.

- Ultimately, the primary goal was to create a sales projection based on genre and region. In order to do this
the data was split into training variables by 0.4. This decision was based on research from different 
sales analysis conducted and our own data set. The reminder of the data points were used for the testing model.


### Explanation of model choice, including limitations and benefits

- For this analysis linear regression was the model choice selected. It is a supervised machine learning model that allows for target prediction of the independent variable. Since this model can determine if a specific genre of game will sale better in a different region this model a good choice for this analysis. One of the 
main limitations of this model is the reliance on linear relationships. It is based on the assumption that the relationships at their core are linearly connected, however this may not truly be the case.

### Description of how they have trained the model thus far, and any additional training that will take place

- To keep consistent the data was split as shown below:
 
X_train, X_test, y_train, y_test = train_test_split(X, y, train_size = 0.7, test_size = 0.3, random_state = 100)
This means that the test size was 30% of the data. No additional training will be conducted in the future, however other variables such as different random states and test size were tried. These variables were however, less effective than the above ones. 

### Description of final accuracy score
                          
==============================================================================

Dep. Variable:               NA_Sales   R-squared:                       0.092
Model:                            OLS   Adj. R-squared:                  0.070
Method:                 Least Squares   F-statistic:                     4.329
Date:                Thu, 22 Sep 2022   Prob (F-statistic):           3.52e-06
Time:                        18:58:48   Log-Likelihood:                -440.78
No. Observations:                 484   AIC:                             905.6
Df Residuals:                     472   BIC:                             955.8
Df Model:                          11                                         
Covariance Type:            nonrobust                                         

                   coef    std err          t      P>|t|      [0.025      0.975]
                   
--------------------------------------------------------------------------------

const            0.2291      0.046      4.933      0.000       0.138       0.320

Adventure       -0.1554      0.133     -1.171      0.242      -0.416       0.105

Fighting         0.0801      0.130      0.614      0.539      -0.176       0.336

Misc             0.0727      0.117      0.620      0.535      -0.158       0.303

Platform         0.2200      0.138      1.595      0.111      -0.051       0.491

Puzzle          -0.0425      0.355     -0.120      0.905      -0.740       0.655

Racing           0.0780      0.124      0.628      0.530      -0.166       0.322

Role-Playing     0.0223      0.099      0.225      0.822      -0.173       0.218

Shooter          0.5752      0.096      6.010      0.000       0.387       0.763

Simulation      -0.1606      0.235     -0.684      0.495      -0.622       0.301

Sports           0.1881      0.091      2.072      0.039       0.010       0.366

Strategy        -0.1891      0.208     -0.908      0.364      -0.598       0.220

Omnibus:                      393.827   Durbin-Watson:                   1.809

Prob(Omnibus):                  0.000   Jarque-Bera (JB):             7172.279

Skew:                           3.503   Prob(JB):                         0.00

Kurtosis:                      20.509   Cond. No.                         13.2


Notes:

[1] Standard Errors assume that the covariance matrix of the errors is correctly specified.
                           
==============================================================================
Dep. Variable:               EU_Sales   R-squared:                       0.056
Model:                            OLS   Adj. R-squared:                  0.034
Method:                 Least Squares   F-statistic:                     2.567
Date:                Thu, 22 Sep 2022   Prob (F-statistic):            0.00362
Time:                        19:04:08   Log-Likelihood:                -476.28
No. Observations:                 484   AIC:                             976.6
Df Residuals:                     472   BIC:                             1027.
Df Model:                          11                                         
Covariance Type:            nonrobust                                         

                   coef    std err          t      P>|t|      [0.025      0.975]
                   
--------------------------------------------------------------------------------

const            0.2244      0.050      4.489      0.000       0.126       0.323
Adventure       -0.1331      0.143     -0.932      0.352      -0.414       0.148
Fighting        -0.0480      0.140     -0.342      0.733      -0.324       0.228
Misc            -0.0237      0.126     -0.188      0.851      -0.272       0.224
Platform         0.1275      0.148      0.859      0.391      -0.164       0.419
Puzzle          -0.0977      0.382     -0.256      0.798      -0.848       0.652
Racing           0.1556      0.134      1.165      0.245      -0.107       0.418
Role-Playing     0.0042      0.107      0.039      0.969      -0.206       0.214
Shooter          0.4307      0.103      4.183      0.000       0.228       0.633
Simulation      -0.1472      0.253     -0.582      0.561      -0.644       0.349
Sports           0.2110      0.098      2.161      0.031       0.019       0.403
Strategy        -0.2010      0.224     -0.897      0.370      -0.641       0.239

Omnibus:                      533.502   Durbin-Watson:                   1.923
Prob(Omnibus):                  0.000   Jarque-Bera (JB):            26816.547
Skew:                           5.135   Prob(JB):                         0.00
Kurtosis:                      37.990   Cond. No.                         13.2


Notes:

[1] Standard Errors assume that the covariance matrix of the errors is correctly specified.
                         
==============================================================================

Dep. Variable:               JP_Sales   R-squared:                       0.045
Model:                            OLS   Adj. R-squared:                  0.023
Method:                 Least Squares   F-statistic:                     2.021
Date:                Thu, 22 Sep 2022   Prob (F-statistic):             0.0249
Time:                        19:05:30   Log-Likelihood:                 313.79
No. Observations:                 484   AIC:                            -603.6
Df Residuals:                     472   BIC:                            -553.4
Df Model:                          11                                         
Covariance Type:            nonrobust                                         

                   coef    std err          t      P>|t|      [0.025      0.975]
                   
--------------------------------------------------------------------------------

const            0.0244      0.010      2.499      0.013       0.005       0.044
Adventure       -0.0094      0.028     -0.337      0.736      -0.064       0.045
Fighting         0.0368      0.027      1.341      0.181      -0.017       0.091
Misc             0.0262      0.025      1.062      0.289      -0.022       0.075
Platform         0.1101      0.029      3.796      0.000       0.053       0.167
Puzzle           0.0456      0.075      0.611      0.542      -0.101       0.192
Racing           0.0281      0.026      1.075      0.283      -0.023       0.079
Role-Playing     0.0370      0.021      1.771      0.077      -0.004       0.078
Shooter          0.0329      0.020      1.636      0.102      -0.007       0.072
Simulation      -0.0016      0.049     -0.032      0.975      -0.099       0.096
Sports          -0.0105      0.019     -0.549      0.583      -0.048       0.027
Strategy        -0.0144      0.044     -0.329      0.742      -0.101       0.072

Omnibus:                      658.221   Durbin-Watson:                   2.013
Prob(Omnibus):                  0.000   Jarque-Bera (JB):            81625.084
Skew:                           7.004   Prob(JB):                         0.00
Kurtosis:                      65.059   Cond. No.                         13.2


Notes:

[1] Standard Errors assume that the covariance matrix of the errors is correctly specified.
                  
==============================================================================

Dep. Variable:           Global_Sales   R-squared:                       0.075
Model:                            OLS   Adj. R-squared:                  0.054
Method:                 Least Squares   F-statistic:                     3.501
Date:                Thu, 22 Sep 2022   Prob (F-statistic):           0.000100
Time:                        19:06:21   Log-Likelihood:                -853.24
No. Observations:                 484   AIC:                             1730.
Df Residuals:                     472   BIC:                             1781.
Df Model:                          11                                         
Covariance Type:            nonrobust  


                   coef    std err          t      P>|t|      [0.025      0.975]
                   
--------------------------------------------------------------------------------

const            0.5522      0.109      5.070      0.000       0.338       0.766
Adventure       -0.3460      0.311     -1.112      0.267      -0.958       0.266
Fighting         0.0726      0.306      0.237      0.812      -0.528       0.673
Misc             0.0637      0.275      0.232      0.817      -0.477       0.604
Platform         0.4755      0.323      1.470      0.142      -0.160       1.111
Puzzle          -0.1422      0.832     -0.171      0.864      -1.777       1.492
Racing           0.2710      0.291      0.931      0.352      -0.301       0.843
Role-Playing     0.0667      0.233      0.286      0.775      -0.391       0.525
Shooter          1.1746      0.224      5.234      0.000       0.734       1.616
Simulation      -0.3636      0.551     -0.660      0.509      -1.446       0.719
Sports           0.4527      0.213      2.127      0.034       0.034       0.871
Strategy        -0.4722      0.488     -0.967      0.334      -1.432       0.488

Omnibus:                      456.702   Durbin-Watson:                   1.861
Prob(Omnibus):                  0.000   Jarque-Bera (JB):            14181.013
Skew:                           4.146   Prob(JB):                         0.00
Kurtosis:                      28.188   Cond. No.                         13.2


Notes:

[1] Standard Errors assume that the covariance matrix of the errors is correctly specified.

------------------------------------------------------------------------------------------------------------------

- This score does however mean that the accuracy is weaker than would be liked, however when these above variables were adjusted there was not a signifigant change. This accuracy issue could be the result of the size of the intial data set, and the resulting training size. Since we limited our consoles to certain generations there was only so much data available in the first place to conduct training with.  

- The p values do indicate that there is a relationship between sales in a particular region and the genre of a videogame. It is interesting to note that the p value was consistent through out the model, but North America and Japan had the better f statistic score. This could be due to the higher amount of data that is availabe for their model. In the future, more data for the other regions or focusing on specific countires would yeild more consistent data. 
The final regression model predictions are below: X axis indicates sales, Y axis is the numerical representations of the genres and match thier above coefficients.  

![NA regression prediction](https://user-images.githubusercontent.com/103790879/191971978-71e88fab-123e-4f99-9dcc-bf0918586d25.png)

![EU regression Prediction](https://user-images.githubusercontent.com/103790879/191971986-ed0906a5-3148-4c5e-9876-a4253aca6d87.png)

![Jp_Regression prediction](https://user-images.githubusercontent.com/103790879/191971996-871202a3-eaca-4b1c-8f39-05258d246252.png)

![GS_regression Prediction](https://user-images.githubusercontent.com/103790879/191972010-244f7722-2b9b-4039-b991-3b8e3ce5f12a.png)

 - Even with the data and accuracy issues, there is evidence to suggest that hisotical sales data can be used to predict if a game will sell better in certain regions. In the United states There is a correlation between certain genres, their sales, and the country they were sold in; for example, shooting games in North America sale better than in Japan. In Europe however, sports games have a higher chance of selling better than the other countries, and this tracks with the future predictions shown in the regression model. 

## Dashboard Links :

https://public.tableau.com/app/profile/diana.villarreal1441/viz/VideoGamesSalesAnalysis-Group4/Dashboard14?publish=yes

https://public.tableau.com/app/profile/diana.villarreal1441/viz/VideoGamesSalesAnalysis-GroupGenreYear/Dashboard12?publish=yes

https://public.tableau.com/app/profile/diana.villarreal1441/viz/VideoGamesSalesAnalysis-GroupSales/Dashboard1?publish=yes

https://public.tableau.com/app/profile/diana.villarreal1441/viz/VideoGamesSalesAnalysis-Group4TopGames/Dashboard13?publish=yes


## Presentation Link:

https://docs.google.com/presentation/d/1YTVxh378Mi2xpPuBV5jdmMxUdYK3iB-dB-H8gtijIBg/edit#slide=id.p










