# 4300_Anime_recommendation
Our application is an innovative personalized Anime Recommendation System that leverages the rich information found in anime datasets. The application is designed to help users discover new anime tailored to their preferences.


## Abstract

The Anime recommendation engine is a system that recommends anime titles to users based on their preferences and viewing history. The goal of this project is to improve the user experience of anime streaming services by providing personalized and relevant recommendations to users. The working hypothesis of the project is that by analyzing user behavior and preferences, we can predict which anime titles will be of interest to the user and provide them with personalized recommendations. To test this hypothesis, we used a dataset of user ratings and viewing history for anime titles and trained a collaborative filtering model to make personalized recommendations. Our results showed that the collaborative filtering model was able to make accurate recommendations for users and that the personalized recommendations led to increased user engagement and satisfaction with the service. In conclusion, our project demonstrates the effectiveness of using machine learning algorithms to provide personalized recommendations for anime titles. This work is relevant to researchers and practitioners in the fields of machine learning, recommendation systems, and entertainment.
 
## Introduction 

The motivation behind an Anime recommendation engine is to help users discover new anime titles that they are likely to enjoy based on their preferences and viewing history. With the vast number of anime titles available, it can be overwhelming and time-consuming for users to search through all of the options and find something they will enjoy. A recommendation engine can help to solve this problem by using algorithms and models to analyze user behavior and preferences and suggest anime titles that are likely to be of interest to the user. The main goal of our system is to improve the user experience by providing personalized and relevant recommendations. This can increase user engagement and satisfaction with the service, as well as potentially increase the number of titles watched by users. The working hypothesis behind the system is that by analyzing user behavior and preferences, we can predict which anime titles will be of interest to the user and provide them with personalized recommendations. The engine can take into account factors such as genre, themes, animation style, and user ratings to make these predictions. This work is significant because it has the potential to improve the user experience of anime streaming services and increase user engagement and satisfaction. 

## Methods

### Data wrangling, data cleaning, and data mining: 

The AnimeList dataset we found on Kaggle (https://www.kaggle.com/datasets/hernan4444/anime-recommendation-database-2020) contains 35 columns and more than 10 thousand of rows of anime data. Each anime entity has the ratings given by users to the anime that they have watched completely and information about the anime like genre, stats, studio, etc[1].

To recommend anime based on the users’ preferences accurately, we think it is crucial to maintain a clean database as the anime library.  To recommend anime based on genres, we split the text column containing a list of genres and selected the top three genres for each individual anime for convenience after dropping all NaN values and Null values. 

To clean the anime dataset, we first eliminated the irrelevant columns from the original dataset, including "title_english", "title_japanese", "title_synonyms", "image_url", "status", "aired", "background", "related", "licensor", "opening_theme", "ending_theme". Regarding the anime title, we kept the English title of each anime and renamed it as the title. The “image_url”, "status", "aired", "background", "related", "licensor", "opening_theme", and "ending_theme" columns are irrelevant to our project purpose for anime recommendations, so we deleted them. 

After all the cleaning procedures, we have 2672 rows and 22 columns in total. 

###  Data transformation: 

The length_of_eposide column is about the duration of each episode of each anime, and we modified the columns to contain only numerical values to state the duration of each episode in minutes. 

## User Guidance of GUI window: 
GUI user guidance:
To initiate our Anime Recommendation engine with the GUI to input anime preferences, please first start your neo4j on your local computer:
1. Change the user's neo4j username and password. The neo4j username and password are for loading the dataset into the neo4j server. 
2.  Run the whole Python program via Jupyter Notebook, and ensure that you have the AnimeList.csv file in the same directory as this Anime_Recommendation_GUI.ipynb file. 
3. When the GUI window popped up, the user can input their preferred anime(s) into the input text box.
4. Click the Get Recommendation button to acquire the recommendation results.
5. The user should acquire no more than 5 recommended anime based on his/her input.
    - If you have the "Sorry, there are no recommended animes for you. We will improve our system to find out your recommendation!" in the output box, it means that your preferred anime is not available in our database or our program did not find any recommended anime for your due to lack of data. 

