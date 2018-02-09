# Maximizing ACME Store Profits in Iowa
A presentation to ACME by Dunder Mifflin Consulting, LLC

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

# How do we define a store’s annual profit?
As mentioned above, we don't have actual data about sales to consumers, so it was necessary to infer it. I calculated the annual profit of each store as the profit that ABD made on its sales to each store, multiplied mark-up value of 18%. Profit was calculated as the wholesale cost of each bottle minus its retail cost, times the number of bottles in the order, and summed across all orders made by the store in 2015, times the mark-up value. The average profit of a liquor store in Iowa was $48,249. I excluded 74 stores with annual profits above $300,000, as well as an additional 12 stores with outlier values for average price or number of bottles ordered.

# What is the optimal number of bottles?
The average order to the Iowa ABD was 10.1 bottles per order. Stores that place larger orders tend to have higher annual revenue, up to a point. The optimal order size was 10-20 bottles per order; stores in this range had the highest average annual profit.

# What is the optimal price point?
To maximize annual profit, stores should focus on bottles priced $15-$20 (wholesale). This target is above the average order of $13.6 per bottle (wholesale). Stores whose average ordered-bottle price was above or below this range tended to have lower annual profits.

# Do metro counties have higher profits?
Stores in non-metro, non-rural counties have higher annual profits, all else being equal. “Non-metro” counties have an urban population of 20,000 or more, not adjacent to a metro area, according to the USDA.

# Does county saturation impact profit?
Saturation is defined as the number of people in the county per liquor store. Stores in under-saturated counties have higher profits, all else being equal. However, only a couple of counties had a saturation rate of higher than 3,000.

# Recommendations
* The two regression models predicted the annual profit of liquor stores in Iowa in 2015. The first model included 4 predictors: average bottle price, average number of bottles ordered, county saturation, and the urban/metro status of the county. All predictors were significant, suggesting that stores in non-metro, highly saturated counties would have higher profit. The first model thus identified 5 counties for further research.
* The second regression model included 7 predictors: average bottle price, average number of bottles ordered, and dummy variables for the five non-metro counties. Two of the five counties (Wapello, Cerro Gordo) had significant, positive coefficients. Therefore, we predict that these two counties are the best locations for a new liquor store. A store in these counties will make close to twice the average annual profit of average liquor stores in Iowa.

# How much can our prediction explain?
Our model explained about 15% of the variability in the outcome, stores’ annual profit. This is not unusual: a typical social science regression study might expect to explain 10-30% of variance in the outcome. I validated the model using two methods: train-test split, and 5-fold validation. These methods both confirmed the robustness of the model, explaining about 14% of the variability in the outcome.

# Additional research
With higher quality data, the study could be improved. Ideally, the improved model would incorporate data about actual sales to consumers. In addition, the improved model would have data about stores that aren't included here.


A new store in Wapello county is predicted to have an annual profit that is $30,430 higher than similar stores in other counties.
A new store in Cerro Gordo is predicted to have an annual profit that is $43,940 higher than similar stores in other counties.
