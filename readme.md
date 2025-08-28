# Aspiration.AI - Financial Data Science Internship Project

## Overview

This repository contains my comprehensive work during the Aspiration.AI Machine Learning Internship, where I developed and implemented various data science and machine learning techniques for financial market analysis. The project demonstrates proficiency in data processing, statistical analysis, machine learning algorithms, and portfolio optimization techniques applied to real-world financial data.

**Internship Link:** [Aspiration.AI Machine Learning Internship](http://www.aspiration.ai/machine-learning/internship/)

## Project Background

The financial industry has undergone a significant transformation with the integration of data science and machine learning. This project addresses the growing need for quantitative analysis in investment banking, portfolio management, and trading by implementing various analytical techniques on real market data.

The project encompasses six comprehensive modules, each focusing on different aspects of financial data science:

## Data Sources

The analysis utilizes real market data from Indian stock exchanges, including:
- **Large Cap Stocks**: TCS, Reliance, HDFC Bank, Infosys, ITC, and others
- **Mid Cap Stocks**: Various mid-capitalization companies
- **Small Cap Stocks**: Small-capitalization companies
- **Commodities**: Gold futures data (MCX)
- **Market Indices**: Nifty 50 index data

## Module 1: CSV Data Pipeline and Statistical Analysis

### Problem Statement
Develop a comprehensive data processing pipeline for financial time series data with statistical calculations and feature engineering.

### Implementation
- **Data Import and Cleaning**: Imported CSV files using pandas, filtered for equity series ('EQ'), and handled missing values
- **Date Processing**: Converted date columns to datetime64 format for time-series analysis
- **Statistical Calculations**: 
  - Maximum, minimum, and mean prices for rolling periods (90 days)
  - VWAP (Volume Weighted Average Price) calculations by month
  - Daily percentage change calculations using pandas pct_change()
- **Feature Engineering**: 
  - Created trend classification based on daily percentage changes
  - Implemented functions for average price and profit/loss calculations over various time periods
- **Data Export**: Generated processed datasets for subsequent analysis

### Key Results
- Successfully processed TCS stock data with 500+ trading days
- Implemented VWAP calculations showing volume-price relationships
- Created trend classification system with 8 categories (Slight, Positive, Negative, etc.)
- Analyzed volume patterns by trend: "Among top gainers" showed highest average volume (4.7M shares)
- Generated week2.csv with enhanced features for subsequent analysis

## Module 2: Data Visualization and Technical Analysis

### Problem Statement
Create comprehensive visualizations and implement technical indicators for market analysis and trading signals.

### Implementation
- **Price Charts**: Line plots of closing prices over time with trend analysis
- **Volume Analysis**: Stem plots of daily percentage changes and volume relationships
- **Trend Distribution**: Pie charts and bar plots showing frequency of different market trends
- **Correlation Analysis**: Correlation matrices for multiple stocks using seaborn
- **Technical Indicators**:
  - Rolling volatility calculations (7-day windows)
  - Beta calculations against market indices
  - Simple Moving Averages (21-day and 34-day)
  - Bollinger Bands with 14-day periods and 2 standard deviations
- **Trading Signals**: Implemented buy/sell signals based on moving average crossovers

### Key Results
- Identified significant market events: TCS ex-bonus date (May 31, 2018) with -8.5% drop
- Created comprehensive visualizations: price charts, stem plots, pie charts, correlation matrices
- Analyzed 5 large-cap stocks (ADANIPORTS, ASIANPAINT, AXISBANK, BAJFINANCE, BPCL) correlation patterns
- Implemented 7-day rolling volatility calculations with market comparison
- Generated trading signals using 21-day and 34-day moving average crossovers
- Built Bollinger Bands with 14-day periods and 2 standard deviations for technical analysis

## Module 3: Fundamental Analysis using Linear Regression

### Problem Statement
Apply regression techniques for fundamental analysis, including Beta calculations and CAPM analysis.

### Implementation
- **Linear Regression Models**: 
  - Fitted linear and polynomial functions to OHLC price data
  - Completed missing values in target columns using trained models
- **Beta Calculations**:
  - Daily Beta calculations using regression approach (OLS)
  - Monthly Beta calculations for different time horizons
  - Comparison with market indices (Nifty 50)
- **CAPM Analysis**: Implemented Capital Asset Pricing Model for risk assessment
- **Model Validation**: Used histograms and distribution plots for prediction accuracy

### Key Results
- Successfully identified linear vs polynomial relationships in gold price data
- Achieved perfect score (1.0) for linear regression on 'Pred' column
- Improved polynomial regression score from ~0.7 to ~0.99 using PolynomialFeatures(2)
- Implemented CAPM analysis and Beta calculations using regression approach
- Completed missing values in target columns using trained models
- Validated predictions using histograms and distribution plots

## Module 4: Trade Call Prediction using Classification

### Problem Statement
Develop classification models for automated trading decisions using various technical indicators.

### Implementation
- **Bollinger Band Classification**:
  - Created trading signals based on price position relative to Bollinger Bands
  - Implemented multi-class classification (Buy, Hold, Short)
  - Trained models using Bollinger Band indicators as features
- **Random Forest Implementation**:
  - Feature engineering: Open-Close, High-Low percentage changes
  - Rolling statistics: 5-day mean and standard deviation of returns
  - Action prediction: Next day price movement (1 for increase, -1 for decrease)
- **Model Comparison**: Evaluated multiple classification algorithms for accuracy
- **Performance Analysis**: Calculated cumulative returns from algorithmic trading

### Key Results
- **Achieved 86.27% accuracy** with Neural Network classifier (MLPClassifier) for Bollinger Band trading signals
- Implemented 10 different classification algorithms with performance comparison
- Created 4-class trading system: Buy, Hold Buy/Liquidate Short, Hold Short/Liquidate Buy, Short
- Successfully applied trained model to TITAN stock data for cross-validation
- Built Random Forest classifier for next-day price movement prediction (1 for increase, -1 for decrease)
- Demonstrated practical application of machine learning in automated trading decisions

## Module 5: Modern Portfolio Theory

### Problem Statement
Implement portfolio optimization techniques using Modern Portfolio Theory principles.

### Implementation
- **Risk-Return Calculations**:
  - Annualized returns and volatility calculations
  - Daily to annual conversion using 252 trading days
- **Portfolio Construction**:
  - Built diversified portfolios with 5 stocks from different sectors
  - Equal weightage (20%) portfolio analysis
  - Covariance matrix calculations for risk assessment
- **Efficient Frontier Analysis**:
  - Scatter plots of returns vs volatility for different weight combinations
  - Sharpe ratio calculations for risk-adjusted returns
  - Identification of optimal portfolios (highest Sharpe ratio, lowest volatility)
- **Monte Carlo Simulation**: Portfolio optimization using random weight combinations

### Key Results
- Built diversified portfolio with 5 stocks from different sectors and market caps
- Calculated portfolio metrics: 8% annualized return with 6% volatility
- Implemented Monte Carlo simulation for portfolio optimization
- Created scatter plots showing risk-return trade-offs with Sharpe ratio coloring
- Identified optimal portfolios: highest Sharpe ratio and lowest volatility combinations
- Demonstrated practical application of Modern Portfolio Theory principles

## Module 6: Clustering for Diversification Analysis

### Problem Statement
Apply unsupervised learning techniques for stock clustering and portfolio diversification.

### Implementation
- **Data Preparation**:
  - Collected closing prices for 30 stocks (10 each from large, mid, and small caps)
  - Calculated annual returns and volatility for clustering features
- **K-Means Clustering**:
  - Implemented K-means algorithm for stock grouping
  - Used Elbow method to determine optimal number of clusters
  - Clustered based on return and volatility characteristics
- **Cluster Analysis**: 
  - Identified stocks belonging to same risk-return clusters
  - Created cluster membership dataframes for portfolio construction

### Key Results
- Created comprehensive dataset with 30 stocks (10 each from Large, Mid, and Small caps)
- Implemented K-means clustering with elbow method analysis
- Identified optimal cluster numbers: 5 clusters (primary elbow) and 9 clusters (secondary elbow)
- Generated 3x3 grid visualization showing clustering results for different cluster numbers
- Created cluster membership dataframes for systematic portfolio construction
- Demonstrated practical application of unsupervised learning for stock diversification

## Technical Skills Demonstrated

### Programming Languages & Libraries
- **Python**: Primary programming language
- **Pandas**: Data manipulation and analysis
- **NumPy**: Numerical computations
- **Matplotlib/Seaborn**: Data visualization
- **Scikit-learn**: Machine learning algorithms
- **Jupyter Notebooks**: Interactive development and documentation

### Machine Learning Techniques
- **Supervised Learning**: Linear Regression, Random Forest, Classification
- **Unsupervised Learning**: K-Means Clustering
- **Feature Engineering**: Technical indicators, rolling statistics
- **Model Validation**: Cross-validation, accuracy metrics

### Financial Analysis
- **Technical Analysis**: Moving averages, Bollinger Bands, volatility
- **Fundamental Analysis**: Beta calculations, CAPM
- **Portfolio Theory**: Risk-return optimization, diversification
- **Trading Strategies**: Algorithmic trading signals

## Key Insights and Conclusions

### Market Analysis Findings
- Identified significant correlations between different stock sectors
- Demonstrated effectiveness of technical indicators for trading decisions
- Showed importance of portfolio diversification in risk management

### Machine Learning Applications
- Successfully applied classification algorithms for automated trading
- Implemented regression techniques for fundamental analysis
- Used clustering for systematic portfolio construction

### Practical Applications
- Developed frameworks for quantitative trading strategies
- Created tools for portfolio optimization and risk assessment
- Demonstrated real-world application of data science in finance

## Project Impact

This project demonstrates comprehensive understanding of:
- Financial data processing and analysis
- Machine learning applications in finance
- Portfolio management and optimization
- Quantitative trading strategies
- Risk assessment and management

The work showcases practical implementation of theoretical concepts in a real-world financial context, making it directly relevant for roles in quantitative finance, data science, and investment analysis.

## Files Structure

```
├── Module1.ipynb          # Data pipeline and statistical analysis
├── Module2.ipynb          # Visualization and technical analysis
├── Module3.ipynb          # Linear regression and fundamental analysis
├── Module4.ipynb          # Classification for trading signals
├── Module5.ipynb          # Modern portfolio theory
├── Module6.ipynb          # Clustering for diversification
├── data/                  # Stock data by market cap
├── data1/                 # Additional market data
├── Module_Descriptions_Queries/  # Detailed problem statements
└── Various CSV files      # Processed datasets and results
```

## Key Visualizations and Results

### Module 1: Data Pipeline
- **Trend Distribution Analysis**: Bar chart showing volume patterns by trend categories
- **VWAP Calculations**: Monthly volume-weighted average price analysis

### Module 2: Technical Analysis
- **Price Charts**: TCS closing price over time with significant events marked
- **Stem Plots**: Daily percentage changes showing market volatility
- **Correlation Matrix**: Heatmap of 5 large-cap stocks correlation patterns
- **Bollinger Bands**: Price action with upper/lower bands and moving averages
- **Volume Analysis**: Dual-axis plot showing price changes vs trading volume

### Module 3: Regression Analysis
- **Linear vs Polynomial Fits**: Comparison plots for gold price predictions
- **Beta Calculations**: Regression plots showing stock vs market relationships
- **Prediction Validation**: Histogram distributions of actual vs predicted values

### Module 4: Classification Results
- **Model Performance Comparison**: Bar chart of 10 classification algorithms accuracy
- **Trading Signal Visualization**: Price chart with Bollinger Bands and predicted calls
- **Cross-Validation Results**: TITAN stock predictions using trained model

### Module 5: Portfolio Optimization
- **Efficient Frontier**: Scatter plot of risk vs return with Sharpe ratio coloring
- **Monte Carlo Results**: Portfolio weight combinations and their performance
- **Optimal Portfolio Markers**: Highlighted points for best Sharpe ratio and lowest volatility

### Module 6: Clustering Analysis
- **Elbow Curve**: Inertia plot for optimal cluster number selection
- **K-Means Results**: 3x3 grid showing clustering for different cluster numbers
- **Cluster Centers**: Scatter plot with cluster centers marked

## Technologies Used

- **Python 3.x**
- **Pandas & NumPy**
- **Matplotlib & Seaborn**
- **Scikit-learn**
- **Jupyter Notebooks**
- **Git for version control**

---

*This project represents a comprehensive application of data science and machine learning techniques to financial market analysis, demonstrating both theoretical understanding and practical implementation skills.*

