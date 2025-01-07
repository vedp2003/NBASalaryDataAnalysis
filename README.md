# NBA Player Salary Prediction 

Initial data science project focuses on analyzing NBA player performance data and predicting player salaries using data analysis and machine learning models. The analysis identifies key metrics influencing salaries and provides actionable insights through data visualization, database queries, and modeling.

---

## Datasets

The dataset was sourced from Kaggle. The data can be found here: [NBA Salary Dataset](https://www.kaggle.com/datasets/loganlauton/nba-players-and-team-data). The two important datasets used are 'NBA Player Stats.csv' and 'NBA Salaries.csv'. 

---

## Key Steps implemented in this project

### Data Preprocessing and Cleaning
1. Merged the player statistics and salary datasets to include player performance statistics, positions, teams, and salaries. This involved joining the datasets on common attributes. 
2. Handled missing values and outliers across key features like points, assists, rebounds, and salary. This involved data cleaning, handling Null Values, and removing outliers using the Z-Score Method.
3. Converted numerical columns to the appropriate data types for mathematical operations.
4. Standardized features and scaled data where necessary.

### Feature Engineering
We derived new variables from existing ones to better capture underlying patterns in the data.
1. **Weighted Efficiency (WEFF)**: Combines points, assists, rebounds, steals, blocks, and turnovers, normalized by games played.
2. **Points Per Game (PPG)**: Points scored divided by games played.
3. **Assists Per Game (APG)**: Assists divided by games played.
4. **Rebounds Per Game (RPG)**: Total rebounds divided by games played.
5. **Steals Per Game (SPG)**: Steals divided by games played.
6. **Blocks Per Game (BPG)**: Blocks divided by games played.
7. **Turnovers Per Game (TPG)**: Turnovers divided by games played.
8. **Usage Rate**: Estimate of a player's involvement in offensive plays, based on field goals attempted, free throws attempted, and turnovers.
9. **Shooting Efficiency**: Average of field goal percentage and effective field goal percentage.
10. **Offensive Contribution**: Weighted sum of points, assists, and offensive rebounds.
11. **Defensive Contribution**: Sum of defensive rebounds, steals, and blocks.
12. **Experience**: Estimated years of professional activity, assuming players start their careers at age 19.
13. **Games Started Percentage (GS%)**: Games started as a percentage of games played.
14. **Impact Score**: Weighted Efficiency (WEFF) per minute played
15. **Minutes Played per game (MPG): Total minutes played divided by games played
16. **Efficiency Tiers**: Players categorized into low, moderate, and high efficiency tiers.
   
### Exploratory Data Analysis (EDA)
1. **Visualization**:
   - Created plots to see the correlation of different metrics with Salary to find which metric was important.
   - Made visualizations for each numeric metric vs salary to find the best features for predicting salary 
   - Some plots we made include: 
      - Visualized salary trends by position, efficiency, and season using bar plots, scatter plots, and line plots.
      - Created more salary related visualizations to better see trends for predicting overall salary based on player stats and performance.

### SQL Integration
1. Created a relational SQLite database for querying player statistics.
2. Build a schema and then inserted our dataset information in the local database
3. Executed advanced SQL queries for aspects such as:
   - Analyzed salary trends in relation to NBA player stats, performance metrics, and efficiency.
   - Explored year-on-year salary growth and distribution across seasons.
   - Examined salary variations across different age groups and career stages.
   - Investigated the impact of specific contributions (offensive/defensive) and efficiency on player earnings

4. By incorporating database management, we were able to easily query and find salary related trends, helping us build the overall machine learning model.

### Machine Learning Models
1. **Linear Regression**:
   - Established a baseline model for salary prediction. This model didnt perform too well. 
   - Evaluated using Mean Squared Error (MSE), Mean Absolute Error (MAE), and R² score.
2. **Decision Tree Regressor**:
   - Improved prediction accuracy by capturing non-linear relationships. It uses decision trees to predict.
3. **Random Forest Regressor**:
   - Enhanced the model by reducing overfitting and improving robustness. This works by combining the predictions of multiple decision trees. This turned out to be the best model with a relatively high R² value. 


### Local Dashboard
1. Integrated an user interactive dashboard using `ipywidgets` to dynamically input player statistics and predict salaries.
2. Added a slider and textboxs for value inputs. 
3. Used a trained Random Forest Regressor model (best performing model) to predict salaries dynamically.
4. Displayed predicted salaries after button click to create an user friendly dashboard. 

---

## Requirements

The following libraries were used that must be imported:
- `pandas`
- `numpy`
- `matplotlib`
- `seaborn`
- `scikit-learn`
- `sqlite3`
- `statsmodel`
- `ipywidgets`

---
