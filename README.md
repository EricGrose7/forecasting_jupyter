# Predicting the Future with XGBoost, LSTM, and Prophet
In this project, we explore time series forecasting using various machine learning models like XGBoost, Long Short-Term Memory (LSTM), as well as classical models like Prophet. We will use a dataset containing hourly electricity usage data and try to forecast the future electricity usage based on this data.

**Dataset**   <br>
The dataset we are using is hourly electricity usage data from PJM Interconnection LLC, a regional transmission organization (RTO) in the United States. The data contains hourly electricity usage readings from 1st July 1998 to 31st December 2018. The dataset can be downloaded from the [Kaggle page](https://www.kaggle.com/datasets/robikscube/hourly-energy-consumption).

**Exploratory Data Analysis**   <br>
We begin with a brief exploratory data analysis of the dataset. We visualize the hourly electricity usage data for the first few months in 2017 using a line chart. The chart shows that there is a clear daily pattern in electricity usage with higher usage during the day and lower usage during the night.

**XGBoost Model**   <br>
We first use an XGBoost model to predict future electricity usage. XGBoost is a powerful machine learning algorithm that can be used for time series forecasting. We use the previous 720 hours of electricity usage data to predict the next 24 hours of usage. We use a neural network with two hidden layers followed by a fully connected layer. The model is trained on the first 20 years of data and validated on the last 2 years of data. The model achieves an Mean Absolute Percentage Error (MAPE) of 2.6% on the validation set.

**LSTM Model**   <br>
We first use an LSTM model to predict future electricity usage. We use the previous 720 hours of electricity usage data to predict the next 24 hours of usage. We use a neural network with two LSTM layers followed by a fully connected layer. The model is trained on the first 20 years of data and validated on the last 2 years of data. The model achieves an Mean Absolute Percentage Error (MAPE) of 2.9% on the validation set.

**Prophet Model**   <br>
We then use the Prophet model to predict future electricity usage. Prophet is a classical time series forecasting model developed by Facebook. It is based on an additive model where non-linear trends are fit with yearly, weekly, and daily seasonality, plus holiday effects. We train the Prophet model on the same dataset as the LSTM model and predict the next 24 hours of electricity usage. The model achieves an MAPE of 4.9% on the validation set.


**Conclusion**   <br>
We have shown how to use XGBoost, LSTM, Prophet, and Neural Prophet models to predict future electricity usage. Our results demonstrate that Neural Prophet achieves the best performance with an MAPE of 2.4%. This suggests that using a neural network to model the trend and seasonality components of time series data can lead to better performance than classical models like Prophet.
