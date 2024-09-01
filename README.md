# Predict-NBA-Points-Per-Game

## Project Overview
This project scrapes, cleans, visualizes and uses machine learning to predict the points per game of players from the 2024 NBA season. <br>
1. Web scrape player data from [`basketball-reference.com`](https://www.basketball-reference.com).<br>
2. Read in and clean the html using BeautifulSoup.<br>
3. Parse the individual statistiacs into pandas DataFrames that will be used for both visualizations and machine learning.<br>
4. Select features to identify good predictors, and train machine learning models to predict points per game.<br>

### Cool Techniques
1. Implemented `scikit learn` tools to create a 99.99% accurate `multiple regression model` to predict Points Per Game and to optimize a `K-Nearest Neighbors model`, a `Decision Tree Regressor model`, and a `Random Forest Regressor model`.
2. Used `seaborn` to visualize `Pearson Correlation` values and prevent overfitting of machine learning models by dropping highly correlated variables.
3. Created eaisly-digestible graphics using `matplotlib` and `plotly` of relevant relationships between variables <br>
![Open Position Counts](./Visualizations/PositionCounts.png)

### Challenges
1. I struggled with finding the proper methods to prevent over fitting in the machine learning models. First, I experimented with and creating visualizations of changes in the `Akaike Information Criterion (AIC)` and the `Bayesian Information Criterion BIC` values of my `Multiple Regression Model` to determine the optimal number of variables to include in the model, but the process lacked specificity, and was open to too much personal interpretation of what was "good enough". Next, I tried to use `Variance Inflation Factor (VIF)` to measure the severity of multicollinearity between variables and attempted to exclude values above a certain `VIF` threshold, but cutting off at the standard 5 `VIF` left me with only a few variables.
2. I haven't worked with machine learning techniques before, so the learning curve was steep, and I'm open to ways I can improve my analysis!

### What else I would have liked to do...
1. Implement a method to input values of variables used for prediction and have the machine learning model output a predicted value
2. Create visualizations for the machine learning models
3. Explore other machine learning techniques to model the data
4. See how well this model will predict `points per game` in future seasons

### Code
File Overview: <br>
   - `get_clean_data.ipynb`: web scrapes data, cleans it, and prepares two .csv files for visualization and modeling
   - `visualize.ipynp`: creates visualizations of relationships between variables in the data
   - `model.ipynb`: creates and optimizes four different machine learning models to predict  `Points Per Game` using the data

## Run this project yourself!
### 1. Local Setup <br>

Please install the following locally:
   - JupyterLab/JupyterNotebook
   - Python 3.8+
   - Python Packages
      - [`BeautifulSoup`](https://www.crummy.com/software/BeautifulSoup/bs4/doc/): Used for scraping html.
      - [`pandas`](https://pandas.pydata.org/docs/index.html): Used for cleaning and manipulating data.
      - [`matplotlib`](https://matplotlib.org/stable/index.html): Used for plotting and visualizing data.
      - [`plotly`](https://plotly.com/python/): Used for plotting and visualizing data.
      - [`seaborn`](https://seaborn.pydata.org): Used for visualizing correlations.
      - [`scikit learn`](https://scikit-learn.org/stable/): Used for creating maching learning models.

### 2. Data <br>

Either use the pre-scraped data set [`here`](https://drive.google.com/drive/folders/1Ywo_Pqlyr6psnKRL9X-ettpqIKeGAV_u?usp=share_link) and start running the code form the `visualize.ipynb` onward

**OR**

Run the `get_clean_data.ipynb` to scrape and clean the data yourself!
