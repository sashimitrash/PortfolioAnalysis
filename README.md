# PortfolioAnalysis

 The initial business idea of this project is to offer the lowest entry point into the world of investing.
 The goal was to find the optimal mix of ETFs, and their accompanied weights, for three types of portfolios: low risk, mid risk, and high risk. 
 
This project was done solely on R.
fPortfolio from the Rmetrics package for was used for portfollio optimization, providing portfolio weights.
PerformanceAnalytics was used for returns calculations.

Methodology used:
1. Identify ETFs
▶ Source for ETFs
▶ Omit ETFs, with justification in appendix
2. Prepare data
▶ Obtain adjusted closing price for each ETF
▶ Obtain proxies for ETFs that do not have data dating back to
our chosen start date
▶ VOO proxied by SPY
▶ DBEM proxied by EEM
▶ VCSH proxied by IGSB
▶ BNDX & BIV proxied by AGG ▶ BCI proxied by DBC
▶ ICLN proxied by PBW
▶ Account for currency differences
▶ Obtain individual ETF returns, Ri , and market returns, Rmkt
▶ Get data of a 60% ACWI, 40% BGA market portfolio
3. Calculate βi foreachETFbyregressingRi,t =α+βiRmkt,t 4. Obtain mean and standard deviation for each ETF
▶ Calculate historical mean and standard deviation
▶ Calculate CAPM mean using E(Ri) = μCAPM = rf +βiE(Rmkt)
▶ Take the risk-free rate to be equivalent to the yield on a 20-year Japanese Government bond, rf = 0.76%
▶ Take the expected market returns to be E(Rmkt) = 5% ▶ Calculate μ using μ = 32 μCAPM + 13 μhist
5. Get portfolio
▶ Get portfolio weights from μ and covariance
▶ Generate efficient frontier using fPortfolio
▶ From the efficient frontier, obtain low, medium, high risk
portfolios
6. Backtest, amend initial portfolio choices.


Data is accurate as as of April 2022.
