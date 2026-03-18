# 🎬 Movie Recommendation System

A **content-based movie recommendation engine** that suggests similar movies based on metadata like genres, cast, crew, and keywords — powered by Cosine Similarity and deployed as an interactive Streamlit web app.

---

## 🚀 Live Demo
> 🔗 [Coming Soon — Streamlit Deployment]

---

## 📌 Overview

Ever wondered how Netflix or Spotify knows what to suggest next? This project replicates that core idea using **Content-Based Filtering** — analyzing what a movie *is* rather than what users *rated* it.

Given any movie title, the system finds the **Top 5 most similar movies** by computing similarity across key metadata features from the TMDB dataset.

---

## ✨ Features

- 🔍 Search any movie and get 5 instant recommendations
- 🧠 Content-based filtering using NLP-style feature extraction
- ⚡ Fast results via precomputed similarity matrix (Pickle)
- 🎨 Clean and interactive Streamlit UI
- 🎥 Movie poster fetching via TMDB API

---

## 🛠️ Tech Stack

| Tool | Purpose |
|------|---------|
| Python | Core language |
| Pandas & NumPy | Data processing |
| Scikit-learn | Vectorization & Cosine Similarity |
| TMDB Dataset | Movie metadata |
| Pickle | Model serialization |
| Streamlit | Web app deployment |

---

## 🧠 How It Works

```
User inputs a movie title
        ↓
Fetch movie's feature vector (genres + cast + crew + keywords + overview)
        ↓
Compute Cosine Similarity against all movies in dataset
        ↓
Return Top 5 most similar movies
```

1. **Data Preprocessing** — Combined genres, cast, crew, keywords into a single `tags` column
2. **Vectorization** — Converted tags into numerical vectors using Count Vectorizer
3. **Similarity Computation** — Applied Cosine Similarity to find closest matches
4. **Serialization** — Saved model & similarity matrix using Pickle for fast loading
5. **Deployment** — Built interactive UI with Streamlit

---

## 📂 Project Structure

```
Movie-recommendation-system/
│
├── app.py                  # Streamlit web app
├── movie_recommendation.ipynb  # Model building notebook
├── movies.pkl              # Serialized movie data
├── similarity.pkl          # Precomputed similarity matrix
├── requirements.txt        # Dependencies
└── README.md
```

---

## ⚙️ Installation & Setup

```bash
# 1. Clone the repository
git clone https://github.com/byteephantom/Movie-recommendation-system.git
cd Movie-recommendation-system

# 2. Install dependencies
pip install -r requirements.txt

# 3. Run the app
streamlit run app.py
```

---

## 📦 Requirements

```
pandas
numpy
scikit-learn
streamlit
requests
pickle-mixin
```

---

## 📊 Dataset

- **Source:** [TMDB Movie Dataset — Kaggle](https://www.kaggle.com/datasets/tmdb/tmdb-movie-metadata)
- **Size:** 5000+ movies
- **Features used:** title, genres, keywords, cast, crew, overview

---

## 🙋‍♂️ Author

**YOUR NAME**
- GitHub: [@byteephantom](https://github.com/byteephantom)
- LinkedIn: [your-linkedin](https://linkedin.com/in/yourprofile)

---

## 📄 License

This project is licensed under the [MIT License](LICENSE).

---

⭐ If you found this project helpful, consider giving it a star!
