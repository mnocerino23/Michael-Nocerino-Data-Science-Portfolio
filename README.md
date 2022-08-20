# Michael-Nocerino-Data-Science-Portfolio


About Me:
My name is Michael Nocerino, and I am a rising senior at Santa Clara University (SCU) in Northern California majoring in Math (Data Science Emphasis) and minoring in Computer Science. I have an analytical background with strong exposure to probability and statistics, discrete math, programming in Python and C++, data mining, cleaning, visualization, and supervised machine learning from the program at SCU thus far.

The first two data science courses I took my junior year provided a glimpse into the powerful applications of machine learning algorithms and left me feeling extremely motivated to explore the subject in greater depth. From self-learning in my free time during this spring and summer, I have added additional skills such as SQL, Tableau, and the fundamentals of deep learning, developing these skills through a variety of data science projects which required me to learn on the fly as I completed necessary tasks step by step. This summer I primarily worked on a research project through SCU in which I explored wildfire trends (from 2001-2019) in the state of California and attempted to analyze trends as well as predict high risk areas experimenting with machine learning techniques. I also worked on a variety of personal projects involving topics such as Major League Baseball salary prediction, board game strategy, and analyzing student engagement data within the hiking club I'm involved in at Santa Clara. I am not intinmidated to learn new Python libraries, programming languages, technologies, and techniques on my own along the way and have found self-learning and completing projects to be very rewarding. I have thoroughly enjoyed the process and growing my knowledge outside of the classroom through online content such as LinkedIn Learning and YouTube series.

My personal interests include nature and the outdoors, sports (MLB, NBA, and skateboarding) and environmental issues and it's been extremely fascinating to explore questions related to these interests through a data lens. Since this past spring, I have been hooked on using Python, visualization tools, and machine learning to explore questions that fascinate me. My goal is to apply my curiosity and passion for analytics to help provide valuable data driven insight to an organization helping guide business decisions in a data science, data analyst, or related role after graduating from college in June 2023. Below, I provide summaries of the projects I have been working on over the past year (all can be found here: https://github.com/mnocerino23?tab=repositories) and share some relevant visuals.

1. California Wildfire Forecaster

Received a grant from Santa Clara University to work on a data science research project this summer with Dr. Smita Ghosh in which I perform an in-depth analysis on wildfires in the state of California since the year 2000 with the goal of predicting high risk areas within the state with ML models. Queried a government SQLite database containing information on millions of U.S. Wildfires to extract data for over 100,000 California forest fires since the year 2000. Performed cleaning and modifications on this dataset in addition to another smaller Kaggle dataset containing recent california wildfire data to ensure that both datasets contained consistent features and formatting. From there, I was able to request monthly weather data for the past 20 years in different areas of California from the National Oceanic and Atmospheric Administration (NOAA) that I would eventually add on to each fire in the two datasets. This included features such as average wind, min and max temperatures during each month, days exceeding 90 degrees within the month, percepitation statistics and was able to map each fire to its closest NOAA weather station within California (utilized a function that finds the NOAA station with the shortest haversine distance -distance calculated between locations given coordinates- from the fire) and the weather there during the month and the year of the fire. In addition to this, I gathered March snow related data (total snowpack, snow water content, snow density) from 20 mountain peaks of the most relevant river basins in the Sierra Nevada (mountainous area of California) from the California Department of Water Resources, restructured, and cleaned the data in Pandas so that it could be added on to each fire that occured in a county that receives snow (mapped to each station once again using shortest haversine distance). I engineered four additional features with the weather data I had gathered and the date-time library such as number of heatwaves in the two months before the fire and total percipitation during the rainy season before the fire. Finally, I utilized public geographical APIs to extract the elevation each fire occured at as well as the county for fires who were missing a value. Having cleaned and prepped the two datasets, I then went on to experiment with building machine learning models, taking both classification and regression approaches. Experimented with multi-class classification algorithms (such as KNN, SVM, Naive Bayes, Gradient Boosting, Decision Tree, Random Forest, and Deep Neural Networks) to try to classify past fires by size (Small, Medium, or Large) so that this model could be used to also predict areas that are at high risk for large forest fires. While the multi-class classifiers struggled to perform well, I also experimented with regression techniques (such as multi-linear, ridge, lasso, decision tree, and neural network regressions) to predict acres burned, which I found to be more effective. I am currently in the process of experimentation with different algorithms and hyperparameters to tune the best multi-class classification and regression models as I finish up my project this month.

