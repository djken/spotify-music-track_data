# Spotify Music Tracks Dataset

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Dataset](https://img.shields.io/badge/Dataset-Kaggle-blue.svg)](https://www.kaggle.com/datasets/maharshinaik/spotify-dataset-114000-songs)
[![Python](https://img.shields.io/badge/Python-3.7+-blue.svg)](https://www.python.org/downloads/)

A comprehensive dataset containing over 114,000 Spotify music tracks with various acoustic features and metadata. This dataset is designed for music analysis, recommendation system development, and exploratory data analysis (EDA).

---

## 📋 Table of Contents

- [About the Project](#about-the-project)
- [Main Features](#main-features)
- [Tech Stack](#tech-stack)
- [Project Structure](#project-structure)
- [Getting Started](#getting-started)
  - [Prerequisites](#prerequisites)
  - [Installation](#installation)
- [Usage](#usage)
- [Configuration](#configuration)
- [Tests](#tests)
- [Dataset Details](#dataset-details)
- [Roadmap](#roadmap)
- [Contributing](#contributing)
- [License](#license)
- [Contact](#contact)

---

## 📖 About the Project

This repository hosts a rich dataset of Spotify tracks, originally sourced from Kaggle. It provides a wide array of musical attributes that can be used to understand trends in music, build predictive models for song popularity, or create genre-based recommendation engines.

### Main Features

- **Large Scale**: Contains 114,000+ unique tracks.
- **Rich Metadata**: Includes track name, artist, album, and popularity.
- **Acoustic Features**: Detailed metrics for each song, including:
  - Danceability, Energy, Loudness, Speechiness.
  - Acousticness, Instrumentalness, Liveness, Valence.
  - Tempo and Time Signature.
- **Genre Diversity**: Covers a broad spectrum of musical genres.

---

## 🛠 Tech Stack

- **Data Format**: CSV (Comma Separated Values)
- **Primary Tools**:
  - [Pandas](https://pandas.pydata.org/) for data manipulation.
  - [NumPy](https://numpy.org/) for numerical computations.
  - [Matplotlib](https://matplotlib.org/) / [Seaborn](https://seaborn.pydata.org/) for visualization.
  - [Scikit-learn](https://scikit-learn.org/) for machine learning.

---

## 📂 Project Structure

```text
spotify-music-track-kaggle/
├── spotify-track-music.csv    # Main dataset file
└── README.md                   # Project documentation
```

---

## 🚀 Getting Started

### Prerequisites

To work with this dataset, it is recommended to have Python installed along with the following libraries:

```bash
pip install pandas numpy matplotlib seaborn
```

### Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/djken/spotify-music-track-kaggle.git
   ```
2. Navigate to the project directory:
   ```bash
   cd spotify-music-track-kaggle
   ```

---

## 💻 Usage

You can easily load and explore the dataset using Python and Pandas:

```python
import pandas as pd

# Load the dataset
df = pd.read_csv('spotify-track-music.csv', index_col=0)

# Display the first few rows
print(df.head())

# Get summary statistics
print(df.describe())

# Filter by genre
acoustic_tracks = df[df['track_genre'] == 'acoustic']
print(acoustic_tracks.head())
```

---

## ⚙️ Configuration

No complex configuration is required. However, if you are using this in a larger pipeline, you can configure the data path using environment variables:

```bash
export SPOTIFY_DATA_PATH="./spotify-track-music.csv"
```

---

## 🧪 Tests

To ensure the dataset integrity or test your analysis scripts, you can run:

```bash
# Example using pytest for analysis scripts
pytest tests/
```

---

## 📊 Dataset Details

The CSV file contains the following columns:

| Column | Description |
| :--- | :--- |
| `track_id` | The Spotify ID for the track |
| `artists` | The artists' names who performed the track |
| `album_name` | The album name in which the track appears |
| `track_name` | Name of the track |
| `popularity` | The popularity of the track (0-100) |
| `duration_ms` | The track length in milliseconds |
| `explicit` | Whether or not the track has explicit lyrics |
| `danceability` | How suitable a track is for dancing |
| ... | ... |
| `track_genre` | The genre in which the track belongs |

---

## 🗺 Roadmap

- [ ] Add Jupyter Notebook for Exploratory Data Analysis (EDA).
- [ ] Implement a basic Recommendation System.
- [ ] Update dataset with 2024-2025 tracks.
- [ ] Add scripts for data cleaning and preprocessing.

---

## 🤝 Contributing

Contributions are what make the open-source community such an amazing place to learn, inspire, and create. Any contributions you make are **greatly appreciated**.

1. Fork the Project
2. Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3. Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the Branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

---

## ⚖️ License

Distributed under the MIT License. See `LICENSE` for more information (if available).

---

## ✉️ Contact

**Author**: djken
**Project Link**: [https://github.com/djken/spotify-music-track-kaggle](https://github.com/djken/spotify-music-track-kaggle)
