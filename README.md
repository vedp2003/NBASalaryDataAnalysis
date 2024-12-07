# Predicting NBA Player Salaries with Machine Learning

This project focuses on analyzing NBA player performance data and predicting player salaries using machine learning models. The analysis identifies key metrics influencing salaries and provides actionable insights through data visualization and modeling.

---

## Dataset

The dataset was sourced from Kaggle. Make sure to download it from the following link: [NBA Salary Dataset](https://kaggle.com) and place it in the project directory as `nba_salaries.csv`.

---

## Key Steps

### Data Preprocessing and Cleaning
1. Merged multiple datasets to include player performance statistics, positions, teams, and salaries.
2. Handled missing values and outliers across key features like points, assists, rebounds, and salary.
3. Converted numerical columns to the appropriate data types for mathematical operations.
4. Standardized features and scaled data where necessary.

### Exploratory Data Analysis (EDA)
1. **Correlation Analysis**:
   - Analyzed relationships between metrics like Weighted Efficiency (WEFF) and salary.
   - Computed correlations to find the most impactful features.
2. **Visualization**:
   - Visualized salary trends by position, efficiency, and season using bar plots, scatter plots, and line plots.
   - Identified top-performing players based on WEFF.
   - Created heatmaps to compare average salaries by position, efficiency tier, and season.

### Feature Engineering
1. Calculated Weighted Efficiency (WEFF) using player performance metrics.
2. Binned players into efficiency tiers: Low, Moderate, and High Efficiency.
3. Added derived columns to enhance feature richness for model training.

### Machine Learning Models
1. **Linear Regression**:
   - Established a baseline for salary prediction.
   - Evaluated using Mean Squared Error (MSE), Mean Absolute Error (MAE), and R² score.
2. **Decision Tree Regressor**:
   - Improved prediction accuracy by capturing non-linear relationships.
3. **Random Forest Regressor**:
   - Enhanced the model by reducing overfitting and improving robustness.

### SQL Integration
1. Created a relational SQLite database for querying player statistics.
2. Executed advanced SQL queries to:
   - Analyze salary trends by position and efficiency.
   - Identify high-performing, low-salary players.
   - Explore year-on-year salary growth across seasons.

---

## Flow of the Project

1. **Setup and Environment**:
   - Clone this repository and open the Jupyter Notebook file `finalProj.ipynb` in a Python notebook platform like Jupyter Notebook or an online IDE such as CodeBench.

2. **Data Import**:
   - The notebook imports multiple `.csv` files containing player statistics, salaries, and team information.
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
   - Executes queries to analyze salary trends, identify top players, and evaluate team performance.

6. **Machine Learning**:
   - Trains regression models (Linear Regression, Decision Tree, and Random Forest) to predict salaries based on player performance metrics.
   - Evaluates models using metrics like Mean Absolute Error (MAE), Root Mean Squared Error (RMSE), and R² score.

7. **Final Outputs**:
   - Identifies key insights, such as top players by Weighted Efficiency, salary-to-performance ratio, and team-level salary analysis.

---

## Requirements

The following libraries were used:
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
   git clone https://github.com/yourusername/nba-salary-prediction.git
   
2. Navigate to the project folder:
   ```bash
   cd nba-salary-prediction

3. Download the dataset from Kaggle and save it as `nba_salaries.csv`.
4. Open and run the Jupyter notebook `finalProj.ipynb` cell by cell to execute the analysis.

