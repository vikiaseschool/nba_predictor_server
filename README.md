# NBA Results Predictor V2.0

## WARNING!

this application is only for educational purposes, please don't use it for betting. The model is not accurate enough and you may lose your money.

## Use of AI

I used ChatGpt and Github copilot extension. Some parts (I think like 10-20%) of my code are optimalized by AI, usually when operating with large datasets, model training optimalization or some GUI optimalization. Also some comments or code parts are upgraded by AI to make the code readable and structuable, but it is a minority of the code.

## Overview

This project is an NBA results predictor that uses machine learning models to predict the outcome of NBA games. The application provides predictions for the winning team, expected scores for both teams and prediction for starting five players PTS/REB/AST. Additionally, it offers statistics on the last games played by the teams and their head-to-head matchups.

## Features

- **Match Data Generation**: Creates a CSV file with match information for the specified teams and date.
- **Statistics Calculation**: Retrieves and calculates statistics for the last games played by the teams and their head-to-head matchups.
- **Prediction Models**: Uses trained machine learning models to predict the winning team, the scores and player statistics.
- **Web Interface**: A Flask-based web interface to input team names and date, and to display the predictions and statistics.

## Files

- `main.py`: Contains the core functions for retrieving team IDs, generating match data, calculating statistics, and making predictions.
- `GUI.py`: Flask application that provides a web interface for the user to input data and view predictions and statistics.
- `nba_data.py`: Functions to fetch and preprocess historical NBA game data.
- `nba_player_data.py`: Functions to fetch and preprocess historical NBA game data and player data.
- `players_training.py`: Script to train the machine learning models for predicting starting five players statistics.
- `results_training.py`: Script to train the machine learning models for predicting game outcomes and scores.
- `templates/web_gui.html`: HTML template for the main input form.
- `templates/result.html`: HTML template for displaying the prediction results and feedback form.
- `templates/statistics.html`: HTML template for displaying the game statistics.

## Requirements

- Python 3.x
- pandas
- joblib
- nba_api
- Flask
- scikit-learn
- imbalanced-learn

## Model accuracy test results
Match predictions:
- Accuracy of Win/lose prediction: 58%
- false win/lose [190 202], correct win/lose [191 329]
- Mean Squared Error for PTS team 1 prediction: 163.0
- Mean Squared Error for PTS team 2 prediction: 162.3
- Average percentage deviation for PTS team 1: 9.1%
- Average percentage deviation for PTS team 2: 9.2%

Player predictions:
- Points (PTS) R2 Score: 58.31%
- Rebounds (REB) R2 Score: 61.56%
- Assists (AST) R2 Score: 62.27%

## UPDATE DESCRIPTIONS
**V2.0 changes**
- made the project public via nest hosting
- added player points, assists and rebounds prediction
   - trained new model
- added feedback form
- made the GUI prettier

**V1.1 changes**
- repaired datasets, data are now more precise
- better trained model, accuracy increase + 2%
- added last 5 games stats

