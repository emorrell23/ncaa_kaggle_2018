# March Madness Kaggle Competition
## Using machine learning to predict the 2018 NCAA tournament

This repository is for my entry into the 2018 Machine Learning Kaggle competition for the Men's NCAA Tournament. The goal for the competition was to use historical college basketball data to build a machine learning model to predict the probability of a team winning every possible matchup in this year's tournament. 

I used game by game data for every regular season and tournament game since 1985 to build my model, which was provided by Kaggle. The features that I used for the model were a team's ELO score and a team's recent statistical performance. An ELO score is basically a team's rating, based on game-by-game data and updated after each game. I used a variation of the ELO score used by fivethirtyeight.com (more info here: https://fivethirtyeight.com/features/how-our-march-madness-predictions-work/#anchor). In addition to that I used box score statistics in additions to some additional stats that I created using the box score statistics. For these I used only the stats from a team's previous 9 games.

Once I had all of that data I was able to build my model (I used a Gradient Boost Classifier) and input the teams that made the tournament to predict the probability of each team winning a game against every other potential opponent. Each submission was evaluated on the log loss of the model, where a smaller log loss is better. Log loss provides extreme punishment for being both confident and wrong, but more reward if the model is both confident and correct. 

My entry finished with a log loss of 0.5385 and was 114th out of 934 entries (top 12%). It correctly predicted 3 of the 4 Final Four teams (Michigan, Kansas and Villanova) and correctly predicted Villanova to win.

For more info on how I went about this, please check out my code (Kaggle 2018 NCAA.ipynb)
