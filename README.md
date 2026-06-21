# IMDb Top 250 Achievements & Poster Tracker

A single-page web utility for tracking your watch completion of the IMDb Top 250 all-time movies, styled with a minimal, high-contrast black-and-white Criterion Collection aesthetic.

## Deployed Live App

- 🏆 **[IMDb Top 250 Achievements & Poster Tracker](https://suz41.github.io/imdb-watchlist/)**

## Features

### 1. Interactive 5-Column Grid
* Renders the 250 greatest movies of all time sorted by rank, rating, or release year.
* Custom, minimal rank badges (`1` to `250`) overlaid on top of loaded poster art.
* Fully responsive layout (5 columns on desktop/tablets, scaling to 3 columns on mobile viewports).

### 2. Gamified Achievements
* **10 Unlockable Milestones**: Track director collections (e.g. Nolan, Coppola), release decades, genre focus, and total count badges.
* Real-time progress bar updating your overall completion percentage.

### 3. High Performance Poster Loader
* **Flexible TMDB API Integration**: Queries the TMDB search API using your configured key. If year-constrained filtering returns no results, the system automatically falls back to a clean title search, guaranteeing a verified poster match.
* **Instant Fallbacks**: Attempts to load high-efficiency CDN thumbnails initially, displaying a clean text card on load failure.
* **Prioritized Viewport Fetching**: Utilizes `IntersectionObserver` to track which poster cards are visible on screen, moving their API fetching tasks to the front of the queue.
* **Fail-Safe Caching**: Safely caches retrieved posters in LocalStorage. Network errors or invalid API key status codes will not poison the cache, ensuring the system only marks a movie search as "failed" when a query successfully completes with zero results.
* **Visual Polish**: Smooth image fade-ins (`opacity 0.4s`) and interactive card scale zoom animations on hover.

### 4. Premium Minimal Theme
* Designed with Outfit and Playfair Display typography, responsive glassmorphic cards, and a dark, strictly grayscale palette.

## Local Running

Start a local server to view:
```bash
python -m http.server
```
Visit `http://localhost:8000`.
