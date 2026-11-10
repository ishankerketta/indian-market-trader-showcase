# Product overview

Indian Market Trader turns Claude into a careful assistant for intraday trading on the NSE. It does not predict the market. Its job is the preparation work around a trade, done the same way every time, with the uncertainty stated plainly.

## Value in one line

**Every trade gets the same checks: market context, a reason for the move, a planned exit, the true cost, a position size within your limit, and a check against your own rules. You still make the final call.**

## Design principles

- **Paper first.** Trades go to a pretend-money ledger by default. Real orders are opt-in.
- **Your yes, always.** No real order is sent without your explicit yes for that exact order.
- **Every charge counted.** Reward-to-risk, sizing and journal results are shown *after* Indian trading charges.
- **Honest about uncertainty.** Answers say when a source was unavailable, when a sample is small, or when a score is only a rough first pass.
- **Plain language.** You can ask in English, Hindi or Hinglish. You don't need to learn any commands.

## The four stages of a trading day

### 1. Before the open (by 9:15)
- **Market pulse:** NIFTY, BANK NIFTY, SENSEX and India VIX, plus a trend regime label (risk-on, mixed or risk-off). You also get FII/DII cash flows, sector leaders and laggards, Nifty 500 breadth, whether NSE is open today and the next NSE holiday.
- **Scanner / watchlist:** scans the Nifty 500 for end-of-day setups: 20-day breakouts, 52-week highs, oversold bounces, volume spikes, gaps and narrow-range days. The shortlist becomes your watchlist.
- **News and sentiment:** recent headlines and NSE filings, each tagged by event type (results, order wins, deals, fundraising, regulatory) and by tone. Also news and Reddit buzz compared with the normal level, with a pump-and-dump risk flag.
- **Big-investor activity:** bulk and block deals, and insider trades disclosed under SEBI rules, totalled by stock.

### 2. Picking one trade (after 9:30)
- **Breakouts:** which watchlist stocks have broken out of their opening range, and whether each breakout is still holding.
- **Levels:** the few support and resistance lines that matter, drawn on a chart you can open in your browser.
- **Entry:** for each setup, *waiting*, *triggered* or *expired*. If a stock has already run too far past the trigger, it tells you not to chase it.
- **Exit plan:** stop-loss, target and a flat-by time, with reward-to-risk shown before and after charges.
- **Odds (Time Machine):** replays the rest of the session thousands of times using the stock's own recent price action, and checks how the same rule did on past sessions. You get an estimate of how often the target or the stop is hit first, after charges. If the answer is "skip it", that is a perfectly good result.
- **Charges:** brokerage, STT, exchange fees, SEBI fee, stamp duty and GST, with net P&L and breakeven, compared across brokers.
- **Position size:** how many shares to buy so the loss at your stop stays within your limit, charges included.
- **Risk check:** PASS or BLOCK against your limits and NSE rules. It checks loss per trade, the daily loss limit, the number of trades per day, the minimum reward-to-risk and the entry window. It also checks circuit bands, NSE holidays and your list of companies where you are an insider. It warns you about results days and pump risk.
- **Order:** shown to you in plain words. It goes to the paper ledger, or to your broker if you have switched paper trading off and said yes.

### 3. While the trade is open
- **Alerts:** a one-time alert when the price touches your stop, your target or a level you set, and a reminder at the flat-by time.

### 4. After the close
- **Journal:** win rate, average win and loss in rupees, charges as a share of profit, drawdown, losing streaks, rule breaks, and a readiness check on whether your paper record is good enough to consider real money.

## Expected outcomes

What you can reasonably expect:

- A faster, consistent pre-market routine.
- A complete plan for every trade (entry, stop, target, size, cost) before you commit.
- Fewer impulsive trades, because the risk check blocks trades that break your own rules.
- An honest record of your results after charges.

What you should **not** expect:

- Guaranteed profits, or "buy this" tips. The pack gives you context and arithmetic, not signals.
- Official or real-time exchange data. It uses free public sources that can be late or unavailable.

## Supported brokers

Angel One, Dhan, Zerodha, Upstox, FYERS and Groww, plus around 40 more through [OpenAlgo](https://github.com/marketcalls/openalgo). See [Requirements and compatibility](../README.md#requirements-and-compatibility) for what has been tested.

---

Ready to try it? See [Getting started](getting-started.md).
