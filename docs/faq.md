# FAQ

### Who is this for?
People who day-trade, or want to learn to day-trade, stocks on India's NSE, and who want a consistent routine and honest numbers. It suits beginners practising with paper trading and experienced traders who want a faster pre-market and pre-trade checklist.

### Does it tell me what to buy?
No. It shows market context, setups that match fixed rules, news, levels, costs and your own risk limits. A regime label or a scanner hit describes the backdrop. It is not a recommendation. You make every decision.

### Is this investment advice?
No. It is software that reads public data and does arithmetic on rules you choose. It is not a SEBI-registered investment adviser or research analyst.

### Will it place trades on its own?
No. Orders go to a paper (pretend-money) ledger by default. A real order needs three things: paper trading switched off, a fresh risk-check PASS, and your explicit yes for that exact order.

### Which brokers does it work with?
Angel One, Dhan, Zerodha, Upstox, FYERS and Groww, plus about 40 more through OpenAlgo. So far, login and read-only checks are verified on real Angel One and Dhan accounts. Placing real orders, and the other brokers, have not been tested yet. Treat them as beta.

### Do I need a broker account to use it?
No. Market pulse, scanner, levels, news, sentiment, charges, sizing, risk checks, paper trading and the journal all work without connecting a broker.

### What do I need to run it?
Claude Code or the Code tab of the Claude desktop app, running on your own computer, with Python 3 installed. Claude Code needs a paid Claude plan. It has been checked on a Mac. Windows has not been tested yet.

### Does it work in Claude's web chat?
It is not recommended. Claude's cloud blocks the market-data sites unless you allow them, and NSE may still refuse requests that come from the cloud.

### Does it work with ChatGPT or Codex?
Not tested.

### Can I ask in Hindi or Hinglish?
Yes. For example, *"aaj market kaisa hai?"*

### Where does the data come from? Is it real time?
Free public sources: Yahoo Finance, NSE's website and published files, Nifty Indices, Google News India and Reddit. They are unofficial and can be late, change or be blocked. Check anything important in your broker's app. If a source is down, the output says so.

### How accurate are the charges?
Brokerage and statutory charges (STT, exchange fees, SEBI fee, stamp duty and GST) use rates as of 3 Nov 2026. Rates change, so compare against one of your real contract notes.

### What does the "Time Machine" odds check actually promise?
Nothing. It is a simulation built from the stock's own recent price action and from how the same rule did on past sessions. A small sample, results days, circuits or big news can make the future very different.

### Can a stop-loss fail?
Yes. In a fast market or a circuit, a stop can fill far from your price, or not at all.

### What about insider trading rules?
You can list any company where you are an insider in your settings. The risk check will then always block trades in it.

### Do I need a static IP?
Under SEBI rules, brokers may accept API orders only from an internet address (IP) you have registered with them. Viewing your account works without one.

### How are updates delivered?
Updates are delivered through Agensi. See the [changelog](../CHANGELOG.md) for public release notes.

### How do I get support?
[Support contact, added after publication]

### Can I get the code from this repository?
No. This repository is only a showcase. The product is available through the Agensi listing: [Agensi listing URL, added after publication].
