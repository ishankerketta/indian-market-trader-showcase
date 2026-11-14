# Privacy and security

This page describes how Indian Market Trader handles data, based on how the current beta works. It is not a complete privacy policy. For how your conversations with Claude are handled, see Anthropic's privacy documentation. For purchase and account data, see Agensi's privacy documentation.

## Where it runs

The skills run on **your own computer**, inside Claude Code or the Code tab of the Claude desktop app.

Like anything you do with Claude, your questions and the skills' output become part of your Claude conversation. Anthropic handles that conversation under its own policies.

## What it connects to

To answer market questions, the skills download public information from the internet:

- **Market data:** Yahoo Finance, NSE's website and published files, Nifty Indices
- **News:** Google News India
- **Social sentiment:** Reddit

These requests ask for public market information, such as a stock symbol's prices or headlines. They do not include your broker credentials.

If you connect a broker, the skills also talk to that broker's official API.

## What it saves on your computer

- Your results (market pulse, watchlist, levels charts, plans, the paper ledger and the journal) are saved as files in a `trader` folder inside the project folder you work in.
- Your trading settings (capital, loss limits, broker choice, and any companies where you are an insider) are saved locally so they can be reused.

## Broker logins

- **You log in yourself, in a terminal prompt, not in the chat.** Your password, PIN, one-time code and API secret are typed into that prompt, and nothing appears on screen as you type. They do not pass through Claude.
- **Only the session token is kept.** It is saved with the non-secret ID the broker's API needs, in the `trader` folder, with owner-only file permissions on Mac and Linux. Passwords, PINs, one-time codes and API secrets are not saved.
- **Sessions expire.** Broker tokens usually expire each trading day, so you log in again.
- **Previews hide secrets.** When the pack shows you an order request before sending it, authorization headers and keys are replaced with `***`.
- **Treat the session token like a password.** Don't share your `trader` folder, commit it to a public repository or paste its contents into a chat.

## Orders

- Paper trading (pretend money) is the default.
- A real order needs paper trading switched off, a fresh risk-check PASS, and your explicit yes for that exact order.

## What we do not claim

- We do not claim that "your data never leaves your device". Your Claude conversation, data downloads and broker API calls all involve outside services.
- These security measures have not been independently audited.
