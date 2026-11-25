# Baccarat Simulator

**Live:** https://geniuneajay.github.io/baccarat-simulator/

A browser-based Baccarat (Punto Banco) simulator. Enter how many sessions to play; each session is 70 hands, always betting on **Banker**, with a per-hand bet progression carried from one session to the next.

> Virtual simulation only. Every run is random. It shows what happens under real Baccarat rules and cannot predict a real game.

## Features

- Real 8-deck Punto Banco rules: natural 8/9, Player draws on 0–5, full Banker third-card table
- Fresh shuffle every session using `crypto.getRandomValues` (unbiased Fisher–Yates)
- Bet progression per hand number: lose → +₹50,000, win → −₹50,000 (min ₹50,000), tie → same bet; step becomes ₹1,00,000 above ₹5,00,000
- Overall summary with animated counters and sound (can be muted)
- Session summary, bet line chart and hand-by-hand chart, with pagination for large runs
- Accuracy panel: compares the run's Banker / Player / Tie % with real-world odds, with a 95% range and a chi-square check
- P/L graph after each session

## Important

Banker wins are paid **1:1 with no commission** in this version. Real casinos take **5% commission** on Banker wins, which turns the Banker bet from a small player edge into a **1.06% house edge**. Results here are therefore more favourable than a real table.

## Run it

Open `index.html` in any modern browser. No build step or server needed.

## Files

| File | Purpose |
|---|---|
| `index.html` | Page layout |
| `style.css` | Styles, mobile responsive |
| `game.js` | Shoe, Baccarat rules, bet lines, rendering, counters, sound |
