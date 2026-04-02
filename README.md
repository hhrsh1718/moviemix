# 🍿 Moviemix

A movie recommendation web app built with Flask and Machine Learning.

---

## What it does

Search for a movie you like, and Moviemix will instantly suggest 10 similar movies. It also fetches real reviews and tells you if the audience liked it or not (sentiment analysis).

---

## Features

- 🔍 **Smart Search** — Autocomplete search from a 25,000 movie dataset
- 🎯 **Recommendations** — Suggests 10 movies using a hybrid ML algorithm
- 💬 **Sentiment Analysis** — Classifies real reviews as *Good* or *Bad*
- 🎭 **Cast Info** — Shows cast photos, bios, and character roles
- 🎬 **Genre Browsing** — Browse movies by genre
- ⚡ **Fast** — Pre-computed vectors + parallel API calls = quick load times

---

## How it works

1. You type a movie name
2. The app finds similar movies using cosine similarity on TF-IDF vectors
3. Movie details, posters, and cast are fetched from the TMDb API
4. Reviews are run through a Naive Bayes classifier for sentiment

---

## Tech Stack

| Layer | Tools |
|---|---|
| Backend | Python, Flask |
| ML | scikit-learn, scipy, pandas, numpy |
| Frontend | HTML, CSS, JavaScript, Jinja2 |
| API | TMDb API |

---

## Run Locally

```bash
# Clone the repo
git clone https://github.com/hhrsh1718/moviemix.git
cd moviemix

# Create and activate virtual environment
python -m venv venv
venv\Scripts\activate        # Windows
# source venv/bin/activate   # Mac/Linux

# Install dependencies
pip install -r requirements.txt

# Start the app
python app.py
```

Then open **http://127.0.0.1:10000** in your browser.

---

## Project Structure

```
moviemix/
├── app.py                  # Flask app + ML logic
├── requirements.txt        # Dependencies
├── data/                   # Movie + review datasets
├── models/                 # Trained ML models
├── static/                 # CSS, JS files
└── templates/              # HTML pages
    ├── home.html
    ├── recommend.html
    └── genre.html
```

---

> This product uses the TMDb API but is not endorsed or certified by TMDb.

Made with ❤️ for movie lovers.
