
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

## Discriptions of the communication Protocols

- We communicate our project related tasks through Slack and via zoom meetings.
- Each team member give their regular updates about the progress and changes via slack messages.

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


