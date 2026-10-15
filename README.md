# 🎬 Movie Recommendation System

A **content-based movie recommendation system** built with Python. Enter your favorite movie, and the system suggests the 20 most similar movies based on genres, keywords, tagline, cast, and director.

## 📌 How It Works

1. **Data Loading:** Load the movies dataset (`movies.csv`) using Pandas.
2. **Preprocessing:** Select the key features (`genres`, `keywords`, `tagline`, `cast`, `director`) and fill missing values with empty strings.
3. **Feature Combination:** Merge all selected features into a single text representation for each movie.
4. **Vectorization:** Convert the combined text into numerical vectors using **TF-IDF** (`TfidfVectorizer`).
5. **Similarity Calculation:** Compute movie-to-movie similarity using **cosine similarity**.
6. **Fuzzy Matching:** Use `difflib.get_close_matches` to find the closest title, so typos and partial names still work.
7. **Recommendation:** Sort movies by similarity score and return the top 20 matches (excluding the input movie itself).

## 🛠️ Tech Stack

- **Python**
- **Pandas** & **NumPy**: data handling and preprocessing
- **Scikit-learn**: TF-IDF vectorization and cosine similarity
- **Matplotlib** & **Seaborn**: similarity heatmap visualization
- **difflib**: fuzzy title matching

## 📂 Project Structure

```
├── movie_recommendatio_system.ipynb   # Main notebook
├── movies.csv                         # Dataset (add your own copy)
└── README.md
```

## 🚀 Getting Started

### 1. Clone the repository

```bash
git clone https://github.com/your-username/your-repo.git
cd your-repo
```

### 2. Install dependencies

```bash
pip install numpy pandas scikit-learn matplotlib seaborn jupyter
```

### 3. Add the dataset

Place `movies.csv` in the project folder. Then update the path in the notebook:

```python
movies_data = pd.read_csv("movies.csv")
```

> The notebook was originally written in Google Colab, where the path is `/content/movies.csv`.

### 4. Run the notebook

```bash
jupyter notebook movie_recommendatio_system.ipynb
```

## 💡 Example Usage

```
Enter your favourite movie: avatar

Movies Suggested for you :

1  . Movie A
2  . Movie B
3  . Movie C
...
```

## 📊 Visualization

The notebook includes a heatmap of the similarity matrix (first 20 movies) to show how closely movies relate to each other based on their content.

## 🔮 Future Improvements

- Build an interactive web app with **Streamlit** or **Gradio**
- Add a hybrid approach combining content-based and collaborative filtering
- Include movie ratings and popularity in the ranking
- Deploy the app online

## 👤 Author

**[Abdallah Elkady]**
[LinkedIn](https://www.linkedin.com/in/abdallah-elkady-aba0032b4/)
