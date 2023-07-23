# Predicting Solar Power Generation and finding Anomalies
### Project Overview
This project involved developing and evaluating machine learning models for detecting anomalies in solar photovoltaic (PV) systems using time series data. The goal was to identify the most effective model for accurately detecting abnormalities that could lead to power loss.

### Data
The data was collected from two solar power plants located in India over a period of 34 days at 15-minute intervals. It contained measurements like DC power, AC power, irradiation, ambient temperature, and module temperature.

### Models Compared
The following models were developed and their performance was compared:

* LSTM
* MLP with LSTM Encoder
* CNN-LSTM
* Transformer
  
### Key Results
* The MLP model with LSTM encoder showed the best performance with lowest error and highest R^2 value of 0.9661
  
* It was effective at capturing anomalies on specific dates in the dataset
  
* LSTM, CNN-LSTM, and Transformer also performed decently but had more false positives
  
* The models were evaluated using metrics like MAE, MSE, R^2, accuracy, and confusion matrix
  
### Conclusion
The MLP model with LSTM encoder was most effective for anomaly detection in the PV system data. Future work could explore Gaussian methods and model optimization techniques like grid search.
