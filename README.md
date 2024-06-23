
# League of Legends Match Prediction

This project aims to predict the outcome of League of Legends matches using machine learning techniques. Match details from top players were extracted, and numerical encoding and feature engineering were performed to train and validate the models.



## Features

- Extracted 1705 match IDs and it's details from top player's histories for training.
- Achieved over 95% accuracy on the validation set.

## Folder Structure
- data/
  - train_data_set.csv: Training dataset containing features and labels.
  - test_data_set.csv: Test dataset for evaluating the model.
- notebooks/
  - model_train_validation.ipynb: Notebook for training and validating the model.
  - model_test.ipynb: Notebook for testing the model on unseen data.
  - best_model_info.pkl: Pickle file containing the best model and its parameters.
- scripts/
  - get_match_ids.ipynb: Script to retrieve match IDs using Riot Games API of top players.
  - make_training_dataset.ipynb: Script to create the training dataset from match details.
  - list_of_match_details_for_testing.pkl: Pickle file with match details for testing.
  - list_of_match_details_for_training.pkl: Pickle file with match details for training.
  - list_of_match_ids_for_testing.pkl: Pickle file with match IDs for testing.
  - list_of_match_ids_for_training.pkl: Pickle file with match IDs for training.
- README.md: Overview of the project, setup instructions, and usage guidelines.
- requirements.txt: List of dependencies required for the project.
- about_the_game.txt: Information needed about League of Legends game, to understand my code.
## Requirements
- Ensure you have Python installed, along with the required libraries listed in requirements.txt.
- Clone the repository: 
```bash
git clone https://github.com/your_username/league-of-legends-prediction.git
cd league-of-legends-prediction
```
- Install dependencies:
```bash
pip install -r requirements.txt
```
## Usage/Examples



