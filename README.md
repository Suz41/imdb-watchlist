# IMDb Watchlist & achievements Portal

A premium collection of web utilities for cinema lovers, styled with a dark, glassmorphic Criterion Collection display aesthetic. 

This repository contains two main applications to catalog, track, and gamify your movie watching journey.

---

## 1. IMDb Watchlist Manager (`index.html`)
An interactive dashboard to manage and log your personal movie watchlist.

### Key Features
- **Personal Film Logger**: Add custom movies with title, genres, release year, runtime, ratings, and poster art.
- **Smart Autocomplete**: Quick lookup database populated with some of the most popular movies (e.g. *The Shawshank Redemption*, *Inception*, *The Godfather*) to speed up logging.
- **Visual Grouping**: Watchlist categorized cleanly into **Want to Watch** and **Completed** sections.
- **Statistics Widget**: Real-time counter of total items, status breakdowns, and cumulative watch time.
- **Persistence**: Automatically saves your logged data inside the browser's `LocalStorage`.

---

## 2. IMDb Top 500 Tracker & Badges (`top500.html`)
A minimalist gamified tracker for completing the top 500 movies of the decade.

### Key Features
- **Client-Side CSV Parsing**: Automatically downloads and parses the IMDb Top 1000 dataset in the browser, slicing it to the Top 500.
- **Minimalist Completion Tracker**: Easy checklist interface to mark films as "Watched" with instant search filters.
- **Gamified Achievements**: Unlock 9 custom badges with visual progression fills, including:
  - 🏅 **Cinephile Apprentice**: Watch at least 5 movies.
  - 🏆 **Dedicated Cinephile**: Watch at least 25 movies.
  - 👑 **Grand Completionist**: Watch 100 movies.
  - 🔥 **Action Junkie**: Watch 10 Action films.
  - 🧑‍🚀 **Sci-Fi Fanatic**: Watch 5 Sci-Fi films.
  - 🎭 **Drama Lover**: Watch 15 Drama films.
  - 🧠 **Nolan Disciple**: Watch 5 movies directed by Christopher Nolan.
  - ⌛ **Vintage Explorer**: Watch 5 movies released before 2010.
  - 🎟️ **Box Office Fan**: Watch 5 blockbusters with over 500,000 votes.
- **Achievements Tab**: Live counts showing how many badges have been unlocked.
- **Persistence**: Completion state is saved securely using browser `LocalStorage`.

---

## Design System

- **Typography**: Playfair Display (editorial serif headlines) + Outfit (modern high-readability body text)
- **Palette**: Void black background (`#060608`), glassmorphic content cards (`rgba(14, 14, 18, 0.75)` with blurred backdrops), and warm golden accents (`#f5c518`).
- **Icons**: Powered by FontAwesome for premium design.

---

## Running Locally

To run either application locally, start a static web server inside this directory:
```bash
python -m http.server
```
Then visit:
- **Watchlist Manager**: `http://localhost:8000/index.html` (or simply `http://localhost:8000/`)
- **Achievements Tracker**: `http://localhost:8000/top500.html`
