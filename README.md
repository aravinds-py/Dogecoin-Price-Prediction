# 🐕 Dogecoin Price Prediction with Machine Learning 🚀

Welcome to the **Dogecoin Price Prediction** project! This repository demonstrates how to build, train, and evaluate a machine learning model for forecasting Dogecoin (DOGE) prices using historical market data and modern data science tools.

## 📚 Project Overview

- **Goal:** Predict closing prices of Dogecoin using historical price & volume data, custom feature engineering, and machine learning models "Random Forest".
- **Main File:** [`Dogecoin.ipynb`](./Dogecoin.ipynb)  
  A well-commented and modular Jupyter Notebook guiding you through the entire workflow, from data loading to model evaluation and visualization.

## 🗂️ Repository Structure

```
├── Dogecoin.ipynb     # Main notebook with code, charts, and explanations
├── README.md          # You are here!
├── DOGE-USD.csv       # Historical Dogecoin data (get from Yahoo or attach yourself)
```

## 📦 Requirements

- Python 3.7+
- Jupyter Notebook / JupyterLab
- `pandas`, `numpy`, `matplotlib`, `scikit-learn`, `statsmodels`
- For interactive plots: `seaborn` (optional)

**Install requirements:**
```bash
pip install pandas numpy matplotlib scikit-learn statsmodels seaborn
```

## 🚦 How to Run

1. **Clone the repository**
   ```bash
   git clone https://github.com/aravinds-py/dogecoin-price-prediction.git
   cd dogecoin-price-prediction
   ```

2. **Ensure the dataset file is present**
   - Make sure you have `DOGE-USD.csv` (can be downloaded from Yahoo Finance: [Official Page](https://finance.yahoo.com/quote/DOGE-USD/history)).

3. **Launch Jupyter Notebook**
   ```bash
   jupyter notebook
   ```
   - Or open the notebook in Colab for a cloud experience.

4. **Open `Dogecoin.ipynb`**
   - Follow along cell-by-cell for explanations & outputs.

## 🔍 Workflow Breakdown

### 1. 📥 Data Loading & Cleaning
- Read historical prices for DOGE-USD (`DOGE-USD.csv`).
- Parse the Date column, remove missing data.

### 2. 🧑‍🔬 Feature Engineering
- Add market-derived features (`gap`, `a`, `b`) to help model volatility and trend.
  - `gap` = (High - Low) × Volume
  - `a` = High / Low
  - `b` = (High / Low) × Volume

### 3. 📊 Exploratory Data Analysis
- Visualize daily close prices and feature relationships.
- Summary statistics and charts for trends and volatility.

### 4. 🔀 Train/Test Split
- Use the most recent 30 days as a backtest window.
- 11 days for training, 19 days for evaluation (mimicking real-world forecasting).

### 5. 🧠 Model Training
- **Random Forest Regressor**: Train and predict with ensemble trees.

### 6. 📈 Evaluation
- Compute **Mean Absolute Error (MAE)**, **Root Mean Squared Error (RMSE)**, and **R² Score** to assess predictive accuracy.
- Plot predictions vs. true values.
- Example:
  ```
  Mean Absolute Error: 0.00568
  Root Mean Squared Error: 0.00627
  R2 Score: 0.114
  ```

### 7. 📉 Visualization
- Graph actual vs predicted close prices to visually inspect model performance.

## 🧑‍💻 Usage & Customization

- 💡 **Modify feature engineering** to experiment with your own signals!
- 🤖 **Swap out models** with others from scikit-learn (SVR, GradientBoosting, etc).
- 🔗 **Integrate with live feeds** for ongoing market predictions.

## 📝 Notes

- Data source: Yahoo Finance, [DOGE-USD](https://finance.yahoo.com/quote/DOGE-USD/history)
- **Accuracy is limited** by the small recent-window split; more robust models will require more data and careful validation.
- **No investment advice** — this is for educational/data science purposes!

## 🤝 Contributing

Pull requests welcome! Open an [issue](https://github.com/aravinds-py/dogecoin-price-prediction-ml/issues) for ideas or improvements.

---

**Made with ❤️ by [aravinds-py](https://github.com/aravinds-py)**

```
🐕📈🚀
```