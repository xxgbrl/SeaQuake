# 🌊 SeaQuake

**Real-time earthquake monitor for ASEAN and nearby regions**, built on live public data from **BMKG** (Indonesia's Meteorology, Climatology, and Geophysics Agency) / InaTEWS.

Inspired by BMKG's official **WRS-AEIC** mobile app — SeaQuake is a lightweight, installable web app with the same at-a-glance experience: a live map, an event feed, and a detail view you can share as an image.

**🔴 Live demo:** https://seaquake.pages.dev

> ⚠️ SeaQuake is an independent, unofficial project — **not affiliated with or endorsed by BMKG**. All earthquake data is sourced from BMKG's public InaTEWS feed (`bmkg-content-inatews.storage.googleapis.com`). For official warnings and information, always refer to [inatews.bmkg.go.id](https://inatews.bmkg.go.id) or other official BMKG channels.

## ✨ Features

- **Live map** — every recent earthquake plotted with MapLibre GL, sized and colored by magnitude, with the latest event pulsing so it stands out
- **Auto-focus on the latest quake** — opening or refreshing the app flies straight to the newest event and opens its info card, just like the official app
- **Event list** — scrollable feed of recent earthquakes with magnitude, depth, time, and region
- **Detail view** — a dedicated screen per earthquake with its own focused map, magnitude/depth/coordinates, and region info
- **Active faults overlay** — togglable fault-line layer on the map
- **Share / Save image** — generates a shareable earthquake card; opens the native share sheet on mobile (pick any app to send it to) or downloads a PNG on desktop
- **Installable (PWA)** — add it to your home screen for a native app–like experience
- **Responsive** — works well on mobile and desktop, with a two-pane layout on larger screens
- Dark UI, no front-end framework, kept lightweight on purpose

## 🛠️ Tech Stack

- Plain HTML, CSS, and JavaScript — no build step, no framework
- [MapLibre GL JS](https://maplibre.org/) for the interactive vector map
- Basemap by [CARTO](https://carto.com/basemaps)
- Live earthquake feed from BMKG (XML)
- Web Share API for native image sharing on mobile

## 🚀 Running locally

No build tools required — just serve the static files:

```bash
# clone the repo
git clone https://github.com/xxgbrl/inatews.git
cd inatews

# serve with any static server, e.g.:
npx serve .
# or
python3 -m http.server 8080
```

Then open `http://localhost:8080` (or whichever port your server uses) in your browser.

## ⚙️ Configuration

This project uses a CARTO basemap API key embedded directly in `index.html`. If you deploy your own copy, it's recommended to swap it for your own key from [CARTO](https://carto.com/basemaps).

## 📂 Project Structure

```
seaquake/
├── index.html      # all markup, styling, and app logic
├── favicon.ico
├── favicon-16x16.png
├── favicon-32x32.png
├── apple-touch-icon.png
├── android-chrome-192x192.png
├── android-chrome-512x512.png
├── site.webmanifest
├── robots.txt
├── sitemap.xml
├── LICENSE
└── README.md
```

## 🙏 Data Source & Credits

- Earthquake data: [BMKG](https://www.bmkg.go.id/) / [InaTEWS](https://inatews.bmkg.go.id/)
- Map & basemap: [MapLibre GL JS](https://maplibre.org/) & [CARTO](https://carto.com/)
- Design inspired by BMKG's official **WRS-AEIC** mobile app

## 🤝 Contributing

Issues and pull requests are welcome — found a bug or have an idea? Feel free to open one.

## 📄 License

Licensed under the [MIT License](./LICENSE).
