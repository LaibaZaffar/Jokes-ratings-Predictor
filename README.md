# Jokes Rating Prediction System

This repository contains a Jokes Rating Prediction System that utilizes user ratings of jokes to predict the ratings for the jokes. It uses both a collaborative recommender and a random recommender for prediction. The system is evaluated using Mean Absolute Error (MAE). This project is implemented in Python and utilizes libraries such as NumPy, Pandas, and others.

## Dataset Information

The Jokes Rating Prediction System leverages the Jester Dataset 3, which consists of user ratings for jokes. Below is a detailed description of the dataset:

### Jester Dataset 3
- **Link**: [Eigentaste Dataset](https://eigentaste.berkeley.edu/dataset/)
- **Dataset Description**:
  - The dataset contains 2.3 million ratings, ranging from -10.00 to +10.00, for 100 jokes provided by 73,421 users. The data was collected between April 1999 and May 2003.
  - An updated version includes 150 jokes (50 not in Dataset 1) with over 115,000 new ratings from 82,366 total users, collected from November 2006 to March 2015.

### Jokes Texts
- **File**: `jester_dataset_2/3_joke_texts.zip` (29KB)
- **Format**:
  - Excel spreadsheet with 150 rows.
  - The row number corresponds to the joke ID used in the ratings data.
  - The first 100 jokes and their IDs are consistent with those in Dataset 1.

### Ratings Data
- **File**: `jester_dataset_3.zip` (6MB)
- **Format**:
  - Excel file representing a 54,905 by 151 matrix (users by jokes).
  - The left-most column contains the total number of jokes rated by the user.
  - The dataset includes 54,905 users and 150 jokes.
  - Ratings range from -10.00 to +10.00. A rating of 99 indicates a null rating (user did not rate the joke).
  - 22 jokes with few ratings were removed as of May 2009 due to being outdated.

## Usage

1. **Dataset Preparation**:
   - Download the `jester_dataset_3.zip` and `jester_dataset_2/3_joke_texts.zip` files from the [Eigentaste Dataset](https://eigentaste.berkeley.edu/dataset/) and unzip them.
   - The unzipped files should contain the user ratings for jokes and the joke texts, respectively.

2. **Ratings Predictor System**:
   - The Jokes Rating Prediction System is implemented in the `Jokes Recommender.ipynb` Jupyter Notebook.
   - Load the dataset into the notebook and run the cells to test the recommender system and generate joke predictions.

3. **Evaluation**:
   - The system is evaluated using Mean Absolute Error (MAE) to assess the accuracy of the predictions.

## Features

- **Collaborative Filtering**: The system uses collaborative filtering techniques to generate joke predictions.
- **Random Recommender**: A baseline random recommender is implemented for comparison.
- **Real-Valued Ratings**: The dataset contains real-valued ratings, providing a richer input for the recommendation algorithm.


