# Predicting NBA Player Salaries with Machine Learning

This project focuses on analyzing NBA player performance data and predicting player salaries using data analysis and machine learning models. The analysis identifies key metrics influencing salaries and provides actionable insights through data visualization, database queries, and modeling.

---

## Dataset

The dataset was sourced from Kaggle. The data can be downloaded from here: [NBA Salary Dataset](https://www.kaggle.com/datasets/loganlauton/nba-players-and-team-data). The two important datasets used are 'NBA Player Stats.csv' and 'NBA Salaries.csv'.

---

## Key Steps implemented in this project

### Data Preprocessing and Cleaning
1. Merged the player statistics and salary datasets to include player performance statistics, positions, teams, and salaries. This involved joining the datasets on common attributes. 
2. Handled missing values and outliers across key features like points, assists, rebounds, and salary. This involved data cleaning and handling Null Values. 
3. Converted numerical columns to the appropriate data types for mathematical operations.
4. Standardized features and scaled data where necessary.

### Feature Engineering
1. Calculated Weighted Efficiency (WEFF) using player performance metrics.
2. Binned players into efficiency tiers: Low, Moderate, and High Efficiency.
3. Added derived columns to enhance feature richness for model training.
   
### Exploratory Data Analysis (EDA)
1. **Correlation Analysis**:
   - Analyzed relationships between metrics like Weighted Efficiency (WEFF) and salary.
   - Computed correlations to find the most impactful features.
2. **Visualization**:
   - Visualized salary trends by position, efficiency, and season using bar plots, scatter plots, and line plots.
   - Identified top-performing players based on WEFF.
   - Created heatmaps to compare average salaries by position, efficiency tier, and season.
   - Created more salary related visualizations to better see trends for predicting overall salary based on player stats and performance.

### SQL Integration
1. Created a relational SQLite database for querying player statistics.
2. Build a schema and then inserted our dataset information in the local database
3. Executed advanced SQL queries for aspects such as:
   - Analyze salary trends by position and efficiency.
   - Identify high-performing, low-salary players.
   - Explore year-on-year salary growth across seasons.
4. By incorporating database management, we were able to easily query and find salary related trends, helping us build the overall machine learning model.

### Machine Learning Models
1. **Linear Regression**:
   - Established a baseline for salary prediction.
   - Evaluated using Mean Squared Error (MSE), Mean Absolute Error (MAE), and R² score.
2. **Decision Tree Regressor**:
   - Improved prediction accuracy by capturing non-linear relationships.
3. **Random Forest Regressor**:
   - Enhanced the model by reducing overfitting and improving robustness. This turned out to be the best model with a relatively high R² value. 


---

## Flow of the Project

1. **Setup and Environment**:
   - Clone this repository and open the Jupyter Notebook file `finalProj.ipynb` in a Python notebook platform like Jupyter Notebook or CodeBench.

2. **Data Import**:
   - The notebook imports multiple `.csv` files containing player statistics/info and salaries. This was downloaded fromthe Kaggle data link. 
   - Reads and retrieves the data using `pandas` and merges datasets into a consolidated DataFrame.

3. **Data Cleaning and Processing**:
   - Handles missing values and outliers.
   - Converts numerical columns to appropriate data types.
   - Performs feature engineering to calculate metrics like Weighted Efficiency (WEFF).

4. **Visualization**:
   - Creates various plots and charts (e.g., bar plots, scatter plots, heatmaps) to understand trends and relationships in the data.
   - Analyzes salary trends by season, player position, and efficiency tiers.

5. **SQL Queries**:
   - Transfers the data into an SQLite database.
   - Executes queries to analyze salary trends, identify top players, evaluate team performance, etc. 

6. **Machine Learning**:
   - Trains regression models (Linear Regression, Decision Tree, and Random Forest) to predict salaries based on player performance metrics.
   - Evaluates models using metrics like Mean Absolute Error (MAE), Root Mean Squared Error (RMSE), and R² score.

7. **Final Outputs**:
   - Identifies key insights, such as top players by Weighted Efficiency, salary-to-performance ratio, and team-level salary analysis.
   - Creates a good model that can help predict NBA player salaries in future seasons/years given their current stats/performance.

---

## Requirements

The following libraries were used that must be imported:
- `pandas`
- `numpy`
- `matplotlib`
- `seaborn`
- `scikit-learn`
- `sqlite3`

---

## Steps to Run the Project

1. Clone this repository:
   ```bash
   git clone https://github.com/vedp2003/NBAMachineLearningProject.git
   
2. Navigate to the project folder:
   ```bash
   cd NBAMachineLearningProject

3. Download the dataset csvs from Kaggle.
4. Open and run the Jupyter notebook `finalProj.ipynb` cell by cell to execute the analysis (you can open this and run it on CodeBench or other Python platforms that allow Python Notebooks)

## Video Demo

Watch the full video demo [here](https://youtube.com).


