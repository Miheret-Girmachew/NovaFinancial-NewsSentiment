# B5W1: Predicting Price Moves with News Sentiment

This repository contains the full analysis for the "Predicting Price Moves with News Sentiment" project, completed for Nova Financial Solutions. The project explores the relationship between financial news headlines and stock market movements.

## Project Overview

The primary objective of this project was to enhance Nova Financial Solutions' predictive analytics capabilities by analyzing a large corpus of financial news. The analysis focused on two main areas:

1.  **Sentiment Analysis:** Quantifying the sentiment of news headlines using Natural Language Processing (NLP).
2.  **Correlation Analysis:** Measuring the statistical correlation between the derived news sentiment and daily stock price returns.

The ultimate goal was to develop data-driven, actionable insights for investment strategies.

## Key Finding: "Buy the Rumor, Sell the News"

Our analysis uncovered a fascinating and counter-intuitive insight for high-growth tech stocks like **NVIDIA (NVDA)**.

> **We found a moderate negative correlation of -0.4377 between the average daily news sentiment and the stock's same-day returns.**

This suggests a classic "sell the news" phenomenon, where a surge in positive news may indicate a peak in price, providing an opportunity for early investors to take profits. This finding forms the basis of a proposed contrarian trading indicator for Nova Financial Solutions.

## Tech Stack & Libraries

- **Python 3.10**
- **JupyterLab** for interactive analysis
- **Pandas & NumPy** for data manipulation
- **Matplotlib & Seaborn** for data visualization
- **Scikit-learn** for text feature extraction
- **TA-Lib** for calculating technical indicators (SMA, RSI, MACD)
- **TextBlob** for sentiment analysis

## Project Structure

```
├── .gitignore
├── README.md
├── requirements.txt
├── data/ # Data (not in repo), see setup instructions
├── notebooks/
│   ├── 01_EDA.ipynb
│   ├── 02_Technical_Analysis.ipynb
│   └── 03_Correlation_Analysis.ipynb
└── ... (other project folders)
```

## Setup and Usage

To replicate this analysis, please follow these steps:

**1. Clone the Repository**

```bash
git clone https://github.com/Miheret-Girmachew/NovaFinancial-NewsSentiment.git
cd NovaFinancial-NewsSentiment
```

**2. Create and Activate a Virtual Environment**

```bash
# Create the environment
python -m venv .venv

# Activate the environment
# On Windows:
.venv\Scripts\activate
# On macOS/Linux:
source .venv/bin/activate
```

**3. Install Dependencies**

All required packages are listed in requirements.txt. Install them using:

```bash
python -m pip install -r requirements.txt
```

Note: TA-Lib may require special installation steps depending on your OS. Refer to the project documentation for details.

**4. Place Data**

This repository does not include the raw data files.

- Create a folder named `data` in the root of the project.
- Place the `raw_analyst_ratings.csv.zip` and `yfinance_data.zip` files inside this `data/` folder.

**5. Run the Analysis**

You can now run the Jupyter notebooks located in the `notebooks/` directory. It is recommended to run them in order:

- 01_EDA.ipynb
- 02_Technical_Analysis.ipynb
- 03_Correlation_Analysis.ipynb

## Future Work

- **Lag Analysis:** Investigate the correlation between today's news and tomorrow's returns.
- **Expand Stock Universe:** Apply the analysis to a broader range of stocks to test the generalizability of the findings.
- **Advanced NLP:** Utilize finance-specific sentiment models like FinBERT for a more nuanced analysis.
