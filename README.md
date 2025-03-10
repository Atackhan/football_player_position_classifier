# ⚽ Football Player Analysis & Position Prediction

## 📌 Project Overview
This project analyzes football player statistics and predicts their primary positions using various machine learning models. The dataset is sourced from **Transfermarkt** and **WhoScored**, containing detailed player performance metrics, including passing, shooting, and defensive actions.

## 🏆 Goals of the Project
- Clean and preprocess football player data.
- Perform exploratory data analysis (EDA) to identify key metrics.
- Train multiple machine learning models to predict player positions.
- Compare models based on accuracy and classification metrics.
- **Future Update**: Reclassify positions into broader categories (Goalkeeper, Defender, Midfielder, Forward) for improved prediction accuracy.

---

## 📂 Dataset Description
The dataset includes various player statistics from different leagues and teams. Below are some key features:

- **Player Name**: Name of the football player.
- **Player Team**: Club the player belongs to.
- **Team Formation**: Tactical formation used by the team (e.g., 4-2-3-1, 4-3-3).
- **Player Age**: Age of the player.
- **Player Height**: Height in centimeters.
- **Position 1**: Primary playing position.
- **Position 2**: Secondary playing position.
- **Mins Played**: Total minutes played in the season.
- **tacklePerGame**: Average tackles per game.
- **interceptionPerGame**: Average interceptions per game.
- **totalPassesPerGame**: Total passes per game.
- **passSuccess**: Pass accuracy percentage.
- **accurateCrossesPerGame**: Successful crosses per game.
- **accurateLongPassPerGame**: Successful long passes per game.
- **accurateThroughBallPerGame**: Successful through balls per game.
- **xG (Expected Goals)**: Total expected goals for the season.
- **xGPerNinety**: Expected goals per 90 minutes.
- **totalShots**: Total shots taken.
- **xGPerShot**: Expected goals per shot.
- **rating**: Overall player rating.

---

## 🧹 Data Preprocessing
### Handling Missing Values
- Converted `xGPerNinety` to numeric values.
- Filled missing values with the **median** for `xGPerNinety`.
- Used `.fillna(0)` to replace remaining NaN values.

### Feature Encoding
- Applied **Label Encoding** to the `Position 1` column.

### Feature Selection
- Removed non-relevant features like `Player Name`, `Player Team`, `Team Formation`, `Player Age`, `Mins Played`, and `rating` for machine learning training.

---

## 🤖 Machine Learning Models
The project trains and evaluates different models using **GridSearchCV** for hyperparameter tuning.

### Model Performance

| Model                 | Accuracy |
|-----------------------|---------|
| 🌲 **Random Forest**  | 42.50%  |
| 🎯 **SVM**            | 40.29%  |
| 🔥 **XGBoost**        | 40.54%  |
| 🐱 **CatBoost**       | 42.99%  |
| 🧠 **MLP Neural Network** | 41.19%  |

### 🏆 Best Model
- **Best Model**: CatBoost Classifier  
- **Best Score**: 42.99%  

---

## 🔄 Planned Improvements
While the initial classification results are promising, the accuracy can be improved by reclassifying player positions. Instead of predicting **detailed positional roles**, we will segment players into **four broader categories**:
1. **Goalkeepers (GK)**
2. **Defenders (CB, RB, LB, etc.)**
3. **Midfielders (CM, CDM, CAM, etc.)**
4. **Forwards (ST, LW, RW, etc.)**

This adjustment is expected to simplify the classification problem and improve accuracy.

---

## 📜 Data Sources
- **[Transfermarkt](https://www.transfermarkt.com/)** - Player transfers, market values, and position data.
- **[WhoScored](https://www.whoscored.com/)** - Player performance metrics (xG, tackles, passes, etc.).

---
