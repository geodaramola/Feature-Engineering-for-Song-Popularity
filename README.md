Predicting Song Popularity with Engineered Audio Features

📌 Project Overview

Bassline.io is exploring whether its existing engineered audio features can effectively predict the popularity of a song. This project evaluates the usefulness of those features by building and interpreting a machine learning model to predict song popularity.

The goal is not to deploy a production-ready model, but rather to assess:

- Whether the current feature set has predictive value

- Which features contribute most to song popularity

- What limitations exist in the current feature engineering approach

🧠 Business Problem

The data science team at Bassline.io has previously engineered several audio-related features, including:

- Danceability

- Energy

- Acousticness

Before investing further effort into feature development, the team wants to understand:

- Are these features actually useful for predicting song popularity?

To answer this, we frame the task as a supervised regression problem where song popularity is predicted using the existing engineered features.

🎯 Objectives

Build a machine learning model to predict song popularity

- Evaluate model performance using Mean Squared Error (MSE)

- Interpret model results to determine feature usefulness

- Identify limitations of the current feature set

- Provide insights to guide future feature engineering efforts

## Conclusion
For this project, I created a machine learning pipeline that scales the data using MinMaxScaler, selects four features using SelectKBest, and applies a Decision Tree Regressor with a maximum depth of 3 for prediction. The pipeline configuration was chosen using GridSearchCV, which evaluated multiple models and their respective hyperparameters and selected the best estimator by minimizing the mean squared error (MSE).

The grid search identified an optimal estimator with a mean squared error of 405.7 using 4 features, using all the features will yield and MSE of about ~403, we can see that using these 4 features still yields a MSE close to the MSE using all the features. Since the primary objective of this project is to identify the most important features for predicting song popularity, the selected model—combined with SelectKBest—highlighted the following four features as most informative: danceability, instrumentalness, loudness, and audio_valence.

To tie the modeling approach back to the business problem, we begin with domain-driven expectations about how engineered audio features should relate to song popularity.

For example, we expect songs with high danceability to be more popular. Highly danceable tracks are more likely to be played in radio rotations, clubs, parties, and curated playlists, all of which increase exposure and listener engagement. As a result, danceability should have a positive relationship with song popularity.





