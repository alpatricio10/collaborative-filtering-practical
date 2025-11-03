# Collaborative Filtering Practical

# Overview

This repository implements collaborative filtering algorithms for movie recommendation based on critics' ratings. The project demonstrates how to compute similarity between users using Manhattan, Euclidean, Pearson, and Cosine methods, and how to generate recommendations using weighted scoring schemes.

## Requirements

- Python 3.x environment with Jupyter Notebook installed
- Libraries used:
  - pandas
  - numpy
  - math (built-in)

You can install dependencies via:

pip install pandas numpy jupyter

## Usage

### Running the Notebook

Open and run the cells in the Jupyter Notebook - app.ipynb

Execute the notebook cells in sequence to load data, define similarity functions, calculate neighbors, and generate recommendations.

### Input Data Format

The ratings data is loaded from Excel files containing critics as rows and movies/music as columns, with numeric ratings.

**Example data:**

| Critic       | Lady | Snakes | Luck | Superman | Dupree | Night |
|--------------|-------|---------|-------|----------|---------|-------|
| Lisa Rose    | 2.5   | 3.5     | 3.0   | 3.5      | 2.5     | 3.0   |
| Gene Seymour | 3.0   | 3.5     | 1.5   | 5.0      | 3.0     | 3.5   |

## Data Files

The `data` folder contains several Excel datasets used for collaborative filtering examples and testing:

| File Name                | Description                                                                                  |
|--------------------------|----------------------------------------------------------------------------------------------|
| `movie_critique.xlsx`     | Contains movie ratings by several critics across multiple movies such as Lady, Snakes, Luck, Superman, Dupree, and Night. Each row represents a critic's ratings, with empty cells for unrated movies. Used for movie recommendation examples. |
| `music_critique.xlsx`     | Similar format as `moviecritique.xlsx` but for music critics and artists. Includes ratings for artists like Broken Bells, Phoenix, and Vampire Weekend. Used to test recommendation algorithms on music preference data. |
| `same_recommendation.xlsx`| Dataset constructed so that all similarity measures and recommendation methods yield the same top recommendation for the target reviewer, demonstrating consensus across algorithms. |
| `different_recommendations.xlsx` | Dataset designed to produce different top recommendations depending on the similarity measure used. Demonstrates how choice of similarity metric affects recommendations. |

These datasets support step-by-step collaborative filtering implementations for evaluating similarity, nearest neighbors, and weighted recommendation scores.

## Notebook Features

- Similarity measures (Manhattan, Euclidean, Pearson, Cosine)
- Nearest neighbor identification
- Weighted recommendation scoring
- Summary statistics and output display for recommendations

## Notes

- The notebook format is ideal for step-by-step exploration and experimentation.
- Weighted recommendations include distance-based and exponential decay weighting.
- Missing ratings are handled gracefully during similarity calculations.