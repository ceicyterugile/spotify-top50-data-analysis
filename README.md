# Spotify Top 50 Tracks: Exploratory Data Analysis & Product Metrics

## Project Context & Strategic Business Goal
In this project, I act as an internal Data Analyst within the Spotify Content Analysis team. The objective is to evaluate the global **Top 50 Spotify Tracks dataset** to programmatically discover, clean, and quantify what specific audio characteristics and artist parameters drive a mainstream hit song. 

The analytical pipeline is designed to balance technical data engineering with high-level business storytelling, translating raw audio variables into actionable product intelligence for Product Managers and Senior Data Scientists.

## Core Requirements & Technical Objectives
- **Data Ingestion:** Sourced raw streaming configurations from Kaggle and programmatically mapped them into memory using **Pandas DataFrame architectures**.
- **Data Cleansing & Integrity Audits:** 
  - Isolated and treated missing data fields.
  - Audited and stripped duplicate records, samples, and overlapping features.
  - Checked for and handled statistical outliers to ensure clean downstream modeling.
- **Exploratory Data Analysis (EDA):** Applied vectorized matrix filters and aggregations to answer explicit product questions across three distinct analytical pillars:

### 1. Structural Dataset & Feature Profiling
* Programmatically measured baseline observation volumes and total feature dimensions.
* Separated categorical metadata labels from raw numeric data arrays.
* Quantified market fragmentation by tracking total unique artists, albums, and genre counts (identifying 16 distinct genres in total).

### 2. Behavioral & Content Metrics Querying
* **Artist & Album Market Share:** Identified overlapping hit tracks to reveal key creator dominance (e.g., multi-track presence by Dua Lipa, Billie Eilish, and Travis Scott).
* **Audio Matrix Segmentation:** Filtered exact tracking parameters based on critical business thresholds:
  * *Danceability Constraints:* Isolated track volumes tracking above `0.7` and below `0.4`.
  * *Loudness Boundaries:* Audited decibel scales filtering positions above `-5dB` and below `-8dB`.
  * *Chronological Extremes:* Programmatically calculated the absolute shortest and longest tracks on the global charts.
* **Niche Variable Isolation:** Extracted hyper-specific market entries, including code scripts designed to identify genres with only a single track representation:
  ```python
  genre_counts = df['genre'].value_counts()
  genres_with_one_song = genre_counts[genre_counts == 1].index.tolist()
  ```

### 3. Cross-Genre Statistical Profiling
* Conducted granular behavioral comparisons evaluating **Danceability, Loudness, and Acousticness** distribution variations across core competitive genres: *Pop, Hip-Hop/Rap, Dance/Electronic, and Alternative/Indie*.
* Measured multi-variable correlation coefficients to isolate strong positive, strong negative, and linear feature relationships.


##  Analytical Refinements & Future Improvements
1. **Feature Engineering:** Integrating external streaming metrics (e.g., active user skip rates and regional location tags) to expand the depth of behavior mapping.
2. **Advanced Modeling:** Transitioning from linear correlation tests to non-linear clustering (e.g., K-Means) to categorize distinct "hit blueprints" based on audio properties.

https://colab.research.google.com/drive/1Qv5NimrX1CcZBPX4NDhoYHjl92frfqDa#scrollTo=GhEVAhBPMdY6

