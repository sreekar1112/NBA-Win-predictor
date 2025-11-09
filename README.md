# NBA-Win-Predictor

This project predicts the winner of an NBA basketball game using real match statistics. The goal is to use team stats such as total points, rebounds, assists, turnovers, fouls, blocks, steals and home advantage to determine which team is most likely to win.

---

## Dataset
The dataset used is from Kaggle and includes:
- **games.csv** (final match results)
- **games_details.csv** (player-level statistics)
- **teams.csv** (team information)

Using **GAME_ID**, the datasets were merged and player statistics were converted into team totals so each team has one row per game.

---

## Features Used
| Feature | Meaning |
|---------|---------|
| TOTAL_PTS | Total points scored |
| TOTAL_REB | Rebounds |
| TOTAL_AST | Assists |
| TOTAL_STL | Steals |
| TOTAL_BLK | Blocks |
| TOTAL_TO  | Turnovers |
| TOTAL_PF  | Personal fouls |
| IS_HOME   | Home advantage (1 = home, 0 = away) |

**Target Variable:** `TEAM_WON` → 1 if the team won, 0 if they lost

---

##  Model Training
Models used:
- Logistic Regression
- Random Forest
- **XGBoost (Best model)**

XGBoost achieved **~73% accuracy**, which is strong considering only match statistics were used.

---

##  Interactive Prediction Tool
Inside the notebook:
- Select 2 teams
- Enter their game stats
- Click **Predict Winner**
- Model returns:
   predicted winning team  
   winning probability for both teams

---

##  What This Project Demonstrates
✔ Using machine learning for real sports analytics  
✔ Feature engineering & dataset merging  
✔ Practical prediction interface in Google Colab  

---

##  Technologies Used
- Python
- Pandas / NumPy
- Scikit-learn
- XGBoost
- Kaggle dataset
- ipywidgets

