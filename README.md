# Predicting NBA Player Salaries with Machine Learning

This project focuses on analyzing NBA player performance data and predicting player salaries using data analysis and machine learning models. The analysis identifies key metrics influencing salaries and provides actionable insights through data visualization, database queries, and modeling.

---

## Dataset

The dataset was sourced from Kaggle. The data can be downloaded from here: [NBA Salary Dataset](https://www.kaggle.com/datasets/loganlauton/nba-players-and-team-data). The two important datasets used are 'NBA Player Stats.csv' and 'NBA Salaries.csv'. We have also added these dataset csv files to this repository folder. We downloaded the zip file and extracted the CSV files, which are now available in this GitHub repository. Download these from the Github repository and ensure the data files are in the same directory as the other files including the Jupyter notebook.

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
14. **Impact Score**: Weighted Efficiency (WEFF) per minute played.
15. **Efficiency Tiers**: Players categorized into low, moderate, and high efficiency tiers.
   
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
   - Analyze salary trends in relation to NBA player stats/performance metrics
   - Explore year-on-year salary growth across seasons.
4. By incorporating database management, we were able to easily query and find salary related trends, helping us build the overall machine learning model.

### Machine Learning Models
1. **Linear Regression**:
   - Established a baseline model for salary prediction. This model didnt perform too well. 
   - Evaluated using Mean Squared Error (MSE), Mean Absolute Error (MAE), and R² score.
2. **Decision Tree Regressor**:
   - Improved prediction accuracy by capturing non-linear relationships. It uses decision trees to predict. 
3. **Random Forest Regressor**:
   - Enhanced the model by reducing overfitting and improving robustness. This works by combining the predictions of multiple decision trees. This turned out to be the best model with a relatively high R² value. 

### Interactive Dashboard
1. Integrated an user interactive dashboard using `ipywidgets` to dynamically input player statistics and predict salaries.
2. Added a slider for values (e.g., Age, FG, Season). 
3. Used a trained Random Forest Regressor model (best performing model) to predict salaries dynamically.
4. Displayed predicted salaries after button click to create an user friendly dashboard.

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
   - Create robust models that can help predict NBA player salaries in future seasons/years given their current stats/performance.
     
7. **Interactive Dashboard**:
   - Implements an user interacgive dashboard using `ipywidgets` to allow users to input player stats dynamically.
   - Predicts salaries using the best performing model (Random Forest Regressor) and displays results interactively.

---

## Requirements

The following libraries were used that must be imported:
- `pandas`
- `numpy`
- `matplotlib`
- `seaborn`
- `scikit-learn`
- `sqlite3`
- `ipywidgets`


---

## Steps to Run the Project

1. Clone this repository:
   ```bash
   git clone https://github.com/vedp2003/NBAMachineLearningProject.git
   
2. Navigate to the project folder:
   ```bash
   cd NBAMachineLearningProject

3. Download the dataset csvs from Kaggle. Save them in the same directory/folder as the Jupyter notebook. 
4. Open and run the Jupyter notebook `finalProj.ipynb` cell by cell to execute the analysis (you can open this and run it on CodeBench or other Python platforms that allow Python Notebooks)
5. Additional steps and installations may be needed to successfully run the Interactive Dashboard on the notebook. See below for steps

## Setup for Interactive Dashboard

To enable the interactive dashboard in Jupyter Notebook, follow these steps:

1. **Verify Node.js and npm**:
   Run the following commands to check if Node.js and npm are installed and their versions:
   ```bash
   node -v
   npm -v
   
2. . **Upgrade Node.js if necessary**:
   If your Node.js version is below 20.0.0, you may need to upgrade it using the following commands:
   ```bash
   wget https://nodejs.org/dist/v20.8.0/node-v20.8.0-linux-x64.tar.xz
   tar -xf node-v20.8.0-linux-x64.tar.xz
   mv node-v20.8.0-linux-x64 /path/to/your/directory/nodejs  # Replace /path/to/your/directory with the directory you want
   export PATH=/path/to/your/directory/nodejs/bin:$PATH  # Replace with the same directory as above

3. **Make sure updated Node.js path is active:-**:
   You can ensure the updated Node.js path is active by running this:
    ```bash
    import os
    os.environ['PATH'] = "/path/to/your/directory/nodejs/bin:" + os.environ['PATH']  Replace /path/to/your/directory with the directory
    
5. **Install required Python packages**:
   Install the necessary Python packages for widgets functionality:
   ```bash
   pip install --user ipywidgets
   pip install --user jupyterlab-widgets

6. **Install JupyterLab extensions**:
   Install the required JupyterLab extensions for enabling widgets:
   ```bash
   jupyter labextension install @jupyter-widgets/jupyterlab-manager

7. **Rebuild JupyterLab and Restart the Kernel**:
   After installing the extensions, rebuild JupyterLab to integrate the changes. Restart the kernel to ensure all updates take effect.
   It can be rebuilt by running: !jupyter lab build
   
   ### NOTE
   The commands listed above can be executed in the terminal. However, these commands can also be run directly within Jupyter Notebook cells by adding a `!` in front of each command. For example:
   ```bash
   !pip install --user ipywidgets
   !jupyter labextension install @jupyter-widgets/jupyterlab-manager --app-dir=$(jupyter --data-dir)/lab   #This installs the extensions in your home director
   !jupyter labextension install @jupyter-widgets/jupyterlab-manager #You can rrun this as well if there are no permission constraints


---

## Video Demo

We have a video demo going through our project. Watch the full video demo [here](https://youtube.com).

