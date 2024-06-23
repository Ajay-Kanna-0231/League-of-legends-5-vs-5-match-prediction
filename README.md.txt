
# League of Legends Match Prediction

This project aims to predict the outcome of League of Legends matches using machine learning techniques. Match details from top players were extracted, and numerical encoding and feature engineering were performed to train and validate the models.



## Features

- Extracted 1705 match IDs and it's details from top player's histories for training.
- Achieved over 95% accuracy on the validation set.

## Features Used to predict the outcome:

- Kills, Deaths, and Assists (KDA): The number of kills, deaths, and assists each team has.
- Champion Class Distribution: Instead of using all 190 individual champions as features, which would result in 190 features, we grouped champions by their classes. This reduced the number of features to 6, corresponding to the six champion classes, thereby improving the model's efficiency.
- (Tier + Rank) Scores: The average (tier + rank) score of all the players on each team.
- Champion Experience and Level: Each champion gains experience and levels up during the game, which increases their health, attack, and speed. To accurately represent a champion's strength, we combined experience and level into a single feature by multiplying them. This accounts for the significant boost in stats that occurs when a champion levels up. For example, a champion with 1000 experience has a notable advantage over the same champion with 999 experience, as reaching 1000 might result in a level increase and corresponding stat boost.
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
## Usage
- Run `scripts/get_match_ids.ipynb` to get all the match IDs from the player's history:
  - Get the game name and tag line from [OP.GG Leaderboards](https://www.op.gg/leaderboards/tier).
  - The game name is the username of the player/summoner which comes before the hashtag, and the tag line is the part that comes after the hashtag. It's stored as shown below in my code:
    ```python
    game_name = ['Zven', 'Dongdanny', 'wxtonytoppwd']
    tag_line = ['KEKW1', 'pwdd', 'NA1']
    ```
  - assign ```self.REGION ``` the location used by the player you are interested in
  - Now generate your API key from [riot developer portal](https://developer.riotgames.com/) and change it to your API key in my code ``` API_KEY = 'RGAPI-e7a0cc73-2a12-4b8e-b909-71c950ac8132' ```
- To get to know about puuid or to get location of a player based on puuid ... visit https://developer.riotgames.com/apis where I will be mostly using ```SUMMONER V4, LEAGUE V4, MATCH V5```. 
- Now you have the list of match IDs, run the ```make_training_dataset.ipynb``` to get the details of all the match IDs, refer ``` MATCH V5 ``` under ```/lol/match/v5/matches/{matchId}```
- Likewise make the test data set as well if you are not going to use mine
- Now run ```model_train_validation.ipynb```and ```model_test.ipynb```
## Contributing

Contributions are always welcome!

See `contributing.md` for ways to get started.

Please adhere to this project's `code of conduct`.


## Authors

- [@Ajay Kanna](https://github.com/Ajay-Kanna-0231)

