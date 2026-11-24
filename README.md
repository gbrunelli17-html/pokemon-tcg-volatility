# Pokémon TCG Price Volatility

**Question:** Are new Pokémon TCG sets more volatile than old ones?

When a new set comes out, card prices seem to jump around a lot before they settle down. I want to find out if that's actually true in the data, or if it just feels that way.

## Data

Daily TCGplayer market prices from [TCGCSV](https://tcgcsv.com), a free site that posts TCGplayer's price data every day.

The downloaded data isn't stored in this repo. The code pulls it fresh, so anyone can rerun it.

## Rough plan

1. Pull the full list of Pokémon sets and their release dates
2. Get price data for the cards in each set
3. Clean it up (remove sealed product, fix messy names, handle missing prices)
4. Measure how much prices swing in each set
5. Compare newer sets to older ones
6. Chart the results

## Status

In progress. Step 1 (pulling the set list) is working.

## How to run it

```
python -m venv .venv
.venv\Scripts\activate
pip install -r requirements.txt
python step1.py
```

## Built with

Python, requests, pandas, matplotlib

Built by Gio Brunelli.
