# TATA--visulization-project

## Task -1 
- An online retail store has hired you as a consultant to review their data and provide insights that would be valuable to the CEO and CMO of the business. 
- They would also like to view different metrics based on the demographic information that is available in the data.
- Create a set of four questions that you anticipate each business leader will ask and want to know the answers to. 

## Task- 2
- to pick the right visulization for diffrent scenario.
- tabulue and powe BI These are the brilliant tool to perform data cleaning, data preprocessing, and data visualization in many analytics projects.
- plotnine is a data visualization package for the programming language Python that is inspired by the ggplot2 package for R. It allows users to create a wide range of static, animated, and interactive visualizations in Python.

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
* theme_bw() is a function in the ggplot2 package that sets the default theme for a plot to a simple black and white theme.
* function to create a new plot object, and then use functions like geom_point() and geom_line() to add layers to the plot.

## charts 
1. line graph(number)/ trend
 Whether you’re analyzing sales data, whether you’re looking at year-on-year profit, whether you’re looking at how a person’s salary increases in the last year, line charts are very helpful in these scenarios.
2. bar grapgh 
The only difference between them is that in a bar chart, values are represented on the X-axis and categories on the Y-axis.
3. column graph 
similar as bar , column will be resprented on x-axies
4. scaltter plot(number)
continous varibales , Scatter plots are useful for showing a correlation between the data points that may not be easy to see from the data alone.
5 histogram - for frequency(number)
6.Pie Chart
If you want to represent your categorical data as part of the whole, then you should use a pie chart.


- a linear approach for modelling the relationship between a scalar response and one or more explanatory variables (also known as dependent and independent variables).
```
(ggplot(mtcars, 
        aes('wt', 'mpg', 
            color='factor(gear)'))
        + geom_point() 
        + stat_smooth(method='lm') 
        + theme_bw())
```
	![alt text](linear.png)
	
