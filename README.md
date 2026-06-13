MOVIE RECOMMENDATION SYSTEM (TF-IDF + COSINE SIMILARITY)

PROJECT OVERVIEW
This project is a content-based movie recommendation system using TF-IDF Vectorization and Cosine Similarity.
It recommends movies based on similarity of genres and keywords from the TMDB 5000 dataset.

DATASET
- tmdb_5000_movies.csv
- Features used:
  - title
  - genres (JSON format)
  - keywords (JSON format)

WORKFLOW
1. Load dataset
2. Parse JSON fields (genres, keywords)
3. Combine features into text representation
4. Apply TF-IDF Vectorization
5. Compute Cosine Similarity
6. Recommend similar movies

DATA PREPROCESSING
- Convert JSON string to Python objects using json.loads
- Extract genre names and keywords
- Merge them into a single string per movie

FEATURE ENGINEERING
Each movie is represented as:
genres + keywords → text document

TF-IDF VECTORIZATION
Used to convert text into numerical vectors:
from sklearn.feature_extraction.text import TfidfVectorizer

COSINE SIMILARITY
Measures similarity between movies:
from sklearn.metrics.pairwise import cosine_similarity

RECOMMENDATION LOGIC
1. Map movie title to index
2. Get vector of selected movie
3. Compute similarity with all movies
4. Sort by similarity score
5. Return top N similar movies

EXAMPLE
Input: "The Dark Knight"
Output:
- Batman Begins
- The Dark Knight Rises
- Man of Steel
- Watchmen
- Batman Forever

TECH STACK
- Python
- Pandas
- NumPy
- Scikit-learn

CONCEPTS USED
- TF-IDF
- Cosine Similarity
- Content-Based Filtering
- Text Vectorization

FUTURE IMPROVEMENTS
- Add movie overview text
- Use Word Embeddings (Word2Vec / BERT)
- Build hybrid recommender system
- Deploy as web app (Streamlit / Flask)

AUTHOR
Created for learning NLP and recommendation systems.
