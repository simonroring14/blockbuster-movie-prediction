# What Makes a Movie a Blockbuster? — 5,000 Films with Ratings, Budgets & Revenue

**Created by:** [Vedauv Rajkumar Leelavathi](https://www.kaggle.com/vedauv)

## What is this?

A synthetic movie dataset with 5,000 films spanning 1980–2024. Includes budget, revenue, ratings, genre, and a clear target variable: **blockbuster**.

## Why should you use it?

- **Clean, complete data** — no missing values, no messy joins
- **Defined target** — `blockbuster` (revenue > 3× budget AND > $100M)
- **Realistic distributions** — budget and revenue follow lognormal patterns with genre-specific effects
- **Multiple tasks** — classification (blockbuster), regression (revenue, ROI)
- **Broad appeal** — everyone understands movies

## Columns

| Column | Description |
|--------|-------------|
| `movie_id` | Unique identifier |
| `title` | Synthetic movie title (placeholder) |
| `year` | Release year (1980–2024) |
| `decade` | Decade label (1980s, 1990s, etc.) |
| `genre` | Primary genre |
| `runtime_min` | Runtime in minutes |
| `budget_usd` | Production budget (USD) |
| `revenue_usd` | Box office revenue (USD) |
| `profit_usd` | Revenue minus budget (USD) |
| `roi` | Return on investment |
| `rating` | Average rating (0–10) |
| `vote_count` | Number of votes |
| `popularity` | Popularity score |
| `blockbuster` | **Target:** 1 if hit, 0 otherwise |

## Suggested Tasks

- **Classification:** Predict `blockbuster` from budget, genre, rating, runtime
- **Regression:** Predict `revenue_usd` or `roi`
- **Analysis:** Which genres have the highest blockbuster rate?
- **Feature engineering:** Create budget-to-rating ratios, genre interactions

## Quick Start

```python
import pandas as pd

df = pd.read_csv("movie_blockbusters.csv")
print(df.shape)
print(df.head())
print(f"Blockbuster rate: {df['blockbuster'].mean()*100:.1f}%")
```
 ## License
 CC0 Public Domain