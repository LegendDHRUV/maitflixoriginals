# 🎬 MaitFlix

A Netflix-inspired cinematic portfolio site that showcases **trailers, teasers, and descriptions** for movies and TV series — powered live by **The Movie Database (TMDB) API**.

🔗 **Live Demo:** [maitflixoriginals.netlify.app](https://maitflixoriginals.netlify.app/)

> ⚠️ **Disclaimer:** MaitFlix is a portfolio/demo project. It does **not** host or stream any full-length copyrighted content — only publicly available trailers, teasers, posters, and metadata via TMDB.

---

## ✨ Features

- **Netflix-style UI** — dark theme, red accent branding, hero banner, and horizontally scrolling content rows, built to closely mimic the real Netflix experience.
- **Auto-rotating hero carousel** — cycles through trending titles every 7 seconds with a smooth fade transition, pulling official title logos (or a styled text title as fallback) and backdrop art.
- **Dynamic content rows**, each populated live from TMDB:
  - Trending Now
  - Upcoming Hollywood Blockbusters
  - Future Bollywood Hits
  - Binge-Worthy Series
  - Comedy Central
  - Horror Night
  - Bollywood Hits (high-rated, by vote count)
- **Live search with autocomplete** — searches movies & TV shows across TMDB as you type and jumps straight to a title's hero view.
- **Trailer modal** — click "Watch Trailer" to open an embedded YouTube trailer/teaser, along with match %, release year, plot overview, and top billed cast.
- **Immersive intro** — a disclaimer/welcome screen with a Netflix "tudum" sound effect, followed by ambient background music with a mute/unmute toggle.
- **Responsive card interactions** — hover-to-scale content cards with title overlays.

## 🛠️ Tech Stack

- **HTML5 / CSS3** — single-page layout, custom properties (CSS variables) for theming, Flexbox-based responsive rows
- **Vanilla JavaScript** — no frameworks; all data fetching, DOM rendering, carousel, search, and modal logic hand-rolled with the Fetch API
- **[TMDB API](https://www.themoviedb.org/documentation/api)** — trending titles, discovery/genre queries, search, videos (trailers), images, and credits
- **Fonts & Icons** — Google Fonts (`Bebas Neue`, `Montserrat`), Font Awesome 6
- **Hosting** — deployed on [Netlify](https://www.netlify.com/)

## 📁 Project Structure

This is a single self-contained `index.html` file containing all markup, styles, and scripts:

```
MaitFlix/
└── index.html   # Full site: HTML structure + CSS + JS (TMDB integration)
```

## 🚀 Getting Started

Since MaitFlix is a static single-file site, no build step is required.

1. **Clone the repo**
   ```bash
   git clone https://github.com/<your-username>/maitflix.git
   cd maitflix
   ```
2. **Add your TMDB API key**
   - Sign up for a free API key at [themoviedb.org/settings/api](https://www.themoviedb.org/settings/api).
   - Open `index.html` and replace the `API_KEY` constant near the top of the `<script>` section:
     ```js
     const API_KEY = 'YOUR_TMDB_API_KEY';
     ```
3. **Run it locally**
   - Simply open `index.html` in your browser, or serve it with any static server, e.g.:
     ```bash
     npx serve .
     ```
4. **Deploy**
   - Drag and drop the folder onto [Netlify Drop](https://app.netlify.com/drop), or connect the repo to Netlify/Vercel/GitHub Pages for continuous deployment.

## 🎯 How It Works

- On load, `init()` fetches TMDB's trending, discover, and popular endpoints for each content row and renders cards dynamically, skipping duplicates already shown in earlier rows.
- The first ten trending titles seed an auto-playing hero carousel (`updateHero()` + `startCarousel()`), which fades in the backdrop, official logo (or title text), and overview.
- The search bar debounced-queries TMDB's multi-search endpoint and renders live suggestions; selecting one jumps the hero section to that title.
- Clicking a card or search result opens `updateHero()` for that title; clicking "Watch Trailer" opens `openModal()`, which fetches the title's videos, finds a `Trailer` or `Teaser`, and embeds it via YouTube's iframe player alongside plot, rating, year, and cast pulled from the TMDB `credits` response.

## 🔮 Possible Future Improvements

- Multi-provider filtering (Netflix / Prime Video / Disney+ / Apple TV+ availability, via TMDB's `watch/providers` endpoint)
- Personalized "what to watch next" recommendations based on viewing/search history
- User watchlists and ratings
- Pagination / infinite scroll for content rows
- Environment-variable based API key handling for public deployments

## 👨‍💻 Developer

**Dhruv Gupta**
Maharaja Agrasen Institute of Technology

- 📧 dhruvharshgupta@gmail.com
- 📞 +91 8882355904

## 📄 License & Attribution

This project is for portfolio and educational purposes. All movie/TV data, images, and video links are provided via [TMDB](https://www.themoviedb.org/) and YouTube and remain the property of their respective owners. This product uses the TMDB API but is not endorsed or certified by TMDB.
