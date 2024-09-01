# Predict-NBA-Points-Per-Game

## Project Overview
This project scrapes, cleans, visualizes and uses machine learning to predict the points per game of players from the 2024 NBA season. 1. Web scrape player data from [`basketball-reference.com`](https://www.basketball-reference.com).
2. Read in and clean the html using BeautifulSoup
3. Parse the individual statistics into pandas DataFrames that will be used for both visualizations and machine learning
4. Select features to identify good predictors, and train machine learning models to predict points per game

## How the Project Works

1. **Installation**:
   - Clone the repository: `git clone https://github.com/your-username/MyProject.git`
   - Navigate to the project directory: `cd MyProject`
   - Install required packages: `pip install -r requirements.txt`

2. **Usage**:
   - Run the main script: `python main.py`
   - Follow the on-screen instructions to input your data.
   - View the generated visualizations in the `output` folder.

3. **Details**:
   - The project takes input data in CSV format and processes it using `pandas`.
   - It then visualizes the data with `matplotlib`, generating plots that are saved to the `output` directory.
  
4. **Examples**
   - ![Average Points Per Game VS Position] (./Average Points Per Game VS Position.png)
  

## Packages
- [`BeautifulSoup`](https://www.crummy.com/software/BeautifulSoup/bs4/doc/): Used for scraping html.
- [`pandas`](https://pandas.pydata.org/docs/index.html): Used for cleaning and manipulating data.
- [`matplotlib`](https://matplotlib.org/stable/index.html): Used for plotting and visualizing data.
- [`seaborn`](https://seaborn.pydata.org): Used for visualizing correlations.
- [`scikit learn`](https://scikit-learn.org/stable/): Used for creating maching learning models.
