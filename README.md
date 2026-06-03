# Movie Recommendation System

A Machine Learning-based Movie Recommendation System built using the Rotten Tomatoes Movies and Movie Reviews datasets. The project leverages Content-Based Filtering techniques to recommend movies that are similar to a selected movie based on genres, directors, writers, ratings, and review information.

---

![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white)
![Scikit-learn](https://img.shields.io/badge/scikit--learn-F7931E?style=for-the-badge&logo=scikit-learn&logoColor=white)
![Matplotlib](https://img.shields.io/badge/Matplotlib-11557C?style=for-the-badge&logo=python&logoColor=white)
![Seaborn](https://img.shields.io/badge/Seaborn-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Machine Learning](https://img.shields.io/badge/Machine%20Learning-Recommender%20System-green)

## 📌 Project Overview

With thousands of movies available across streaming platforms, users often struggle to find content that matches their interests. This project addresses that challenge by developing a Movie Recommendation System capable of suggesting relevant movies using movie metadata and critic review information.

The system analyzes movie characteristics such as:

* Genre
* Director
* Writer
* Audience Score
* Critic Score (Tomatometer)
* Ratings
* Critic Reviews

and generates personalized recommendations based on content similarity.

---

## 🎯 Problem Statement

Movie recommender systems have become increasingly important in the entertainment industry due to the massive amount of content available online. Users often face difficulty discovering movies that match their preferences.

The objective of this project is to build a recommendation engine that utilizes movie attributes and review information to provide meaningful and relevant movie suggestions. The system focuses on identifying similarities between movies using content-based machine learning techniques.

---

## 📂 Dataset Information

### 1. Rotten Tomatoes Movies Dataset

**File:** `rotten_tomatoes_movies.csv`

Contains movie-related metadata:

| Feature          | Description             |
| ---------------- | ----------------------- |
| id               | Unique movie identifier |
| title            | Movie title             |
| audienceScore    | Audience rating         |
| tomatoMeter      | Critic score            |
| rating           | Movie certification     |
| genre            | Movie genres            |
| director         | Director name           |
| writer           | Writer name             |
| runtimeMinutes   | Movie duration          |
| originalLanguage | Original language       |
| distributor      | Distribution company    |
| boxOffice        | Box office revenue      |

---

### 2. Rotten Tomatoes Movie Reviews Dataset

**File:** `rotten_tomatoes_movie_reviews.csv`

Contains critic review information:

| Feature         | Description               |
| --------------- | ------------------------- |
| reviewId        | Review identifier         |
| criticName      | Critic name               |
| reviewText      | Full review text          |
| reviewState     | Fresh/Rotten              |
| scoreSentiment  | Positive/Neutral/Negative |
| publicationName | Review source             |
| reviewUrl       | Original review link      |

---

## 🛠️ Tech Stack

### Programming Language

* Python

### Libraries Used

* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-Learn
* NLTK
* Surprise
* WordCloud

### Machine Learning Techniques

* TF-IDF Vectorization
* Cosine Similarity
* Content-Based Filtering
* Collaborative Filtering (SVD)
* Exploratory Data Analysis (EDA)

---

## 🔍 Exploratory Data Analysis

EDA was performed to understand the dataset and identify useful patterns.

### Key Findings

* Drama, Comedy, and Action are the most common genres.
* Audience scores and critic scores show moderate positive correlation.
* Japanese-language films received some of the highest audience and critic ratings.
* Most movie pairs have low similarity scores, making recommendations more meaningful.
* Top critics provide predominantly positive reviews.

### Visualizations

* Genre Distribution
* Director Analysis
* Audience vs Critic Scores
* Correlation Heatmaps
* Runtime Analysis
* Box Office Trends
* Word Clouds
* Sentiment Distribution
* Similarity Score Distribution

---

## ⚙️ Data Preprocessing

### Data Cleaning

* Removed duplicate records
* Handled missing values
* Converted data types
* Cleaned textual features
* Removed irrelevant columns

### Missing Value Treatment

* Numerical columns → Mean/Median Imputation
* Text columns → "Unknown" replacement
* Highly incomplete rows removed

### Outlier Treatment

* IQR Method
* Winsorization
* Removal of unrealistic values

---

## 🧠 Feature Engineering

Important movie attributes were combined into a single content feature:

```python
content = title + director + writer + genre
```

This unified representation allows the model to compare movies effectively.

### Features Used

* Title
* Genre
* Director
* Writer
* Rating
* Audience Score
* Tomato Meter

---

## 🤖 Recommendation Models

### 1. Popularity-Based Recommendation

Recommends movies based on popularity and ratings.

**Advantages**

* Simple implementation
* Fast recommendations

**Limitations**

* Not personalized

---

### 2. Content-Based Recommendation (Primary Model)

The main recommendation engine uses:

* TF-IDF Vectorization
* Cosine Similarity

### Workflow

1. Merge movie metadata.
2. Create content feature.
3. Convert text into TF-IDF vectors.
4. Compute cosine similarity matrix.
5. Recommend Top-N similar movies.

### Example

Input Movie:

```text
Inception
```

Recommended Movies:

```text
Interstellar
The Prestige
Memento
Tenet
The Dark Knight
```

---

### 3. Collaborative Filtering

Implemented using Singular Value Decomposition (SVD).

#### Libraries

```python
surprise
cmfrec
```

#### Evaluation Metrics

* RMSE
* MAE

Results:

```text
Average RMSE: 1.8145
Average MAE : 1.6525
```

---

## 📊 Model Validation

### Content-Based Model

Validated using:

* Cosine Similarity Distribution
* Recommendation Quality Checks
* Similarity Visualization

### Collaborative Filtering

Validated using:

* 3-Fold Cross Validation
* RMSE
* MAE

---

## 📈 Results

### Achievements

✅ Successfully built a movie recommendation system

✅ Generated relevant movie recommendations using movie metadata

✅ Implemented TF-IDF and Cosine Similarity

✅ Performed extensive exploratory data analysis

✅ Evaluated collaborative filtering performance using SVD

### Business Impact

* Improved content discovery
* Better user engagement
* Personalized recommendations
* Exposure to lesser-known movies
* Enhanced streaming platform experience

---

## 📁 Project Structure

```
Movie Recommendation System/
│
├── 📁 Dataset/
│   ├── Books.Zip
|   ├── Ratings.csv
|   ├── Users.csv
│   └── recsus_taxonomy2.png
│
├── 📁 Final Report/
│   └── Final Report.pdf
|
├── 📁 Notebook/
│   └── Book Recommendation System.ipynb
|
└── 📁 README.md
```

---

## 🔮 Future Enhancements

* Hybrid Recommendation System
* Deep Learning-Based Recommendations
* User Authentication
* Real-Time Personalization
* Streamlit Web Application
* Sentiment-Aware Recommendations
* Recommendation Explainability

---

## 🤝🏿 **Contributing**

This project represents my personal learning in Data Science. While this is primarily a showcase of my work, I welcome discussions, feedback, and collaborations on data science projects.

## 📧 **Contact**

**Sanketh Ks**  
- GitHub: [@Sankethks27](https://github.com/Sankethks27)
- LinkedIn: [Sanketh Ks](https://www.linkedin.com/in/sanketh-ks-181962273/)
- Email: sankethks27@gmail.com

---

⭐ **If you find this portfolio helpful or inspiring, please give it a star!** ⭐

---
