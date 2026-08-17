# BDO Duo Terminal
*by Weziliey*

A capital allocation & risk model for Black Desert Online's pri&#8594; duo enhancement gamble — built for players who want to treat their silver like a portfolio, not a slot machine.

## Note

Black Desert Online is an MMORPG where players progress through a variety of systems within the official TOS — grinding, lifeskilling, trading, and enhancing gear among them. This tool is built around one lens on that progression: treating enhancement as a market-arbitrage decision rather than a pure gamble.

Every input the calculator uses — success rates, entry fees, tax, and item prices — comes from publicly known game mechanics and the in-game Central Market's own live pricing. Nothing here touches the game client, automates any in-game action, or involves anything outside normal, TOS-compliant play; it's a read-only analysis of numbers any player can already see for themselves. The "roleplay," if you want to call it that, is simply choosing to make enhancement decisions the way a market participant would — sizing a bet against its expected value and downside risk instead of going off gut feel.

## Why this exists

Enhancing gear in BDO is, structurally, a repeated-bet investment decision: you commit capital, face compounding odds across two stages, and the payout is priced live by the market. Most players size these bets on gut feel or streamer hearsay. This tool applies the same discipline you'd expect from any capital allocation decision — expected value, return on capital at risk, and downside modelling — before you spend a single Black Stone.

This tool turns "which piece should we push next" from a debate into a number.

## What it does

- **Live pricing** — pulls current base and target-enhancement market prices directly from the in-game market API (region-selectable), so numbers are never stale copy-pasted estimates.
- **Breakeven analysis** — computes the true breakeven duo market value after entry fees and the 15% marketplace tax, accounting for the full retry structure (pri failures cost materials with no refund; a duo failure sends you back to square one, fees and all).
- **Expected Value (EV) & Return on Investment (ROI)** — every candidate accessory is scored on expected profit *and* expected return per unit of capital at risk, so you're comparing opportunities on equal footing, not just raw payout size.
- **Priority ranking** — a live-sortable leaderboard of tracked accessories ranked by ROI, so you always know what the best use of your next stack of materials is.
- **Risk simulator** — a Monte Carlo model that runs thousands of simulated "trading days" against your actual daily budget, surfacing the realistic spread of outcomes (median day, 5th/95th percentile, chance of a net-negative day) instead of just the theoretical average. This is the difference between "this bet is +EV" and "this bet is +EV *and* survivable at my budget."

<img width="906" height="917" alt="image" src="https://github.com/user-attachments/assets/fe6a06fe-e853-4bc0-ab20-4abe0ddf2632" />

<img width="583" height="742" alt="image" src="https://github.com/user-attachments/assets/67742afa-c3c8-4dba-9cb8-7dcd9edd4e77" />


## Why it's not just another spreadsheet

Spreadsheets tell you the average outcome. They don't tell you that a positive-EV bet can still bankrupt you on a bad day if your throughput is too low to let the law of large numbers work in your favour. The risk simulator exists to answer the question every business plan has to answer to survive variance and realize profit.*

## Who it's for

- Solo players who want a data-backed answer to "is this upgrade worth it right now?"
- Players interested in standardizing enhancement decisions on a consistent & replicable scale, so capital isn't burned on gut-feel plays.
- Anyone who thinks about their playtime the way they'd think about a portfolio.

## Running it

No install, no build step. It's a single self-contained HTML file — open it in a browser, or host it via GitHub Pages for a shareable link your whole crew can use.

## Data source

Live market prices are pulled from [Arsha.io](https://arsha.io), a public BDO market data API. No credentials, no server, no data leaves your browser except the price lookups themselves.

## Disclaimer

Success rates, fees, and tax are user-configurable inputs based on publicly known game mechanics at the time of writing — always verify against current patch notes before making large decisions. This tool models expected behaviour of a random process; it does not guarantee outcomes.

## License

MIT &#183; &#169; Weziliey &#8212; fork it, adapt it, run it for your own guild's numbers.
