# project2
#Board Game Complexity Analysis

**Created by Will Stith
7/19/2020**

**Introduction**

This folder contains files pertinent to Will Stith's second project for Metis. The project is a regression analysis of board game complexity based off of data pulled from boardgamegeek.com. For the execution of this project, 686 board games were sampled from boardgamegeek.com and data on their characteristics were put into a dataframe. Linear regression was performed on the dataset to try and build a model which could predict a board game's complexity based on features such as playing time, popularity, forums, and game mechanics. The model presented on was brought down to 15 variables by lasso regularization (alpha ~ 0.0365) and yielded a final r^2 ~ 0.6409.

**Requirements**

Python 3.?
Necessary modules (listed below)

**Necessary modules**

- pickle
- pandas
- seaborn
- matplotlib
- numpy
- scipy
- sklearn
- statsmodels
- re
- requests
- BeautifulSoup
- xml
- selenium

**Data**

All data for this project was scraped from boardgamegeek.com in a random manner. Not included are pickled saves of board game samples collected during this project.

**Contents**

*project2_url_collection.ipynb* - contains code required to pull urls of random games not excluded from the project sample.
*project2_data_scraping.ipynb* - contains code which accesses each url from the previous notebook and builds a dictionary of dictionaries containing data for each game.
*project2_dataframe_cleaning.ipynb* - contains code for creating a clean dataframe which will be usable in the analysis stage. Some EDA is handled in this notebook as well.
*project2_modeling.ipynb* - contains code for trying out linear models on the previously cleaned dataframe, as well as visualizations of said models.

**Instructions**

In order to recreate a similar regression model to the one I created for this project, follow the four notebooks from the contents section in order. Between notebooks, checkpoints will be pickled to be used in the next notebook. Be sure to collect no more than 150 urls at a time with the url collection function, as its recursive nature causes it to hit a wall after a few thousands iterations (~1000 iterations are required to pull a sample of 100 given the selection criteria). If building a larger dataset, run the url_compiiler function multiple times, turn each dictionary into a dataframe, and then concatenate those dataframes into one.

**Acknowledgements**

I'd like to thank all the Metis instructors and TAs for their incredible ongoing support for this project and others. Additionally, I'd like to thank my fellow Metis students for helping to foster a positive, collaborative, and welcoming work environment.
