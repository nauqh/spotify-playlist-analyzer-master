# 🎧 Resonance – Spotify Playlist Analyzer

![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=fafafa) ![Streamlit](https://img.shields.io/badge/streamlit-%231E7EFF?style=for-the-badge&logo=streamlit&logoColor=white) ![Plotly](https://img.shields.io/badge/plotly-%2300416A.svg?style=for-the-badge&logo=plotly&logoColor=white) ![scikit-learn](https://img.shields.io/badge/scikit--learn-%23388CBF.svg?style=for-the-badge&logo=scikit-learn&logoColor=white)

A Streamlit application that analyzes any public Spotify playlist and provides interactive visualizations, music-taste insights, and content-based song recommendations. 

---

## Features

- **Playlist Extraction**: Fetches track metadata and audio features via the Spotify Web API.
- **Music Taste Analysis**: Uses summary statistics and GPT-4 to describe your playlist’s mood, valence, energy, and more.
- **Interactive Charts**: Radar plots, bar charts, timelines, decade breakdowns, genre word clouds.
- **Obscurity & Popularity**: Computes an obscurity score and highlights your most/least popular tracks and artists.
- **Top Artists & Genres**: Displays your top artists and a word cloud of your favorite genres.
- **Content-Based Recommendations**: Generates 10 similar tracks not already in your playlist using a KNN + cosine similarity pipeline.

---

## Installation

1. Clone this repository:
   ```bash
   git clone https://github.com/nauqh/spotify-playlist-analyzer-master.git
   cd spotify-playlist-analyzer-master
   ```
2. Create and activate a virtual environment (optional but recommended):
   ```bash
   python -m venv venv
   source venv/bin/activate   # macOS/Linux
   venv\Scripts\activate    # Windows
   ```
3. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
4. Create a `.env` file in the project root with your Spotify API credentials:
   ```ini
   ID=<YOUR_SPOTIFY_CLIENT_ID>
   SECRET=<YOUR_SPOTIFY_CLIENT_SECRET>
   ```

---

## Usage

Run the Streamlit app:
```bash
streamlit run app/main.py
```

- Enter a Spotify playlist URL or click **Try sample playlist**.
- Click **Find out** to load data and view your analysis.

---

## Environment Variables

- `ID`: Your Spotify API Client ID.
- `SECRET`: Your Spotify API Client Secret.

---

## Project Structure

```
├── app/
│   ├── engine.py      # Recommendation pipeline (KNN + cosine similarity)
│   ├── graph.py       # Plotting and analysis utilities
│   ├── main.py        # Streamlit interface
│   └── utils.py       # Spotify API wrappers and extraction logic
├── data/              # CSV snapshots (optional)
├── img/               # Static images for docs
├── requirements.txt   # Python dependencies
├── .streamlit/        # Streamlit theme configuration
└── README.md          # This documentation
```

---

## License

This project is released under the MIT License. See [LICENSE](LICENSE) for details.
