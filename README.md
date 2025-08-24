# 🎬 Movie Recommendation System with Sentiment Analysis

## 📌 Project Overview

This project is a Movie Recommendation System enhanced with Sentiment Analysis of user reviews. Unlike traditional recommendation systems that only consider ratings, this system analyzes the sentiments of user reviews to generate more meaningful movie scores.

The dataset contains five sentiment categories:

* Positive
* Somewhat Positive
* Neutral
* Somewhat Negative
* Negative

## 📊 Novelty

A custom formula is designed to calculate the final movie rating based on the weighted contribution of these five sentiment classes, making the recommendation more reliable and realistic.

## ⚙️ Architecture

The workflow of the project can be summarized as:

1.  **Web Scraping**: Extracts movie reviews from IMDb using BeautifulSoup.
2.  **Data Preprocessing & Feature Extraction**: Cleaning, tokenization, stop-word removal, and vectorization (TfidfVectorizer).
3.  **Model Training**: Machine Learning model: Support Vector Classifier (SVC). Achieved an accuracy of 85% on the test set.
4.  **Rating Calculation**: Sentiment scores are combined using the custom rating formula.
5.  **Web Application**: Flask-based web app where users can:
    * Enter/select a movie
    * View scraped reviews with sentiment classification
    * See overall sentiment distribution & calculated rating

## 🛠️ Tech Stack

* **Programming Language**: Python 3
* **Web Framework**: Flask
* **Web Scraping**: BeautifulSoup
* **Machine Learning**: scikit-learn (SVC, TfidfVectorizer)
* **Visualization**: Matplotlib / Seaborn
* **API**: TMDB API (for fetching movie details like posters, metadata)

## 🚀 How to Run the Project

1.  **Clone the repository**
    ```bash
    git clone [https://github.com/your-username/Movie-Recommendation-System-with-Sentiment-Analysis.git](https://github.com/your-username/Movie-Recommendation-System-with-Sentiment-Analysis.git)
    cd Movie-Recommendation-System-with-Sentiment-Analysis
    ```

2.  **Install Dependencies**
    ```bash
    pip install -r requirements.txt
    ```

3.  **Set up TMDB API Key**
    * Create an account at [TMDB](https://www.themoviedb.org/).
    * Generate your API key.
    * Replace the placeholder inside `main.py` with your key:
        ```python
        api_key = "YOUR_TMDB_API_KEY"
        ```

4.  **Pretrained Model Files**
    * `nlp_model.pkl` → Trained SVC classifier
    * `transform.pkl` → Pre-fitted TfidfVectorizer
    * **✅ These files are already included in the repo.**
    * **If you want to retrain the model:**
        * Delete these `.pkl` files
        * Open and run `Movie_Reviews_Classification.ipynb`
        * New `.pkl` files will be generated

5.  **Run the Flask Web Application**
    ```bash
    python main.py
    ```

6.  **Access the Application**
    * Open your browser and visit:
    * `http://127.0.0.1:5000`
