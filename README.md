# IMDb Watchlist & Achievements Tracker

A collection of web utilities for cataloging your movie list and tracking completion of the IMDb Top 500 films and the IMDb Top 250 list, styled with a Criterion Collection dashboard aesthetic.

## Deployed Live Apps

- 📊 **[IMDb Watchlist Manager](https://suz41.github.io/imdb-watchlist/)**
- 🏆 **[IMDb Top 250 Achievements Tracker](https://suz41.github.io/imdb-watchlist/top250.html)**
- 🏅 **[IMDb Top 500 Achievements Tracker](https://suz41.github.io/imdb-watchlist/top500.html)**

## Features

### 1. Watchlist Manager (`index.html`)
* Personal movie logger with local storage persistence.
* Comprehensive statistics tracker (runtime, genre distribution, count).
* Autocomplete movie suggestions.

### 2. Top 250 Achievements Tracker (`top250.html`)
* Interactive grid showing all 250 movies sorted by rank, rating, and release date.
* **10 Unlockable Achievements**: Director collections (e.g. Nolan, Coppola), decade milestones, genre badges, and volume achievements.
* **High Performance Poster Loading System**:
  * **Instant Image Delivery**: Uses the integrated local Amazon thumbnail URLs initially to load the entire page instantly with zero network delay.
  * **Prioritized Viewport Fetching**: Utilizes an `IntersectionObserver` to track which posters are coming into view and shifts their TMDB fetching tasks to the front of the loading queue.
  * **Self-Healing Fallbacks**: If a default poster fails to load, the system displays a gold-accented text placeholder and triggers an on-demand background search on TMDB.
  * **Failure Caching**: Caches failed API searches as `"failed"` in LocalStorage, preventing repeated redundant queries on subsequent page loads.
  * **Visual Polish**: Includes smooth CSS image fade-ins (`opacity 0.4s`) and interactive poster zoom effects on hover.
* **Bidirectional Watchlist Sync**: Real-time two-way synchronization between your personal watchlist (`index.html`) and the Top 250 checklist.

### 3. Top 500 Achievements (`top500.html`)
* Gamified checklist parsing the Top 500 movies of the decade, featuring 9 unlockable badges and progress indicators.

### 4. Premium Aesthetic
* Designed with Outfit and Playfair Display typography, responsive glassmorphic cards, gold/copper accents (`#f5c518`, `#e0a96d`), and dark theme backdrops.

## Local Running

Start a local server to view:
```bash
python -m http.server
```
Visit `http://localhost:8000`.
