# Michael-Nocerino-Data-Science-Portfolio


About Me:
My name is Michael Nocerino, and I am a rising senior at Santa Clara University (SCU) in Northern California majoring in Math (Data Science Emphasis) and minoring in Computer Science. I have an analytical background with strong exposure to probability and statistics, discrete math, programming in Python and C++, data mining, cleaning, visualization, and supervised machine learning from my time at SCU.


1. California Wildfire Forecaster

Received a grant from Santa Clara University to work on a data science research project this summer with Dr. Smita Ghosh in which I perform an in-depth analysis on wildfires in the state of California since the year 2000 with the goal of predicting high risk areas within the state with ML models. Queried a government SQLite database containing information on millions of U.S. Wildfires to extract data for over 100,000 California forest fires since the year 2000. Performed cleaning and modifications on this dataset in addition to another smaller Kaggle dataset containing recent california wildfire data to ensure that both datasets contained consistent features and formatting. From there, I was able to request monthly weather data for the past 20 years in different areas of California from the National Oceanic and Atmospheric Administration (NOAA) that I would eventually add on to each fire in the two datasets. This included features such as average wind, min and max temperatures during each month, days exceeding 90 degrees within the month, precepitation statistics and was able to map each fire to its closest NOAA weather station within California (utilized a function that finds the NOAA station with the shortest haversine distance -distance calculated between locations given coordinates- from the fire) and the weather there during the month and the year of the fire. In addition to this, I gathered March snow related data (total snowpack, snow water content, snow density) from 20 mountain peaks of the most relevant river basins in the Sierra Nevada (mountainous area of California) from the California Department of Water Resources, restructured, and cleaned the data in Pandas so that it could be added on to each fire that occured in a county that receives snow (mapped to each station once again using shortest haversine distance). I engineered four additional features with the weather data I had gathered and the date-time library such as number of heatwaves in the two months before the fire and total precipitation during the rainy season before the fire. Finally, I utilized public geographical APIs to extract the elevation each fire occured at as well as the county for fires who were missing a value. Having cleaned and prepped the two datasets, I then went on to experiment with building machine learning models, taking both classification and regression approaches. Experimented with multi-class classification algorithms (such as KNN, SVM, Naive Bayes, Gradient Boosting, Decision Tree, Random Forest, and Deep Neural Networks) to try to classify past fires by size (Small, Medium, or Large) so that this model could be used to also predict areas that are at high risk for large forest fires. While the multi-class classifiers struggled to perform well, I also experimented with regression techniques (such as multi-linear, ridge, lasso, decision tree, and neural network regressions) to predict acres burned, which I found to be more effective. I am currently in the process of experimentation with different algorithms and hyperparameters to tune the best multi-class classification and regression models as I finish up my project this month.


Tableau Sample Graphics: 

