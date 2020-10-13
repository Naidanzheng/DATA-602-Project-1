# Life Expectancy Prediction(WHO)

#####    by <b>[Naidan Zheng](https://github.com/Naidanzheng)</b>

---

## Repo Content
- <b>Data</b> - The raw dataset can be found on the [Kaggle website](https://www.kaggle.com/augustus0498/life-expectancy-who). 
- <b>[DATA602 Project 1.ipynb](DATA602 Project 1.ipynb)</b> - The main Jupyter Notebook containing the models and analysis for this project.
- <b>[Presentation](Presentation.pdf)</b> - The presentation for this project.
- <b>[README.md](README.md)</b> - A description of the project goals, process, and results.

---

## Table of Content
- <b>[Overview](https://github.com/Naidanzheng/DATA-602-Project-1/blob/main/README.md#overview) 
- <b>[Goals](https://github.com/Naidanzheng/DATA-602-Project-1/blob/main/README.md#goals) 
- <b>[Motivation & Background](https://github.com/Naidanzheng/DATA-602-Project-1/blob/main/README.md#motivation--background) 
- <b>[Data](https://github.com/Naidanzheng/DATA-602-Project-1/blob/main/README.md#data) 
- <b>[Software Requirements](https://github.com/Naidanzheng/DATA-602-Project-1/blob/main/README.md#software-requirements) 


---
## Overview
The Global Health Observatory (GHO) data repository under the World Health Organization (WHO) keeps track of the health status as well as many other related factors for all countries. This objects of this project are to determine the critical factors which are more representative, build regression models, and choose the best model to predict life expectancy accurately.
![life.png](https://github.com/Naidanzheng/DATA-602-Project-1/blob/main/life.png)



## Goals
The first goal for this project is to search for the elements which effects life expectancy by using statistical tools such as MSE, R squared, RMSE, ect. on different regression models.

The second goal for this project is to find the best model to predict life expectancy by using regression.


## Motivation & Background
Life expectancy is an educated prediction of human life. Through the comparative analysis of life expectancy, it can reflect the quality of life of a society and measure the health level of people in this country (or region). Everyone wants to have a longer life expectancy, and it can be affected by a lot of factors. Life expectancy is not only one of the important indicators to measure the health of the population, but also a comprehensive indicator to measure the level of economic and social development of a country or region. In population quality evaluation and prediction, disease burden measurement, and national economy and residents’ quality of life evaluation, life expectancy and other indicators are among the most basic research content


## Data
This dataset is comprised of data from all over the world from various countries aggregated by the World Health Organization. The data is an aggregate of many indicators for a particular country in a particular year. In essence, the data is multiple indicators in a time series separated by country. 

The dataset has 22 Columns and 2938 rows which meant 20 predicting variables. All predicting variables were then divided into several broad categories: Immunization related factors, Mortality factors, Economical factors, and Social factors. 

This graph shows the different life expectancy in developed and developing countries. The average life expectancy of developed countries is 78.69 years, the average life expectacy of developing countries is 67.69 years. There is a large difference of min life expectancy between developed(69.9 years) and developing(44 years) countries. It may be because developing countries have better infrastructure, healthcare, welfare than developing countries.

![Status1.png](https://github.com/Naidanzheng/DATA-602-Project-1/blob/main/Status1.png)

![Status.png](https://github.com/Naidanzheng/DATA-602-Project-1/blob/Image/Status.png)

This graph shows the correlation between features. These variables will be used to create models to predict life expectancy.
![Correlation.png](https://github.com/Naidanzheng/DATA-602-Project-1/blob/Image/Correlation.png)

There is a strong correlation relationship between 'Schooling' and 'Life Expectancy' of 0.728. This may be because education is more established and prevalent in wealthier countries.

Surprisingly, there is a moderate positive correlation between ‘Alcohol’ and ‘Life Expectancy’ of 0.40, it may be because only wealthier countries can afford alcohol or the consumption of alcohol is more prevalent among wealthier populations.


## Modeling 

## Software Requirements
python 3.9.0

Packages used: numPy,pandas, matplotlib, seaborn, scipy.stats, scikit-learn,warning