![Wildfire tableau](https://user-images.githubusercontent.com/81653555/185754770-53419d59-2baa-4692-8388-d0db30ee0ba1.JPG)

![2018](https://user-images.githubusercontent.com/81653555/185754850-a59e0032-f082-491c-bcc4-83061b03cf78.JPG)


Technologies used: SQL (SQLite), Python (Matplotlib, Pandas, Regular Expression, Requests, Scikit-Learn, Seaborn, TensorFlow), Tableau


2. Major League Baseball Player Salary Prediction

Personal project in which I explore player stats with the goal of building models to predict player salary (in millions) for pitchers and hitters in Major League Baseball. Cleaned two datasets, one with pitcher stats and one with position player hitting stats, in Pandas and created visualizations in Seaborn to understand the distributions of various stats throughout the league in addition to the features that correlate with high salary. I trained machine learning models with Scikit-Learn and TensorFlow to predict player salary for position players, pitchers, starting pitchers, and relief pitchers utilizing multivariate linear, ridge, lasso, decision tree and neural network regression techniques. Utilized techniques such as cross validation and tuning of model parameters with GridSearch. In the end, I was able to produce regression models for both position players and pitchers with mean absolute errors under 3 million USD (player salaries in the dataset ranged from 140k to 35 million USD). I am currently working to build specific seperate models for starting pitchers and relief pitchers to lower MAE as much as possible.

![salary vs age](https://user-images.githubusercontent.com/81653555/183914933-a449e935-93e6-4801-a2ec-2cc8792291e0.JPG)
![salary2](https://user-images.githubusercontent.com/81653555/185754950-e19d6d71-bd40-47e7-a36e-0d59063b4cb1.JPG)

![MLB guitar](https://user-images.githubusercontent.com/81653555/183914333-947a77ec-bd28-44bd-8ba9-71fb7c973002.JPG)

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


![Day Hike](https://user-images.githubusercontent.com/81653555/183910569-309c8e54-d674-4868-8f0d-5222602c0725.JPG)





![ITW Overnights](https://user-images.githubusercontent.com/81653555/183909835-dc41becb-4306-47c7-a932-f7068390bb2f.JPG)




![ITW pricing](https://user-images.githubusercontent.com/81653555/183909840-ccf350ed-28cf-4363-9750-17e03fa7e1d5.JPG)

Overnight Trips (2021-2022 School Year) Tableau Visuals:

![Overnights_Overview1](https://user-images.githubusercontent.com/81653555/183911802-d06aa820-c1ef-41df-9761-e53cff58b948.JPG)

![weekly w quarter](https://user-images.githubusercontent.com/81653555/183911830-96ca4ae0-e138-4b7b-8fa3-1e30b4d70cf9.JPG)
![Meter](https://user-images.githubusercontent.com/81653555/183912457-17718c03-de41-443f-b7e9-2669e5845cde.JPG)


![Quarterly signup](https://user-images.githubusercontent.com/81653555/183912019-c2e073be-4a85-4e4f-88e0-f4156d9b1423.JPG)


4. Winner's Circle (Board Game) Strategy Analysis

The goal of this project was to determine the best horses to bet on and devise a stratgey for the board game Winner's Circle. I entered all of the horse cards in the game into a csv with the length of each horses run depending on the dice roll. I wrote a program to simulate a round of Winner's Circle taking into account the rules and restrictions of the game, ran it 100,000 times, and calculated win percentages for every horse. I then investigated whether the difference in win percentage between horses is statistically significant and what features correlate with a high win percentage. 

Technologies Used: Python (Pandas, Seaborn)

Dataset of horses with run lengths for each dice roll (the dice sides are head, helmet, saddle, and horshoe in this game) and additional engineered features:
![Winners circle 2](https://user-images.githubusercontent.com/81653555/183908365-f94bf29d-2a6b-4a1c-b5c3-e336a55014c0.JPG)

The Eight Best Horses (with the Highest Winning Percentages) after the Simulation of 100,000 Games:
![Top horses](https://user-images.githubusercontent.com/81653555/183915854-873cc95d-707c-4339-9a14-9009a792bab7.JPG)



