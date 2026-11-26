# Movie Recommendation System
### Collaborative Filtering Built From Scratch

## 1. Project Overview

This project focuses on building a Movie Recommendation System using collaborative filtering techniques.

The system analyses user ratings and movie preferences to recommend movies that users may enjoy.

The project implements three recommendation approaches:

- User-User Collaborative Filtering
- Item-Item Collaborative Filtering
- Matrix Factorization

The models are developed and evaluated using the MovieLens Latest Small dataset.

## 2. Project Objectives

- Understand and implement collaborative filtering techniques.
- Explore user rating patterns and movie preferences.
- Generate personalised movie recommendations.
- Compare recommendation models using evaluation metrics.
- Visualise model performance using Microsoft Power BI.

## 3. Dataset

**Dataset:** MovieLens Latest Small

The dataset contains movie information and user ratings.

Key dataset statistics:

- 610 unique users
- 9,742 movies in the movie information file
- 100,836 user ratings
- Rating scale: 0.5 to 5.0

The main files used were:

- `ratings.csv` — User ratings for movies.
- `movies.csv` — Movie titles and genres.

## 4. Methodology

The project was completed through the following stages:

### 4.1 Data Preparation
- Loaded and explored the MovieLens dataset.
- Performed SQL-based data exploration using SQLite.
- Created a User-Item Rating Matrix.
- Split the data into training and testing sets.

### 4.2 User-User Collaborative Filtering
- Calculated similarity between users using cosine similarity.
- Identified users with similar movie preferences.
- Generated recommendations based on similar users' ratings.

### 4.3 Item-Item Collaborative Filtering
- Calculated similarity between movies using cosine similarity.
- Identified similar movies.
- Generated recommendations based on movie similarity.

### 4.4 Matrix Factorization
- Implemented Matrix Factorization using Stochastic Gradient Descent (SGD).
- Learned latent user and movie representations.
- Generated predicted movie ratings and recommendations.

### 5. Model Evaluation

The recommendation models were evaluated using ranking metrics:

Precision@10: Measures how many of the top 10 recommended movies were relevant.

Recall@10: Measures how many relevant movies were successfully recommended.

For Matrix Factorization, prediction accuracy was also measured using:

RMSE (Root Mean Squared Error)

MAE (Mean Absolute Error)

### 6. Results

The following results were obtained during model evaluation:

| Model | Precision@10 | Recall@10 | RMSE | MAE |
|---|---:|---:|---:|---:|
| User-User CF | 0.0108 | 0.0140 | — | — |
| Item-Item CF | 0.0002 | 0.0000 | — | — |
| Matrix Factorization | 0.0615 | 0.0444 | 0.8664 | 0.6653 |

The ranking metrics were evaluated across 600 eligible users.

Matrix Factorization achieved the best Precision@10 and Recall@10 among the three approaches.

RMSE and MAE were calculated for Matrix Factorization only.

### 7. Visualisation

A Power BI dashboard was created to present:

Precision@10 comparison

Recall@10 comparison

Test RMSE and MAE

Movie recommendations with model-based filtering

### 8. Limitations

The dataset is relatively small compared with real-world recommendation platforms.

User-User and Item-Item Collaborative Filtering produced relatively low ranking metrics.

Matrix Factorization predictions frequently reached the maximum rating of 5.0 due to prediction clipping.

The recommendation system does not incorporate movie content or additional user information.

### 9. Tools and Technologies

Python

Pandas and NumPy

Scikit-learn

SQLite

Google Colab

Microsoft Power BI

Visual Studio Code

Git and GitHub

## 10. Project Structure

```text
Movie_Recommendation_System/
│
├── notebooks/
│   └── Movie_Recommendation_System.ipynb
│
├── data/
│   ├── metrics.csv
│   └── recommendations.csv
│
├── powerbi/
│   └── Movie_Recommendation_System.pbix
│
└── documentation/
    └── README.md
```

## 11. Conclusion

This project provided practical experience in developing collaborative filtering recommendation systems from scratch.

By implementing and comparing User-User Collaborative Filtering, Item-Item Collaborative Filtering, and Matrix Factorization, the project explored different approaches to personalised movie recommendations.

It also provided hands-on experience in data preparation, similarity computation, model evaluation, and data visualisation.