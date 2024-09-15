# Nvidia Stock Price Prediction (Increase/Decrease Prediction)💹
The Stock Prediction Model project aims to predict future stock price movements using machine learning techniques. By analyzing historical stock data, the model determines whether the price of a stock will rise or fall on the following trading day.

This project utilizes the yfinance library to fetch historical stock data and preprocess it to create relevant features. It then applies a Random Forest Classifier, a robust machine learning algorithm, to predict whether the stock price will increase or decrease.
## Project Overview
The objective of this project is to predict whether tomorrow’s Nvidia stock closing price will be higher or lower than today’s closing price. Using historical data, the project generates a binary target variable (1 for increase and 0 for decrease) and applies a Random Forest Classifier to predict this.

## Key Features:
- Target Generation: A new column is created that compares today’s closing price with tomorrow’s, and the result is used as the prediction target.
- Rolling Averages: Various time horizons (e.g., 2, 5, 60, 250, 1000 days) are used to compute rolling averages to enhance the predictive power.
- Backtesting: A custom backtesting function is employed to evaluate model performance over different periods.
## Data
The stock price data for Nvidia is fetched using the yfinance library and includes the following fields:

- Open
- High
- Low
- Close
- Adjusted Close
- Volume

The stock data spans from the earliest available date until today. The notebook processes this data to create the required features for the model.

## Installation

Ensure the following Python libraries are installed before running the project:
```
pip install yfinance
pip install --upgrade yfinance pandas scikit-learn matplotlib
```
Clone the repository and navigate to the project directory:
```
git clone https://github.com/your-username/nvidia-stock-prediction.git
cd nvidia-stock-prediction
```
## Usage
To fetch the latest Nvidia stock data and run the prediction model:

1. Open the Jupyter notebook:
```
jupyter notebook Nvidia-Stk-pred.ipynb
```
2. Run the notebook cells to:
   - Fetch stock data using yfinance.
   - Visualize the stock price.
   - Train a Random Forest Classifier on past data to predict tomorrow's stock price movement.
   - Evaluate the model using precision scores and visualize the results.
## Results
The model's performance is evaluated using the Precision Score, which measures how accurate the predictions are in terms of predicting stock price increases and decreases.

The notebook also shows the distribution of predicted increases and decreases, and further tuning is done by adding rolling averages as predictors to improve the model's accuracy.

## Contributing
If you would like to contribute, feel free to fork the repository and make pull requests!

- Fork the repo (https://github.com/your-username/nvidia-stock-prediction)
- Create your feature branch (git checkout -b feature/NewFeature)
- Commit your changes (git commit -m 'Add new feature')
- Push to the branch (git push origin feature/NewFeature)
- Open a pull request
## License
This project is licensed under the MIT  [LICENSE](LICENSE) .
