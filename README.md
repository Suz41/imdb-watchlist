# IMDb Watchlist Manager

A high-fidelity, personal movie catalog and watchlist logger designed with a dark, glassmorphic cinema dashboard style. Manage what you want to watch, log completed films, and track your total watch time metrics automatically.

---

## Key Features

- **Personal Film Logger**: Log any film with title, genres, release year, runtime, ratings, and custom poster art.
- **Smart Autocomplete**: Quick lookup database populated with some of the most popular movies (e.g. *The Shawshank Redemption*, *Inception*, *The Godfather*, etc.) to speed up logging.
- **Visual Grouping**: Watchlist categorized cleanly into **Want to Watch** and **Completed** sections.
- **Watchlist Statistics**: Real-time count of total logged items, status breakdowns, and a cumulative watch time calculator.
- **Durable Persistence**: Saves all logged entries automatically inside the browser's `LocalStorage`.
- **Search & Filters**: Multi-criteria search input with genre-specific dropdown pills and multiple sorting options (A-Z title, rating height, newest/oldest year).

---

## Design Systems

- **Typography**: Playfair Display (editorial serif headlines) + Outfit (modern high-readability sans-serif text)
- **Palette**: Void black background (`#060608`), glassmorphic content cards (`rgba(14, 14, 18, 0.75)` with blurred backdrops), and warm golden accents (`#f5c518`).
- **Icons**: Loaded via FontAwesome CDN for high quality indicators.

---

## Installation & Local Test

To view the application locally, start a static web server inside the directory:
```bash
python -m http.server
```
Then visit `http://localhost:8000` in your web browser.
