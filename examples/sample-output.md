# Sample output: one trade, step by step

> **Illustrative example.** This walkthrough uses **TESTCO**, a made-up company in the product's test data. Prices, times and results are synthetic and only show the *kind* of answer you get at each step. They are not real market data, not a trade record and not investment advice. For real output, see the [screenshots in the README](../README.md#see-it-in-action).

In each step you ask in plain words. Claude runs the matching skill and explains the result.

---

### 1. "Any breakouts?" (after 9:30)

```
Mon 02 Nov 2026 09:41 IST: 1 of 2 stocks have closed a 5-minute bar beyond their 15-minute opening range (0 fetch errors).
Still above their range now: 1. Fell back inside (breakout failed): 0.
symbol        side      OR low   OR high  trigger trig close  beyond%      last  rvol   day%  status
TESTCO        long     1704.78   1707.31    09:35    1707.63     0.02   1718.72  0.98   0.60  holding
```

The opening range is the high and low from 9:15 to 9:30. **holding** means the stock is still beyond that range. If a breakout has failed, the stock is marked as back inside its range, so you can skip it.

### 2. "Is it time to buy TESTCO?"

```
TESTCO long ORB @ 09:41: TRIGGERED - first 5-minute close above the range at 09:35
  range 1704.78 - 1707.31, last 1718.72 (09:35 bar)
  trigger close 1707.63 at 09:35
```

The answer is always one of **waiting**, **triggered** or **expired**. *Expired* means the price has already run too far, and Claude tells you not to chase it.

### 3. "Plan the stop and target."

```
TESTCO LONG plan
  entry     1718.72
  stop      1704.70  (or-low, 14.02/share at risk)
  target    1753.70  (2.5R, 34.98/share)
  flat by 15:10 IST either way
  reward:risk 2.5 gross, 2.09 after ~1.83/share charges
```

### 4. "What are the odds?"

```
Time Machine: TESTCO long from 1718.72 (stop 1704.7, target 1753.7, flat by 15:10)
  10,000 replays of the remaining 67 candles, drawn from 59 past sessions (seed 42):
    today is moving at 0.68x its normal pace for this time of day; replayed candles are scaled to match
    target first 7.5%, stop first 11.1%, still open at flat-by 81.4%
    average result +8.84/share after ~1.83/share charges = +0.63R
  History: the same rule fired on 54 of 59 past sessions: 19 target, 26 stop, 9 neither; average +0.27R net
  Verdict: positive on paper, but 60 sessions is a small sample and the future need not repeat them.
```

If the verdict is negative after charges, it says "skip it". Skipping is a perfectly good result.

### 5. "How many shares?" (₹1,00,000 capital, ₹500 maximum loss)

```
Buy 28 TESTCO MIS LIMIT at 1720.5 = ₹48,174.00 (margin ₹48,174.00)
  stop 1704.7: lose about ₹493.32
  target 1753.7: make about ₹877.80 after ₹51.80 charges
  net reward:risk 1.78; flat by 15:10
```

### 6. "Is this trade allowed?"

```
TESTCO-20261102-0941: PASS
  [  ok  ] max loss per trade: ₹493.32 at the stop vs limit ₹500.00
  [  ok  ] daily loss limit: worst case -₹493.32 vs limit -₹1,500.00
  [  ok  ] trades per day: 0 taken today, max 3
  [  ok  ] reward to risk (net): 1.78 vs minimum 1.5
  [  ok  ] entry window: now 09:41, window 09:30-14:30
  [  ok  ] SEBI insider guard: not on your insider list
  [  ok  ] market open today: trading day
  [  ok  ] circuit band: 20.0% band; minimum 10%
  ... and the other checks
```

The limits shown are **your** settings. If any check fails, the answer is **BLOCK** with the reason, and the order cannot go any further.

### 7. "Place it."

Claude shows you the order in plain words and waits. On paper (the default), it records the trade in a practice ledger. A real order needs paper trading switched off and your yes for that exact order.

### 8. "What did it cost?"

```
Buy 28 at 1718.72, sell at 1753.7 (discount brokerage):
  Brokerage                   ₹29.17
  STT (0.025% sell)           ₹12.28
  NSE transaction              ₹2.89
  Stamp duty (buy)             ₹1.44
  GST 18%                      ₹5.81
  Total charges               ₹51.78
  Gross P&L                  ₹979.44
  Net P&L                    ₹927.66
```

### 9. "How am I doing?"

After a few weeks of trades, the journal shows your win rate, average win and loss in rupees, charges paid, your worst losing streak, and whether your record is good enough to consider real money.
