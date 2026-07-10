# Movie Recommendation System 🎬
## Dataset

### Source
The project uses **The Movies Dataset** available on Kaggle:

[The Movies Dataset - Kaggle](https://www.kaggle.com/datasets/rounakbanik/the-movies-dataset)

### Files Used

| File | Description |
|------|-------------|
| `credits.csv` | Contains movie cast and crew information used for feature engineering. |
| `movies_metadata.csv` | Contains movie metadata including titles, genres, overview, ratings, and popularity. |

### Note
The dataset is not included in this repository because some files exceed GitHub's maximum file size limit. Download the dataset from Kaggle and add the required CSV files to the project folder before running the recommendation 

## Overview
This project implements a **content-based movie recommendation system** that recommends movies similar to a user's selected movie.

The system analyzes movie information such as genres, keywords, cast, crew, and descriptions, then uses Natural Language Processing (NLP) techniques to find similarities between movies.

## Features
- Search for a movie title and receive similar movie recommendations
- Handles incorrect movie titles using fuzzy matching
- Provides top-N movie recommendations
- Uses text similarity to identify movies with similar content

## Technologies Used
- Python
- Pandas
- NumPy
- Scikit-learn
- TF-IDF Vectorizer
- Cosine Similarity
- Difflib (Fuzzy String Matching)

## How It Works

### 1. Data Preprocessing
The movie datasets are cleaned and combined by:
- Removing missing values
- Combining relevant movie features into a single text column (`tags`)
- Preparing data for text processing

### 2. Feature Extraction
TF-IDF (Term Frequency-Inverse Document Frequency) is used to convert movie descriptions into numerical vectors.

### 3. Similarity Calculation
Cosine similarity is calculated between movie vectors to measure how similar movies are.

### 4. Recommendation
When a user enters a movie title:
- The system finds the movie in the dataset
- Calculates similarity scores
- Returns the top recommended movies

## Example

Input:
```
Avatar
```

Output:
```
1. Avatar: The Way of Water
2. Guardians of the Galaxy
3. Star Wars: The Force Awakens
...
```

## Project Structure

```
movie-recommendation-system/
│
├── movie_recommendation.ipynb
├── movies.csv
├── credits.csv
├── README.md
└── requirements.txt
```

## Installation

Clone the repository:

```bash
git clone https://github.com/immutuakirema-svg/movie-recommendation-system.git
```

Navigate to the project folder:

```bash
cd movie-recommendation-system
```


## Running the Project

Open the Jupyter Notebook:

```bash
jupyter notebook
```

Run the cells and provide a movie title to get recommendations.

## Future Improvements
- Build a web application using Streamlit
- Add collaborative filtering recommendations
- Include user ratings
- Deploy the model online

## Author
Brandon Mutua
