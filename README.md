# Spotify Catalogue Analysis & Track Recommender

An end-to-end Exploratory Data Analysis (EDA), interactive artist search, and content-based song similarity project built with **Python**, **NumPy**, **Pandas**, **Matplotlib**, **Seaborn**, and **scikit-learn** in **Google Colab**.

## Project Files
- `README.md` — Project documentation and key findings
- `spotifycatalogue.ipynb` — Complete Google Colab notebook (cleaning, EDA, visualizations, artist lookup, and recommender)
- `spotify-tracks-dataset-detailed.csv` — Spotify tracks dataset
- `requirements.txt` — Required Python libraries

## Dataset & Preprocessing
- **Raw Dataset:** `114,000` tracks across `20` columns
- **Cleaned Catalogue:** `81,343` unique tracks across `23` columns after removing missing entries and deduplicating by `track_name` and `artists` (retaining highest popularity)
- **Feature Engineering:**
  - Converted `duration_ms` to `duration_min`
  - Categorized tracks into `popularity_tier` (`Hit`, `Moderate`, `Niche`)
  - Extracted artist collaboration counts (`num_artists`)

## Key Features & Insights
- **Top Popularity Analysis:** Ranked the top 100 unique tracks, led by *Unholy (feat. Kim Petras)* (`100`) and *Quevedo: Bzrp Music Sessions, Vol. 52* (`99`)[span_3](start_span)[span_3](end_span).
- **Hit vs. Niche Comparison:** `Hit` tracks (`popularity >= 75`) show higher average `danceability` (`0.636` vs. `0.545`) and lower `acousticness` (`0.214` vs. `0.333`) than `Niche` tracks[span_4](start_span)[span_4](end_span).
- **Genre Energy Distribution:** High-intensity genres like `heavy-metal` and `grindcore` cluster near maximum `energy` (`~1.0`), whereas `bluegrass` and `comedy` show lower medians and wider spreads[span_5](start_span)[span_5](end_span).
- **Interactive Artist Lookup:** Search any artist name via `input()` (including semicolon-separated collaborations) to view their track count, average popularity, and top songs.
- **Content-Based Similarity Finder:** Uses `MinMaxScaler` and `cosine_similarity` across audio features to recommend the top 5 most sonically similar songs.

## How to Run
1. Open `spotifycatalogue.ipynb` in **Google Colab** (or Jupyter Notebook).
2. Upload `spotify-tracks-dataset-detailed.csv` when prompted.
3. Run all cells from top to bottom.
4.
