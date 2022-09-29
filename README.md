
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

- North America score
                          
![ML 1](https://user-images.githubusercontent.com/96400887/193138950-c6577495-4e8d-40c7-91b3-92d9690c3924.png)

- Europe score

![ML 2](https://user-images.githubusercontent.com/96400887/193140157-37aedafc-9ddc-4bed-b73b-7f190d54633b.png)

- Japan score

![ML 3](https://user-images.githubusercontent.com/96400887/193140176-8c9f6eb7-7d57-460f-944b-244b2f7f75ef.png)

- Global score

![ML 4](https://user-images.githubusercontent.com/96400887/193140191-872d7134-0c87-493c-87d9-8a75dfba4182.png)



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

https://github.com/jwetapatel/VideoGameSalesAnalysis_based-on-Genre-vs-Region/blob/main/Presentation/Group%204%20-%20Video%20Game%20Sales%20Analysis%20(1).pptx











