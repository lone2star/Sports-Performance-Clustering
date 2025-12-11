# Sports Performance Clustering Engine

A Python tool that automates the analysis of cricket delivery data using Unsupervised Learning (K-Means). It processes raw ball-by-ball logs to group players into performance archetypes based on consistency and scoring rate.

## Tech Stack
* **Python 3.x**
* **Pandas:** For data aggregation and cleaning.
* **Scikit-Learn:** For the K-Means clustering algorithm.
* **Matplotlib:** For generating scatter plots.

## Project Structure
* `Talent_Analyzer.ipynb`: Main notebook containing the class logic and execution steps.
* `deliveries_2008-2024.csv`: Raw dataset (260,000+ rows).
* `sde_project_result.png`: Output visualization.

## Implementation Details
This project moves away from linear scripting to a modular, class-based approach:

1. **Object-Oriented Design:** The `TalentAnalyzer` class encapsulates the data loading, processing, and modeling logic. This makes the pipeline reusable for different datasets (e.g., swapping IPL data for T20 World Cup data).

2. **Data Cleaning Pipeline:** Includes automated handling for common data quality issues, such as stripping hidden whitespace from headers and standardizing legacy column names ('batsman' vs 'batter').

3. **Feature Engineering:** Aggregates raw logs to calculate 'Average Runs' (Consistency) and 'Strike Rate' (Velocity) for every player with over 300 balls faced.

## How to Run
1. Install dependencies:
   ```bash
   pip install pandas matplotlib scikit-learn
## Data Source
Dataset: [IPL Complete Dataset (2008-2024)](https://www.kaggle.com/datasets/patrickb1912/ipl-complete-dataset-20082020) on Kaggle.
Original Source: Data originally sourced from [Cricsheet.org](https://cricsheet.org), managed by the open-source cricket analytics community.
