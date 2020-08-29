# Forcasting-Covid-Worldwide
Autoregressive models used to forecast Covid data
# Problem Description

With the biggest topic of the century being about COVID-19, the White House Office of Science and Technology Policy (OSTP) pulled together a coalition research groups and companies to prepare the COVID-19 Open Research Dataset (CORD-19) to attempt to address key open scientific questions on COVID-19. Those questions are drawn from National Academies of Sciences, Engineering, and Medicine’s (NASEM) and the World Health Organization (WHO). This project will try to help answer a subset of the NASEM/WHO questions. While the challenge involves forecasting confirmed cases and fatalities between April 1 and April 30 by region, the primary goal isn't only to produce accurate forecasts. It’s also to identify factors that appear to impact the transmission rate of COVID-19. 
The data that will be used here are:

  - Kaggle data set that consists of confirmed cases and fatalities due to COVID-19 across countries and provinces
  - We will additionally use external data sources that consists of factors that might affect the transmission rate such as, starting dates of social lockdowns, population density numbers, air travel connections, density of the people that can afford air travel, temperature etc.
The output of the model will be a prediction of the cumulative number of confirmed COVID19 cases in various locations across the world, as well as the number of resulting fatalities, for future dates. 

# Algorithm

The prediction algorithm that will be used is an auto-regressive model. It generally is used to describe certain time-varying processes in nature, economics, etc. The autoregressive model specifies that the output variable depends linearly on its own previous values and on a stochastic term (an imperfectly predictable term); thus the model is in the form of a stochastic difference equation (or recurrence relation which should not be confused with differential equation).

The way COVID-19 spreads, is from an individual to other people. The number of positive cases yesterday directly affects the number of positive cases today. Since the problem of COVID-19 depends on its own previous values to a great degree, and since this is a time-varying process an auto-regressive linear model is appropriate. 

There is a lot of attention on this topic and people are using various time series methods, RNN(recurring neural networks),  SIR models, random forests and predictive analytics to arrive at a good prediction.


# Results

The results will be the predictions of confirmed cases and fatalities for the month of April, 2020 for 10 different countries (China, Korea, South, Japan, Italy, Iran, Singapore, France, Germany, Spain, US)  along with the root mean square logarithmic error on the train and validation set. 

The results will also have a graphical visualization of the comparison of the predictions and actual curve for each of these countries. There could be other insights from the analysis regarding the factors (that are included from other data sets such as lock-in date, population density etc. that highly impact the transmissions trends

# References:
  - https://www.kaggle.com/c/covid19-global-forecasting-week-2/overview/evaluation
  - https://github.com/CSSEGISandData/COVID-19/blob/master/csse_covid_19_data/csse_covid_19_time_series/.gitignore
