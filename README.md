# ![](https://ga-dash.s3.amazonaws.com/production/assets/logo-9f88ae6c9c3871690e33280fcf557f33.png) Project: Analysis of Liquor Store Sales in Iowa

### Overview

This was a project completed for the Data Science Immersive class at General Assembly.

[Link to Slides](https://docs.google.com/presentation/d/1Sew0YxC-nzIhU0iMshjbGm6K3D_gJt7or9HEQkoBl-0/edit?usp=sharing)

# Maximizing ACME Store Profits in Iowa
Austin Lasseter - February 9, 2018

# What’s our goal?
This analysis is written to advise a fictitious liquor company regarding its business strategy in the State of Iowa.
The analysis aims to answer to questions on behalf of the company:
• What is the optimal range of bottles ordered and price per bottle?
• Which counties in Iowa are the optimal locations to open new stores?

# Where are the data from?
### Dataset 1: Liquor Sales
The source of the data was the Iowa ABD. The data include about 1,400 liquor stores, and represents all sales in the year 2015.
An important caveat is that the data are sales _from the state to the store_, not from the store to the consumer. So, `retail` means "The amount the store paid for each bottle of liquor ordered". We do not have actual data about sales from stores to consumers.
The ABD dataset is located here: https://data.iowa.gov/Economy/Iowa-Liquor-Sales/m3tr-qhgy

### Dataset 2: County Characteristics
The second dataset is from the US Department of Agriculture. It includes information about each of the 99 counties in the state of Iowa.
The data contain the following variables: Population, Rural/Metro status, Unemployment, Median Income. The last two were informative for the exploratory analysis, but were not used in the final regression analysis because they did not add any explanatory power after the inclusion of the other variables. The USDA dataset is located here:
https://www.ers.usda.gov/data-products/county-level-data-sets/county-level-data-sets-download-data/

