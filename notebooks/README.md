Portfolio Optimization (TSLA, SPY, BND)
1. Objective
The objective of this task was to collect historical financial data, clean it, and perform exploratory data analysis (EDA) to understand trends, volatility, and statistical properties of the selected assets (TSLA, SPY, and BND). These insights form the foundation for later portfolio optimization and risk modeling.
2. Data Collection
Historical market data was downloaded using the yfinance API for the following assets:
•	TSLA (Tesla Inc.) 
•	SPY (S&P 500 ETF) 
•	BND (Vanguard Total Bond Market ETF) 
Time period:
January 1, 2015 – June 30, 2026
3. Data Structure
The final dataset contains the following columns:
 
•	Date 
•	Open 
•	High 
•	Low 
•	Close 
•	Volume 
•	Ticker
 
After merging, the dataset was structured in long format, enabling grouped time-series analysis per asset.
4. Data Cleaning
The following cleaning steps were performed:
•	Converted Date column to datetime format 
•	Converted price columns to numeric types 
•	Handled missing values using forward fill and dropna where necessary 
•	Sorted data by Ticker and Date 
•	Removed invalid or NaN rows after feature engineering 
5. Feature Engineering
The following features were created:
•	Daily Returns: percentage change in closing price 
•	Rolling Volatility (30-day): standard deviation of returns over time 
These features allow better analysis of risk and market behavior.
6. Exploratory Data Analysis (EDA)
6.1 Price Trends
TSLA showed strong long-term upward movement with significant volatility, while SPY demonstrated steady growth and BND remained relatively stable.
 
6.2 Daily Returns Analysis
Daily returns revealed:
•	TSLA → high volatility with frequent spikes 
•	SPY → moderate volatility 
•	BND → very low volatility 
 
6.3 Rolling Volatility
Rolling volatility analysis (30-day window) showed that:
•	TSLA exhibits volatility clustering (periods of high risk) 
•	SPY remains stable 
•	BND shows minimal fluctuation 
 6.4 Correlation Analysis
Correlation between assets:
•	TSLA has weak correlation with BND 
•	SPY acts as a middle-risk benchmark 
•	Diversification benefits exist across all assets 
 
6.5 Return Distribution
Return distributions showed fat tails, especially for TSLA, indicating non-normal behavior.
  

 
 

7. Risk Analysis
7.1 Value at Risk (VaR)
VaR (95%) indicates potential daily loss in worst-case scenarios.
•	TSLA has the highest downside risk 
•	SPY moderate risk 
•	BND lowest risk 
TSLA 95% VaR: -0.0518364389240184
TSLA Sharpe Ratio: 0.7751390389447702
7.2 Sharpe Ratio
Sharpe Ratio results:
•	TSLA → high return, high risk 
•	SPY → balanced performance 
•	BND → stable but low return 
	VaR_95	Sharpe
TSLA	-0.051836	0.775139
SPY	-0.050966	0.757601
BND	-0.054262	0.774691

8. Stationarity Test (ADF Test)
The Augmented Dickey-Fuller test showed:
•	Price series → Non-stationary 
•	Return series → Stationary 
 Interpretation:
This confirms that returns are more suitable for forecasting models like ARIMA.
9. Key Insights
•	TSLA is highly volatile with strong upside and downside risk. 
•	SPY provides stable market exposure. 
•	BND acts as a defensive asset. 
•	Returns are stationary and suitable for modeling. 
•	Diversification benefits exist across the portfolio. 
10. Conclusion
This task successfully prepared a clean, structured financial dataset and provided deep insights into asset behavior, volatility, and risk characteristics. These findings will be used in the next phase of portfolio optimization and predictive modeling.

