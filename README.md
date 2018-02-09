# Maximizing ACME Store Profits in Iowa
A presentation to ACME by Dunder Mifflin Consulting, LLC

Austin Lasseter - February 9, 2018
# What’s our goal?

ACME asked Dunder Mifflin Consulting to determine:
What is the optimal range of bottles ordered and price per bottle?
Which counties in Iowa are the optimal locations to open new stores?

# Where is our data from?
### Dataset 1: Liquor Sales
Source: Iowa ABD
Number of stores: About 1,400
Year: All sales in 2015
Caveat: All sales from state to store

### Dataset 2: County Characteristics
Source: US Department of Agriculture
Contains: Population, Rural/Metro status, Unemployment, Median Income
# How do we define a store’s annual profit?
(Retail-Wholesale) x Bottles
Mark up by 18%, SUM
Average profit = $48,249

# What is the optimal number of bottles?
Average order to Iowa ABD: 10.1 bottles per order
Stores that place larger orders tend to have higher annual revenue, up to a point

# What is the optimal price point?
o maximize annual profit, stores should focus on bottles priced $15-$20 (wholesale)
This is target is above the average order of $13.6 per bottle (wholesale)

# Do metro counties have higher profits?
Stores in non-metro, non-rural counties have higher annual profits
“Non-metro”: Urban population of 20,000 or more, not adjacent to a metro area

# Does county saturation impact profit?
Stores in under-saturated counties have higher profits

# How much can our prediction explain?
Our model explained about 15% of the variability in stores’ annual profit

# Recommendations
Stores should order bottles in above-average quantities of 10-20.
Stores should order bottles in the price range of $15-$20 per bottle.
Ideal counties are non-metro and undersaturated.
A new store in Wapello county is predicted to have an annual profit that is $30,430 higher than similar stores in other counties.
A new store in Cerro Gordo is predicted to have an annual profit that is $43,940 higher than similar stores in other counties.
