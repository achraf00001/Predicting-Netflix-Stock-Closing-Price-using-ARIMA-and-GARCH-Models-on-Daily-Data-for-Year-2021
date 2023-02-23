# TIME SERISE/Predicting-Netflix-Stock-Closing-Price-using-ARIMA-and-GARCH-Models-on-Daily-Data-for-Year-2021 

Goal: 

we are looking at Netflix stock data, it has daily stock values for year 2021 with 251 observations. 
We want to fit the best ARIMA and GARCH model for the Netflix data, in order to predict the 
stock closing price. 

Method:

we are going to fit a good Arima model we fit a Garch model.
We first need to transform the data into a time series object. With this we can create a time series 
model, Autocorrelation Function, and Partial Autocorrelation Function to determine the autoregressive 
value (p), difference, and moving average. We will first look at the time series model and see if it is 
stationary or not, if it is stationary, we do not need to use a difference function. With this information
we can create a few different test models and calculate their Akaike Information Criterion correlated 
(AICc), and those with the lowest AICc will fit the data the best. We will also use the Auto ARIMA 
function and to see how its AICc compares to the ones we tested. Finally, we will use the Ljung- Box-lack 
of fit test to calculate the p-value for the model, if it is greater than 0.05 then we can conclude it fits the 
data well.
First, we select the adjusted close price variable, and we change it to a time series object using the ts 
function. Then we plot the time series TS plus ACF and the PACF plots.
