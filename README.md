#  Bitcoin Price Movement Prediction

This project is a machine learning pipeline designed to predict the **next-day price movement of Bitcoin** using historical price data and technical indicators. It covers everything from data preprocessing and visualization to training and evaluating multiple classification models.

---

##  Objective

Predict whether the closing price of Bitcoin will **increase or decrease the next day** using:
- Technical indicators (moving averages, volatility)
- Price-based features (open-close difference, high-low range)
- Date-based features (quarter-end, day, month, etc.)

---

##  Dataset

The dataset used in this project contains historical Bitcoin market data including:
- `Date`, `Open`, `High`, `Low`, `Close`, `Vol.`

Data source: locally stored CSV file (e.g., from investing.com or kaggle).

---

##  Workflow

### 1. Data Cleaning & Preparation
- Converted date column to datetime format
- Handled volume column with "K/M/B" string suffixes
- Sorted data by date for time series integrity

### 2. Feature Engineering
- Calculated moving averages (7, 30, 90 days)
- Created new features like `high-low`, `close-open`, volatility, etc.
- Added time-based features (month, quarter-end, etc.)
- Defined target variable based on next-day price movement

### 3. Data Visualization
- Plotted closing prices and moving averages
- Visualized rolling standard deviation
- Heatmap of feature correlations
- Class distribution for target labels

### 4. Model Training
Trained and evaluated the following models:
- Logistic Regression
- Gradient Boosting Classifier
- Support Vector Classifier (SVC)

### 5. Evaluation Metric
Used **ROC AUC Score** to evaluate how well each model distinguishes between price going up or down.

---

##  Results

- The performance of the models was compared using both training and validation ROC AUC scores.
- Visualization of model performance helped compare generalization capabilities.

While none of the models achieved extremely high accuracy — which is expected in highly volatile financial data — they performed reasonably well and showed promising trends.

---

##  Requirements

This project uses the following Python libraries:
- `numpy`, `pandas`
- `matplotlib`, `seaborn`
- `scikit-learn`

Install all dependencies using:

```bash
pip install -r requirements.txt
```

---

##  Project Structure

```
bitcoin-price-prediction/
├── bitcoin.csv                # Dataset
├── bitcoin_prediction.ipynb  # Jupyter notebook (main script)
├── README.md                  # Project documentation
├── requirements.txt           # Python dependencies
```

---

##  Conclusion

This project highlights how basic technical indicators and simple machine learning models can be used together to gain insights from historical financial data. Although financial time series prediction is inherently uncertain, combining moving averages and volatility with classification models provides a useful starting point for deeper analysis or integration into trading strategies.

---

##  Contact

If you'd like to connect or discuss this project, feel free to reach out:
- Contact me via Email: karimiabolfazl466@gmail.com  
- Telegram: [@Abolfazlk83](https://t.me/Abolfazlk83)  
- LinkedIn: Coming soon  
- GitHub: [github.com/abolfazlkarimi83](https://github.com/abolfazlkarimi83)

---

## 🙏 Acknowledgments

Thanks for reviewing this project.  
This notebook was developed by **Abolfazl Karimi** as part of a self-study journey in machine learning and time series forecasting.
