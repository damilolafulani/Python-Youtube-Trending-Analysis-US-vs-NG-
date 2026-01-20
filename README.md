# YouTube Trending Analysis (US vs NG)

## Overview

This repository contains a **small research experiment and portfolio project** that analyzes YouTube’s *Most Popular* chart for two regions — **United States (US)** and **Nigeria (NG)** — to explore how trending content, engagement, and user preferences differ across regions.

The goal is not to build a production system, but to demonstrate:

* API data collection
* Data cleaning and enrichment
* Structured exploratory analysis
* Clear research framing

This repo is intentionally **lightweight and temporary**, created to support a portfolio link embedded on my personal website.

---

## Research Focus

This experiment explores:

* How YouTube’s trending lists differ by region
* Whether engagement is evenly distributed across trending videos
* What categories dominate attention in each market
* What “trending” practically reflects about consumer behavior

Rather than assuming trending = popularity, the project treats trending as a **distribution and visibility problem**.

---

## Features

* Fetches real‑time *Most Popular* videos by region (US, NG)
* Extracts:

  * Video metadata
  * Engagement metrics (views, likes, comments)
  * Video duration (ISO 8601 → seconds)
  * Category names (via category ID mapping)
* Produces clean, aligned pandas DataFrames for cross‑region comparison

---

## Technologies

* Python 3
* YouTube Data API v3
* pandas
* google-api-python-client
* isodate

---

## Quick Start

### 1. Install dependencies

```bash
pip install pandas google-api-python-client isodate
```

### 2. Set your API key

Create an environment variable:

```bash
export YOUTUBE_API_KEY="your_api_key_here"
```

### 3. Run the notebook

Open and execute:

```
YouTube Trending videos analysis.ipynb
```

---

## Data Collected

For each region, the notebook collects:

* `videoId`
* `title`
* `channel`
* `publishedAt`
* `categoryId`
* `categoryName`
* `viewCount`
* `likeCount`
* `commentCount`
* `duration_seconds`

Two primary DataFrames are produced:

* `df_us` — United States trending videos
* `df_ng` — Nigeria trending videos

---

## Reproducibility Notes

* Results depend on **query time** — trending lists change constantly
* Engagement values are **snapshots**, not final totals
* API quota limits may restrict repeated runs

For consistent comparisons, runs should be timestamped and versioned.

---

## Limitations

* YouTube’s *Most Popular* endpoint returns a curated subset of trending content
* Trending does not imply equal exposure across all listed videos
* Short‑term volatility can distort conclusions

This project is exploratory, not definitive.

---

## Portfolio Context

This repository demonstrates:

* API integration
* Data engineering fundamentals
* Research framing
* Clean, reproducible analysis workflows

It is designed as a **compact portfolio artifact**, not a long‑term maintained codebase.

---

## Author

**Damilola Fulani**
Data analysis & algorithmic behavior research

---

## License

Open for research and educational use. Attribution appreciated.
