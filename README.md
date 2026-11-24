<p align="center"><img src="icon.png" width="120"></p>

<h1 align="center">Pokémon TCG Price Volatility</h1>

<p align="center">Are new Pokémon sets more volatile than old ones? Finding out with real price data.</p>

<p align="center">
  <img src="https://img.shields.io/badge/Python-7C3AED?style=for-the-badge&logo=python&logoColor=white" alt="Python">
  <img src="https://img.shields.io/badge/pandas-7C3AED?style=for-the-badge&logo=pandas&logoColor=white" alt="pandas">
  <img src="https://img.shields.io/badge/matplotlib-7C3AED?style=for-the-badge" alt="matplotlib">
  <img src="https://img.shields.io/badge/status-in%20progress-34D399?style=for-the-badge" alt="status: in progress">
  <a href="https://tcgcsv.com"><img src="https://img.shields.io/badge/data-TCGCSV-34D399?style=for-the-badge" alt="data: TCGCSV"></a>
</p>

## Table of Contents

- [The question](#the-question)
- [Data](#data)
- [How it works](#how-it-works)
- [Progress](#progress)
- [Results](#results)
- [Project structure](#project-structure)
- [How to run it](#how-to-run-it)
- [About me](#about-me)

## The question

**Are new Pokémon TCG sets more volatile than old ones?**

When a new set comes out, card prices seem to jump around a lot before they settle down. I want to find out if that's actually true in the data, or if it just feels that way.

## Data

Daily TCGplayer market prices from [TCGCSV](https://tcgcsv.com), a free site that posts TCGplayer's price data every day.

The downloaded data isn't stored in this repo. The code pulls it fresh, so anyone can rerun it.

## How it works

```mermaid
flowchart LR
    A[Pull set list] --> B[Get prices]
    B --> C[Clean data]
    C --> D[Measure volatility]
    D --> E[Compare new vs old sets]
    E --> F[Chart results]

    classDef step fill:#7C3AED,stroke:#34D399,stroke-width:2px,color:#FFFFFF
    class A,B,C,D,E,F step
    linkStyle default stroke:#34D399,stroke-width:2px
```

## Progress

- [x] Pull the full list of Pokémon sets and their release dates
- [ ] Get price data for the cards in each set
- [ ] Clean it up (remove sealed product, fix messy names, handle missing prices)
- [ ] Measure how much prices swing in each set
- [ ] Compare newer sets to older ones
- [ ] Chart the results

## Results

Results are coming once the analysis is done.

<!-- ![Results chart](results.png) -->

## Project structure

```
pokemon-tcg-volatility/
├── README.md
└── icon.png
```

## How to run it

```
python -m venv .venv
.venv\Scripts\activate
pip install -r requirements.txt
python step1.py
```

Built with Python, requests, pandas, and matplotlib.

## About me

Built by [Gio Brunelli](https://github.com/gbrunelli17-html), a high school senior interested in economics and data science. I'm building this one step at a time to learn how to work with real data.
