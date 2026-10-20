# Datasheet: What Makes a Movie a Blockbuster? — 5,000 Films

## Motivation

**What is this dataset for?**
A synthetic movie dataset with budget, revenue, ratings, and derived features for predicting blockbuster success. Designed for regression (predicting revenue/ROI) and classification (predicting blockbuster status).

**Who created it and why?**
Created by Vedauv Rajkumar Leelavathi. Real movie datasets often have missing financial data and inconsistent coverage. This synthetic dataset provides a clean, fully-populated benchmark with known generation parameters.

## Composition

**What do the instances represent?**
Each instance is a synthetic movie with financial, rating, and metadata attributes.

**How many instances?**
5,000 movies, spanning years 1980–2024.

**What data does each instance consist of?**
- **Identifiers:** movie_id, title, year, decade
- **Categorical:** genre
- **Numerical:** runtime_min, budget_usd, revenue_usd, profit_usd, roi, rating, vote_count, popularity
- **Target:** blockbuster (1 if revenue > 3× budget AND revenue > $100M, else 0)

**Is there a label or target?**
Yes. `blockbuster` is the binary classification target. `revenue_usd` and `roi` serve as regression targets.

**Are there recommended data splits?**
Split by `movie_id`. All rows are independent.

## Collection Process

**How was the data created?**
Synthetically generated via Python using lognormal distributions for budget and revenue, with genre-specific multipliers to reflect real box office patterns. Ratings and vote counts are generated independently. No real movie data was used.

## Preprocessing

Data is generated in final format with derived features pre-computed.

## Uses

- Binary classification: predict blockbuster success
- Regression: predict revenue or ROI from budget and metadata
- Exploratory analysis: genre trends over decades
- Teaching: feature engineering, class imbalance handling

**Should NOT be used for:**
- Real-world box office prediction 
- Any commercial application involving real film data

## Distribution

**License:** CC0 Public Domain

## Maintenance

**Maintainer:** Vedauv Rajkumar Leelavathi
**Contact:** https://www.kaggle.com/vedauv