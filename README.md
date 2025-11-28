# 2024 U.S. Election Text Mining Modules

## Project Context
* **Course:** IM 5054 Introduction of Text Mining
* **Project Title:** Political Spectrum and Sentiment Analysis: Investigating Social Platforms' Stance on the U.S. Election
* **Team Members:**
    * Chao-An Wang
    * Hsin-Yu Huang
    * Tzu-Huan Huang
    * Yu-Chen Lin
    * Hsiao-Lien Peng

## About This Repository
This repository serves as a code archive for specific technical components of our final group project. While the full group report focuses on sentiment analysis (VADER) and political stance detection, this repository contains:

1.  **Data Collection Module**: The Reddit crawler used to build the project's corpus (Group Contribution).
2.  **Clustering Experiment**: An independent unsupervised learning extension conducted individually (Personal Extension, not included in the final group report).

## Repository Contents

### 1. Data Collection (`reddit_crawler.ipynb`)
The primary data acquisition tool for the project.
* **Function:** Scrapes high-engagement posts from political subreddits (`r/Politics`, `r/Liberal`, `r/Conservative`) using the PRAW library.
* **Features:**
    * Filters posts based on election-specific keywords (e.g., "2024 election", "vote", "primary").
    * Extracts metadata including titles, timestamps, and engagement metrics (upvotes).
    * Data cleaning pipeline to handle special characters and formatting issues.

### 2. Topic Clustering (`clustering.ipynb`)
*Note: This is an extended experiment exploring latent topics in the news data.*
* **Goal:** To group related news/posts without prior labeling using unsupervised learning techniques.
* **Methods:**
    * **Vectorization:** TF-IDF (Term Frequency-Inverse Document Frequency) to convert text data into numerical vectors.
    * **Clustering Algorithms:**
        * **DBSCAN:** Used for density-based clustering to handle noise and identify outliers.
        * **K-Means:** Applied to categorize distinct topics within the dataset.
    * **Analysis:** Includes elbow method visualization and keyword extraction for each cluster.

## Technologies Used
* **Python 3.x**
* **PRAW** (Python Reddit API Wrapper)
* **Scikit-learn** (KMeans, DBSCAN, TfidfVectorizer)
* **Pandas & NumPy**
* **Matplotlib & Seaborn**
