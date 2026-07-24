🎬 MaitFlix

A Netflix-inspired cinematic portfolio site that showcases trailers, teasers, and descriptions for movies and TV series — powered live by The Movie Database (TMDB) API.

🔗 Live Demo: maitflixoriginals.netlify.app

⚠️ Disclaimer: MaitFlix is a portfolio/demo project. It does not host or stream any full-length copyrighted content — only publicly available trailers, teasers, posters, and metadata via TMDB.

✨ Features
Netflix-style UI — dark theme, red accent branding, hero banner, and horizontally scrolling content rows, built to closely mimic the real Netflix experience.
Auto-rotating hero carousel — cycles through trending titles every 7 seconds with a smooth fade transition, pulling official title logos (or a styled text title as fallback) and backdrop art.
Dynamic content rows, each populated live from TMDB:
Trending Now
Upcoming Hollywood Blockbusters
Future Bollywood Hits
Binge-Worthy Series
Comedy Central
Horror Night
Bollywood Hits (high-rated, by vote count)
Live search with autocomplete — searches movies & TV shows across TMDB as you type and jumps straight to a title's hero view.
Trailer modal — click "Watch Trailer" to open an embedded YouTube trailer/teaser, along with match %, release year, plot overview, and top billed cast.
Immersive intro — a disclaimer/welcome screen with a Netflix "tudum" sound effect, followed by ambient background music with a mute/unmute toggle.
Responsive card interactions — hover-to-scale content cards with title overlays.
🛠️ Tech Stack
HTML5 / CSS3 — single-page layout, custom properties (CSS variables) for theming, Flexbox-based responsive rows
Vanilla JavaScript — no frameworks; all data fetching, DOM rendering, carousel, search, and modal logic hand-rolled with the Fetch API
TMDB API — trending titles, discovery/genre queries, search, videos (trailers), images, and credits
Fonts & Icons — Google Fonts (Bebas Neue, Montserrat), Font Awesome 6
Hosting — deployed on Netlify
