# 📈 Stock Price Prediction using TensorFlow and LSTM

## Project Overview

Stock price prediction is a complex and challenging problem in finance, with important applications such as personal investment decision-making and algorithmic trading strategies. This project demonstrates how to build a predictive model for stock prices using **Long Short-Term Memory (LSTM)** networks, a type of recurrent neural network (RNN) well-suited for modeling time series data like stock prices.

Using historical stock data, we develop a deep learning model with TensorFlow to forecast future stock prices, specifically focusing on Apple stock as a case study.

---

## Dataset

The dataset contains daily stock price data over a five-year period for multiple companies, including Apple, Google, Nvidia, and others. Key features include:

- Date of the record
- Open and close prices
- Trading volume
- Company ticker symbol

The dataset was preprocessed to convert date fields to appropriate datetime formats and filtered to extract specific companies for exploratory analysis.

---

## Exploratory Data Analysis (EDA)

Initial analysis focused on visualizing stock price trends and trading volumes over time for a selection of companies, highlighting:

- Variations between opening and closing prices across years
- Trading volume fluctuations
- Seasonal and market trends impacting stock behavior

A detailed examination of Apple’s stock price from 2013 to 2018 was performed to understand historical price movements and prepare data for modeling.

---

## Data Preparation

The Apple stock data was split into training and testing subsets, with approximately 95% of the data used for training the model. The closing prices were scaled to a normalized range to improve the performance of the neural network.

Time series sequences of a fixed window size were created from the scaled training data to serve as input features, with the following day’s price as the target label. This format is ideal for sequential modeling using LSTM networks.

---

## Model Architecture

A deep learning model using stacked LSTM layers was designed to capture temporal dependencies in the stock price data. The model includes:

- Multiple LSTM layers to learn from sequential data and retain information over time
- Dense layers to process learned features
- Dropout layers to prevent overfitting
- A single output neuron for regression to predict the next day’s stock price

The model architecture was summarized and evaluated for suitability.

---

## Model Training and Evaluation

The model was compiled with the Adam optimizer and mean squared error loss function, optimized over multiple epochs. After training, the model’s predictions were generated on the test set.

Model performance was assessed using:

- Mean Squared Error (MSE)
- Root Mean Squared Error (RMSE)

These metrics quantified the average prediction error magnitude and provided insight into the accuracy of the model.

---

## Results and Visualization

Predicted stock prices were plotted alongside actual closing prices to visually assess model performance. The comparison revealed:

- Areas where the model closely tracked actual stock movements
- Periods with noticeable prediction deviations
- Overall trends successfully captured by the model

This visualization helps understand strengths and limitations in forecasting ability.

---

## Conclusion

This project successfully demonstrates the application of LSTM networks for stock price prediction using historical time series data. The approach highlights:

- Effective preprocessing and feature engineering for time series data
- The capability of recurrent neural networks to model sequential dependencies in stock prices
- The importance of model evaluation with appropriate metrics and visualizations

With further refinement, such models can support investment strategies and financial forecasting tasks.

---

## Tools and Libraries

- Python 3
- TensorFlow and Keras for deep learning
- Pandas and NumPy for data manipulation
- Matplotlib and Seaborn for visualization
- Scikit-learn for data preprocessing

---

## References

- Stock data source: [Link to dataset]
- TensorFlow and LSTM documentation
- Financial time series analysis literature

---
