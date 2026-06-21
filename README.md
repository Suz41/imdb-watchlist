# IMDb Watchlist & Achievements Tracker

A collection of web utilities for cataloging your movie list and tracking completion of the IMDb Top 250 list, styled with a minimal black-and-white Criterion Collection aesthetic.

## Deployed Live Apps

- 📊 **[IMDb Watchlist Manager](https://suz41.github.io/imdb-watchlist/)**
- 🏆 **[IMDb Top 250 Achievements Tracker](https://suz41.github.io/imdb-watchlist/top250.html)**

## Features

### 1. Watchlist Manager (`index.html`)
* Personal movie logger with local storage persistence.
* Comprehensive statistics tracker (runtime, genre distribution, count).
* Autocomplete movie suggestions.

### 2. Top 250 Achievements Tracker (`top250.html`)
* Interactive 5-column grid showing all 250 movies sorted by rank, rating, and release date, with movie numbers overlaid.
* **10 Unlockable Achievements**: Director collections (e.g. Nolan, Coppola), decade milestones, genre badges, and volume achievements.
* **High Performance Poster Loading System**:
  * **Robust Fallback Search**: Uses an adaptive fallback search algorithm on TMDB API. If year-constrained search fails to yield results, it falls back to a clean title-based query, ensuring 100% poster matching.
  * **Instant Image Delivery**: Attempts to load high-efficiency CDN thumbnails initially, displaying a clean text card overlay with movie rank numbers on failure.
  * **Prioritized Viewport Fetching**: Utilizes an `IntersectionObserver` to track which posters are coming into view and shifts their TMDB fetching tasks to the front of the queue.
  * **Failure Caching**: Caches verified failed API queries as `"failed"` in LocalStorage, preventing redundant subsequent queries.
  * **Visual Polish**: Includes smooth CSS image fade-ins (`opacity 0.4s`) and interactive poster zoom effects on hover.
* **Bidirectional Watchlist Sync**: Real-time two-way synchronization between your personal watchlist (`index.html`) and the Top 250 checklist.

### 3. Premium Minimal Aesthetic
* Designed with Outfit and Playfair Display typography, responsive glassmorphic cards, and a strictly minimal dark black-and-white theme.

## Local Running

Start a local server to view:
```bash
python -m http.server
```
Visit `http://localhost:8000`.