![Wildfire tableau](https://user-images.githubusercontent.com/81653555/185754770-53419d59-2baa-4692-8388-d0db30ee0ba1.JPG)

![2018](https://user-images.githubusercontent.com/81653555/185754850-a59e0032-f082-491c-bcc4-83061b03cf78.JPG)


Technologies used: SQL (SQLite), Python (Matplotlib, Pandas, Regular Expression, Requests, Scikit-Learn, Seaborn, TensorFlow), Tableau


2. Major League Baseball Player Salary Prediction

Personal project in which I explore player stats with the goal of building models to predict player salary (in millions) for pitchers and hitters in Major League Baseball. Cleaned two datasets, one with pitcher stats and one with position player hitting stats, in Pandas and created visualizations in Seaborn to understand the distributions of various stats throughout the league in addition to the features that correlate with high salary. I trained machine learning models with Scikit-Learn and TensorFlow to predict player salary for position players, pitchers, starting pitchers, and relief pitchers utilizing multivariate linear, ridge, lasso, decision tree and neural network regression techniques. Utilized techniques such as cross validation and tuning of model parameters with GridSearch. In the end, I was able to produce regression models for both position players and pitchers with mean absolute errors under 3 million USD (player salaries in the dataset ranged from 140k to 35 million USD). I am currently working to build specific separate models for starting pitchers and relief pitchers to lower MAE as much as possible.

Salary vs. Age for Position Players:


![salary vs age](https://user-images.githubusercontent.com/81653555/183914933-a449e935-93e6-4801-a2ec-2cc8792291e0.JPG)

Hits vs. Games with Salary in Color for Position Players:



![salary2](https://user-images.githubusercontent.com/81653555/185754950-e19d6d71-bd40-47e7-a36e-0d59063b4cb1.JPG)

Player Salary Distribution by Position and Batting Stance:
![MLB guitar](https://user-images.githubusercontent.com/81653555/183914333-947a77ec-bd28-44bd-8ba9-71fb7c973002.JPG)

Training Neural Network to Predict Position Player Salary:


![Capture](https://user-images.githubusercontent.com/81653555/184680718-e63126d7-98be-47c8-9352-097299da4c4a.JPG)


Technologies used: Python (Matplotlib, Pandas, Scikit-Learn, Seaborn, TensorFlow)


3. Into the Wild Trips Yearly Review and Engagement Analysis

Ongoing project for my role within the student outdoors organization as data analyst. Perform data entry, cleaning, and visualization to create yearly trip reports and  analysis for Santa Clara University's student run outdoors organization, Into the Wild. For this role, using data that I collected and entered, I create visualizations and utilize other techniques to explore our organization's trip sales and factors preventing trips filling for both day hikes and overnight camping trips during the past school year. In addition to crafting Tableau visualizations and programming to answer questions regarding student engagement with the organization, I also improved the organizations data collection by creating new google forms so that we can efficiently collect trip and participant going forward. The questions I explore in this position include but are not limited to the following:

1. What are the most important factors that affect trip sign ups for both day hikes and overnights?
2. Are Friday overnights more popular/likely to fill than Saturday overnights?
3. How are trip sales affected by the quarter (Fall, Winter, Spring)?
4. What locations are in demand (trips we should run again) and which are not (trips we won't run again)?
5. How do sign up numbers vary with type of trip (car camping, backpacking, beach)?

Technologies used: Python (Pandas, Scikit-Learn, Seaborn), Tableau, PowerPoint








Overnight Trips (2021-2022 School Year) Tableau Visuals:

![ITW pricing](https://user-images.githubusercontent.com/81653555/183909840-ccf350ed-28cf-4363-9750-17e03fa7e1d5.JPG)

![Overnights_Overview1](https://user-images.githubusercontent.com/81653555/183911802-d06aa820-c1ef-41df-9761-e53cff58b948.JPG)

![weekly w quarter](https://user-images.githubusercontent.com/81653555/183911830-96ca4ae0-e138-4b7b-8fa3-1e30b4d70cf9.JPG)
![Meter](https://user-images.githubusercontent.com/81653555/183912457-17718c03-de41-443f-b7e9-2669e5845cde.JPG)


![Quarterly signup](https://user-images.githubusercontent.com/81653555/183912019-c2e073be-4a85-4e4f-88e0-f4156d9b1423.JPG)

![ITW Overnights](https://user-images.githubusercontent.com/81653555/185755871-ecee4642-e88a-4bd8-a8e0-cee017f0a224.JPG)


4. Winner's Circle (Board Game) Strategy Analysis

The goal of this project was to determine the best horses to bet on and devise a strategy for the board game Winner's Circle. I entered all of the horse cards in the game into a csv with the length of each horses run depending on the dice roll. I wrote a program to simulate a round of Winner's Circle taking into account the rules and restrictions of the game, ran it 100,000 times, and calculated win percentages for every horse. I then investigated whether there is a large difference in win percentage between horses and what features correlate with a high win percentage. 

Technologies Used: Python (Pandas, Seaborn)

Dataset of horses with run lengths for each dice roll (the dice sides are head, helmet, saddle, and horshoe in this game) and additional engineered features:
![Winners circle 2](https://user-images.githubusercontent.com/81653555/183908365-f94bf29d-2a6b-4a1c-b5c3-e336a55014c0.JPG)

The Eight Best Horses (with the Highest Winning Percentages) after the Simulation of 100,000 Games:


![Top horses](https://user-images.githubusercontent.com/81653555/183915854-873cc95d-707c-4339-9a14-9009a792bab7.JPG)



