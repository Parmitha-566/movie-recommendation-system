# Content-Based Movie Recommendation System

An end-to-end Machine Learning project that recommends the top 5 most similar movies based on content metadata (genres, keywords, taglines, cast, and directors).

## 📌 Project Overview
Unlike collaborative filtering (which requires user ratings history), this project implements **Content-Based Filtering**. It constructs a unified textual profile for each title and calculates similarity using vector angles in a high-dimensional feature space.

## 🛠️ Tech Stack & Concepts
* **Language:** Python
* **Data Wrangling:** Pandas (feature extraction, handling missing `NaN` values)
* **Text Vectorization:** Scikit-Learn `CountVectorizer` (Bag-of-Words model, stop-word removal, 5,000 max features)
* **Similarity Metric:** Cosine Similarity (4760 × 4760 pairwise distance matrix)

## ⚙️ How It Works
1. **Feature Engineering:** Merges `Movie_Genre`, `Movie_Keywords`, `Movie_Tagline`, `Movie_Cast`, and `Movie_Director` into a single text profile per title.
2. **Vector Space Transformation:** Converts text tokens into 5,000-dimensional numerical vectors.
3. **Similarity Computation:** Computes the cosine of the angle between vectors to identify semantic closeness regardless of document length.
4. **Ranking:** Sorts pairwise distance scores in descending order and returns the top 5 nearest neighbors.

## 📊 Sample Output
```text
Top 5 Recommendations for: The Dark Knight Rises
1. The Dark Knight (Similarity: 0.68)
2. Batman Begins (Similarity: 0.68)
3. Amidst the Devil's Wings (Similarity: 0.44)
4. The Killer Inside Me (Similarity: 0.37)
5. The Prestige (Similarity: 0.36)
6. Click the green **Commit changes...** button at the top right.
7. In the pop-up modal, leave the default commit message (`Update README.md`) and click **Commit changes**.

When you return to your repository's main page, the formatted README with headers, badges, and output blocks will display below your code files.

<FollowUp label="Ready to start Project 2: House Price Prediction (Regression)?" query="Walk me through Project 2: House Price Prediction from scratch in Google Colab, explaining the concepts step by step."/>
