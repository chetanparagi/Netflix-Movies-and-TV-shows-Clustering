# 🎬 Netflix Movie Recommender System

## 📌 Overview

This project aims to develop a movie recommender system for Netflix using clustering and content-based techniques. The goal is to improve user satisfaction, content discovery, and overall engagement by providing personalized movie suggestions based on user behavior and movie metadata.

---

## 🎯 Business Objectives

- **Enhanced User Experience:** Provide accurate, tailored recommendations to keep users engaged.
- **Content Utilization:** Promote broader viewership across Netflix’s extensive catalog.
- **Business Success:** Boost user retention and platform growth through effective personalization.

---

## ❓ Problem Statement

With a growing library of content, Netflix users face choice overload. This project tackles the challenge of designing a recommender system that can:

- Deliver **personalized recommendations**
- Improve **user engagement**
- Promote **content discovery**

---

## 📊 Dataset Description

The dataset contains information about movies and TV shows on Netflix. Key attributes:

| Feature         | Description                                      |
|-----------------|--------------------------------------------------|
| `show_id`       | Unique identifier for each title                 |
| `type`          | Movie or TV Show                                 |
| `title`         | Name of the title                                |
| `director`      | Director name                                    |
| `cast`          | Cast involved                                    |
| `country`       | Production country                               |
| `date_added`    | Date it was added on Netflix                     |
| `release_year`  | Year of release                                  |
| `rating`        | TV content rating (e.g., TV-MA, PG)              |
| `duration`      | Duration (in minutes or number of seasons)       |
| `listed_in`     | Genre(s)                                         |
| `description`   | Short summary or synopsis                        |

---

## 🛠️ Approach

### 🔹 Data Preprocessing

- Handled missing values and inconsistent formatting.
- Text preprocessing:
  - Lowercasing
  - Removing punctuation, URLs, digits
  - Removing stopwords
  - Tokenization & normalization
- Applied **PCA** for dimensionality reduction.

### 🔹 Clustering

- Grouped movies/shows using:
  - **K-Means Clustering**
  - **Agglomerative (Hierarchical) Clustering**
- Used **Elbow Method** and **Silhouette Score** to identify optimal number of clusters.

### 🔹 Recommendation Engine

- Used **Cosine Similarity** within clusters to recommend similar titles based on:
  - Description
  - Cast
  - Genre
  - Country
  - Director
  - Rating

---

## 🧪 Models Used

- ✅ **K-Means Clustering**  
- ✅ **Agglomerative Clustering (Hierarchical)**  
- ✅ **Cosine Similarity**  
- ✅ **Elbow Method** (for optimal clusters)  
- ✅ **Silhouette Score** (for validation)

---

## 📈 Results

- **Elbow Method:** Optimal clusters = 6 for K-Means
- **Silhouette Score:** Optimal clusters = 13 for better separation
- **Agglomerative Clustering:** Optimal clusters = 9 (validated using dendrogram)
- Built a content-based recommender using cosine similarity within clusters.

---

## ✅ Conclusion

- Cleaned and explored data using EDA techniques.
- Conducted mono- and bi-variate analysis for feature insights.
- Clustered data using both K-Means and Agglomerative methods.
- Built a recommender using cosine similarity on clustered data.

### Key Insights:
1. 69.1% of titles are movies; 30.9% are TV shows.
2. The majority of titles originate from the United States.
3. Selected six key features: `director`, `cast`, `country`, `genre`, `rating`, and `description` for clustering.
4. Achieved meaningful clustering validated by Silhouette and Elbow methods.

---

## 🚀 Future Improvements

- Incorporate collaborative filtering with user interaction data.
- Integrate deep learning models (e.g., autoencoders, BERT for text).
- Deploy as a web application using Flask/Streamlit.



