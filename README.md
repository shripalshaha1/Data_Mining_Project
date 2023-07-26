# Predicting Solar Power Generation and Anomalies Detection
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

### Results

![Screen Shot 2023-07-26 at 2 20 46 PM](https://github.com/shripalshaha1/Data_Mining_Project/assets/113332807/eed2028c-e2d5-4bf7-8200-f3bff67ef215)

## Anomalies detection by the Models

### Regular LSTM Model

* The regular LSTM model successfully captured some true anomalies on June 7th and June 14th, as seen in the spikes in Figure 1.

* However, the model suffered from a number of false positives, detecting anomalies on several other days incorrectly.

* The confusion matrix in Figure 2 shows the model achieved 46% accuracy in detecting true anomalies out of the 37 known anomalies.

![Anomalies detected by regular LSTM model](https://github.com/shripalshaha1/Data_Mining_Project/assets/113332807/209a0ef5-7cd0-41c4-814c-7caa0bffa4db)

Figure 1: Anomalies detected by regular LSTM model. Spikes on June 7th and 14th (red circles) are true anomalies.

![Screen Shot 2023-07-26 at 2 38 23 PM](https://github.com/shripalshaha1/Data_Mining_Project/assets/113332807/51bd4699-68df-42a9-958a-347a6c35e020)

Figure 2: Confusion matrix for LSTM anomaly detection.

### MLP + LSTM Encoder Model

* The MLP model with LSTM encoder accurately identified the true anomalies on June 7th and 14th, as highlighted in Figure 3.

* It had far fewer false positives compared to the regular LSTM model.

* The confusion matrix in Figure 4 demonstrates the model achieved 86% accuracy in detecting the true anomalies.

![Anomalies detected by MLP + LSTM encoder model](https://github.com/shripalshaha1/Data_Mining_Project/assets/113332807/dee7cbf4-5ffa-4080-93ff-7046ede56e60)

Figure 3: Anomalies detected by MLP + LSTM encoder model. True anomalies on June 7th and 14th were marked.

![Screen Shot 2023-07-26 at 2 37 45 PM](https://github.com/shripalshaha1/Data_Mining_Project/assets/113332807/e45712c7-8d54-4c7c-8540-3e5d7d8790e3)

Figure 4: Confusion matrix for MLP + LSTM encoder anomaly detection.

### CNN-LSTM Model

* The CNN-LSTM model successfully identified the two true anomaly dates of June 7th and 14th, as seen by the spikes in Figure 5.

* However, it suffered from a number of false positives similar to the regular LSTM model.

* Its confusion matrix in Figure 6 shows an accuracy of 51% in detecting true anomalies.

![Anomalies detected by CNN-LSTM model](https://github.com/shripalshaha1/Data_Mining_Project/assets/113332807/dc782266-cb8a-402f-a00b-a37fc9eb2c04)

Figure 5: Anomalies detected by CNN-LSTM model, with true anomalies marked.

![Screen Shot 2023-07-26 at 2 40 30 PM](https://github.com/shripalshaha1/Data_Mining_Project/assets/113332807/9e25bb0f-5129-49ed-a339-873eea9548dd)

Figure 6: Confusion matrix for CNN-LSTM anomaly detection.

### Transformer Model

* The Transformer model detected the true anomaly dates of June 7th and 14th, as highlighted by the spikes in Figure 7.

* It suffered from a number of false positives across different dates similar to LSTM and CNN-LSTM.

* Its confusion matrix in Figure 8 shows it achieved 49% accuracy in detecting the real anomalies.

![Anomalies detected by Transformer model](https://github.com/shripalshaha1/Data_Mining_Project/assets/113332807/773e21ea-0750-4545-bfe5-e5a13e96b20c)

Figure 7: Anomalies detected by Transformer model, with true anomalies marked.

![Screen Shot 2023-07-26 at 2 41 51 PM](https://github.com/shripalshaha1/Data_Mining_Project/assets/113332807/4c603abb-032e-46be-b48f-efad150b14fd)

Figure 8: Confusion matrix for Transformer anomaly detection.

Overall as stated above, the MLP model with the LSTM encoder demonstrated the best performance in accurately detecting true anomalies with the fewest false positives. The regular LSTM, CNN-LSTM, and Transformer models were able to identify the true anomaly dates but suffered from more false positives.
