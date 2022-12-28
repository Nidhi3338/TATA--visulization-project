# TATA--visulization-project

## Task -1 
- An online retail store has hired you as a consultant to review their data and provide insights that would be valuable to the CEO and CMO of the business. 
- They would also like to view different metrics based on the demographic information that is available in the data.
- Create a set of four questions that you anticipate each business leader will ask and want to know the answers to. 

## task- 2
- to pick the right visulization for diffrent scenario.

We always start by loading up and looking at the dataset we want to analyze and visualize. 
```
from plotnine import *
from plotnine.data import mtcars

mtcars.head()
```
We choose a dot or scatter plot in this case for our geometric object to represent each data point.
```
(ggplot(mtcars, 
        aes('wt', 'mpg', 
            color='factor(gear)'))
        + geom_point() 
        + facet_wrap('~cyl') 
        + theme_bw())
```
