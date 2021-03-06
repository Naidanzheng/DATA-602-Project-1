# Life Expectancy Prediction(WHO)

#####    by <b>[Naidan Zheng](https://github.com/Naidanzheng)</b>

---

## Repo Content
- <b>Data</b> - The raw dataset can be found on the [Kaggle website](https://www.kaggle.com/augustus0498/life-expectancy-who). 
- <b>[images](https://github.com/Naidanzheng/DATA-602-Project-1/tree/main/Image)</b> - Various plots and images used in the documents found in this repo.
- <b>[DATA602 Project 1.ipynb](https://github.com/Naidanzheng/DATA-602-Project-1/blob/main/DATA602%20Project%201.ipynb)</b> - The main Jupyter Notebook containing the models and analysis for this project.
- <b>[Presentation1](https://github.com/Naidanzheng/DATA-602-Project-1/blob/main/Presentation1.pptx)</b> - The presentation for this project. The presentation [video](https://www.youtube.com/watch?v=4KKAqstCGxc&t=60s).
- <b>[README.md](README.md)</b> - A description of the project goals, process, and results.

---

## Table of Content
- <b>[Overview](https://github.com/Naidanzheng/DATA-602-Project-1/blob/main/README.md#overview) 
- <b>[Goals](https://github.com/Naidanzheng/DATA-602-Project-1/blob/main/README.md#goals) 
- <b>[Motivation & Background](https://github.com/Naidanzheng/DATA-602-Project-1/blob/main/README.md#motivation--background) 
- <b>[Data](https://github.com/Naidanzheng/DATA-602-Project-1/blob/main/README.md#data) 
- <b>[Modeling](https://github.com/Naidanzheng/DATA-602-Project-1/blob/main/README.md#modeling) 
- <b>[Conclusion](https://github.com/Naidanzheng/DATA-602-Project-1/blob/main/README.md#conclusion) 
- <b>[Future Work](https://github.com/Naidanzheng/DATA-602-Project-1/blob/main/README.md#future-work) 
- <b>[Software Requirements](https://github.com/Naidanzheng/DATA-602-Project-1/blob/main/README.md#software-requirements) 
- <b>[Resource](https://github.com/Naidanzheng/DATA-602-Project-1/blob/main/README.md#resource) 


---
## Overview
The Global Health Observatory (GHO) data repository under the World Health Organization (WHO) keeps track of the health status as well as many other related factors for all countries. The dataset has 22 Columns and 2938 rows which meant 20 predicting variables. All predicting variables were then divided into several broad categories:Immunization related factors, Mortality factors, Economical factors, and Social factors. The objects of this project are to determine the critical factors which are more representative, build regression models(Linear Regression, Lasso Regression, Random Forest Regressor,etc.), and compare their mean square errors and R^2 scores to choose the best regression model to predict life expectancy accurately. 
![life.png](https://github.com/Naidanzheng/DATA-602-Project-1/blob/main/Image/life.png)



## Goals
The first goal for this project is to search for the elements which effects life expectancy by using statistical tools such as MSE, R squared, RMSE, ect. on different regression models.

The second goal for this project is to find the best regression model to predict life expectancy.

The third goal for this project is to find the answer for research questions.

### Research Questions
    1: What are the major variables affecting the life expectancy?
    2: What is the impact of schooling on the lifespan of humans?
    3: What is the impact of Immunization coverage on life Expectancy?

## Motivation & Background
Life expectancy is an educated prediction of human life. Through the comparative analysis of life expectancy, it can reflect the quality of life of a society and measure the health level of people in this country (or region). Everyone wants to have a longer life expectancy, and it can be affected by a lot of factors. Life expectancy is not only one of the important indicators to measure the health of the population, but also a comprehensive indicator to measure the level of economic and social development of a country or region. In population quality evaluation and prediction, disease burden measurement, and national economy and residents’ quality of life evaluation, life expectancy and other indicators are among the most basic research content. I am very interested in this topic because I am studying Health Informatics, and I hope to combine these two different expertise to analyze life expectancy.


## Data
This dataset is comprised of data from all over the world from various countries aggregated by the World Health Organization. The data is an aggregate of many indicators for a particular country in a particular year. In essence, the data is multiple indicators in a time series separated by country. 

The dataset has 22 Columns and 2938 rows which meant 20 predicting variables. All predicting variables were then divided into several broad categories: Immunization related factors, Mortality factors, Economical factors, and Social factors. 

This graph shows the different life expectancy in developed and developing countries. The average life expectancy of developed countries is 78.69 years, the average life expectancy of developing countries is 67.69 years. There is a large difference of min life expectancy between developed(69.9 years) and developing(44 years) countries. It may be because developing countries have better infrastructure, healthcare, welfare than developing countries.

![Status1.png](https://github.com/Naidanzheng/DATA-602-Project-1/blob/main/Image/Status1.png)

![Status.png](https://github.com/Naidanzheng/DATA-602-Project-1/blob/main/Image/Status.png)

This graph shows the correlation between features. These variables will be used to create models to predict life expectancy.
![Correlation.png](https://github.com/Naidanzheng/DATA-602-Project-1/blob/main/Image/Correlation.png)

There is a strong correlation relationship between 'Schooling' and 'Life Expectancy' of 0.728. This may be because education is more established and prevalent in wealthier countries.

Surprisingly, there is a moderate positive correlation between ‘Alcohol’ and ‘Life Expectancy’ of 0.40, it may be because only wealthier countries can afford alcohol or the consumption of alcohol is more prevalent among wealthier populations.


## Modeling 
From the correlation matrix, 'Schooling' and 'Income Composition' are the major positive impacts of life expectancy, and 'Adult Mortality' is the major negative impact of life expectancy. In this project, we will stay away from Time Series Analysis, so we choose all the variables that except 'Years' to build regression models.

The five regression models that created are Linear Regression, Lasso Regression, Ridge Regression, ElasticNet Regression, and Random Forest Regressor, the way to choose the best model is to calculate their mean square errors and R^2 scores.
![r_2.png](https://github.com/Naidanzheng/DATA-602-Project-1/blob/main/Image/r_2.png)
![mse.png](https://github.com/Naidanzheng/DATA-602-Project-1/blob/main/Image/mse.png)

Data is more concentrated in the Random Forest Regressor Model.
![rf.png](https://github.com/Naidanzheng/DATA-602-Project-1/blob/main/Image/rf.png)

In this project, the best model is Random Forest Regressor, because it has the highest R^2 score(0.9475), and the lowest mean square error(4.147). Therefore, we will use Random Forest Regressor to predict life expectancy by using these given variables.

## Conclusion
Life expectancy is determined by immunization related factors, mortality factors, economical factors, and social factors. 'Schooling' and 'Income Composition' are the major positive impacts of life expectancy, and 'Adult Mortality' is the major negative impact of life expectancy.

In this project, the best model is Random Forest Regressor, because it has the highest R^2 score(0.9475), and the lowest mean square error(4.147). Therefore, we will use Random Forest Regressor to predict life expectancy by using these given variables.

## Future Work
To derive even more accurate results, we'd like to expand the project with additional data, specifically 'Years'. Therefore, we will use the Time Series analysis to improve our model.
Also, we can add 'gender','exercise' and 'crime rates' variables to analyze the relationships with life expectancy.
## Software Requirements
<pre>
Languages    : Python 3.9.0
Tools/IDE    : Anaconda, Colab
Libraries    : numPy,pandas, matplotlib, seaborn, scipy.stats, scikit-learn,warning
</pre>

<pre>
Duration     : October 2020
Last Update  : 10.12.2020
</pre>

## Resource
- <b>[7 types regression technique](https://www.analyticssteps.com/blogs/7-types-regression-technique-you-should-know-machine-learning)
- <b>[Machine Learning Algorithms in Python](https://medium.com/towards-artificial-intelligence/machine-learning-algorithms-for-beginners-with-python-code-examples-ml-19c6afd60daa)
