
# RSI Backtester
This program shows how an RSI trading strategy would have performed in the past.
It does not trade real money.

## How to use it

1. Open **index.html** in your web browser.
2. Check the stocks you want to test. Keep **SPY** checked for the comparison.
3. Choose your dates and starting amount of money.
4. Click **Run portfolio backtest** after changing any settings.

The price data is already included. The program works offline.

## The strategy

Your starting money is split equally between the selected assets.
Each part waits in cash until that asset's RSI falls below 35.
RSI measures recent price gains and losses over 14 trading days.

When a buy signal appears, the program buys at the next trading day's opening
price. It buys each asset only once and does not sell during the test.

Each invested part uses **2× daily leverage**. This doubles the asset's daily
percentage change before costs, making both gains and losses larger.
The program subtracts estimated trading and financing costs.

## The settings

- **Starting value:** the money you begin with.
- **Financing cost:** the yearly borrowing-cost assumption.
- **Trading cost:** the estimated cost of each purchase. 10 basis points = 0.1%.
- **In-sample share:** how much history is labeled as the earlier test period.
  The rest is labeled out-of-sample. The portfolio continues across both parts.

## The results

The chart compares your strategy with buying and holding SPY without leverage.
Both start with the same amount of money.

The summary shows growth, yearly growth, volatility, Sharpe ratio, biggest drop,
and the percentage of days with positive returns. Entry cards show when each
asset was bought. You can download the daily results.

## Included history

SPY, AMZN, GOOG, AAPL, and MCD: **January 3, 2011–October 30, 2026**.
These are adjusted Yahoo Finance prices. They do not update automatically.

Past results do not guarantee future results. The leverage model is simplified
and does not simulate broker margin calls.
