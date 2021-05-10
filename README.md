# Assignment3
This  assignment introduces a strategy which is about how to choose a stock with better performance among several stocks in a same sector to invest in. The strategy uses four kinds of estimators, the Sortino Ratio, Maximum Drawdown, Daily Return Volatility and Calmar Ratio, I call it “4R” strategy.

The first “R”, the Sortino ratio, is a measure of the relative performance of an investment portfolio. It is similar to the Sharpe Ratio, but the Sortino Ratio uses the lower standard deviation instead of the total standard deviation to distinguish between unfavorable and favorable fluctuations. Similar to the Sharpe ratio, the higher the ratio, the higher the excess return rate for the fund to bear the same unit of downside risk. The Sortino ratio can be seen as a correction method of the Sharpe ratio when measuring hedge funds/private equity funds.

The second “R”, the Maximum Drawdown rate, refers to the maximum value of the return rate retracement range when the net value of the product reaches the lowest point at any historical point in the selected period. The Maximum Drawdown is used to describe the worst possible situation after buying a product. The Maximum Drawdown is an important risk indicator. For hedge funds and quantitative strategy trading, this indicator is more important than volatility.

The third “R”, the Daily Return Volatility, measures the speed of ups and downs. The smaller this indicator is, the more tidy the daily price return of the asset will be, and there will be no large deviations. So when holding assets with a relatively small daily return volatility, although the rise is slow, it is very stable, and the risk of jumping up and down and being cut leek can also be avoided.

The fourth “R”, the Calmar Ratio is defined as (fund annualized return-risk-free interest rate)/maximum drawdown, it reflects the ratio between excess return and maximum drawdown.

Then we can use the four indicators to help us to choose a stock with the best performance. We can calculate the ratios through Python. The codes is in the file named “MFE5210 Assignment3.ipynb”. I choose three stocks as examples and get the results which is in the file named “results.xlsx”. We can see that the stock with stock code 600519 has the largest Sortino ratio and the smallest Daily Return Volatility, and the Maximum Drawdown rate and the Calmar Ratio are also closed to the best one. Thus we should choose the stock 600519 to invest.

	600519	000858	002304	表现最优	最终选择
sortino ratio	2.506041621	2.300303316	1.244992923	600519	600519
return volatility	0.019287362	0.02383274	0.024531232	600519	
maximum drawdown	-0.255290273	-0.295876887	-0.42942738	002304	
calmar ratio	0.119867683	0.118661184	0.045135907	000858	

Besides, we can also try to construct a “zero loss portfolio”. If we can find a sector that has a negatively correlated yield curve with the selected sector, then when the stock price we selected goes down, the negatively correlated sector will likely go up, thereby driving the overall investment portfolio to avoid losses.
