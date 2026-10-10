# AetherConvert 1.0

> **Local-first image and document converter — no uploads, no server, no cost.**

AetherConvert runs entirely in your browser using the Canvas API, jsPDF, and pdf.js. Files never leave your device.

[![GitHub Pages](https://img.shields.io/badge/live-GitHub%20Pages-10B981?style=flat-square)](https://codewithswastik13.github.io/photo-to-image-converter/)

---

## Features

| Tool | Description |
|---|---|
| **JPG / PNG / WEBP Conversion** | Convert between image formats entirely in-browser |
| **Image to PDF** | Combine one or more images into a single PDF |
| **PDF to Image** | Render individual or all PDF pages as PNG / JPG / WEBP |
| **Advanced Compression** | Binary-search quality encoding to hit a target KB size |
| **Resize & Crop** | Change pixel dimensions with optional aspect-ratio lock |
| **Metadata Remover** | Strip EXIF and embedded metadata by re-encoding via Canvas |
| **Text to PDF** | Convert plain text into a paginated A4 PDF |
| **Word Counter** | Live word, character, and sentence counter |

All tools include drag-and-drop file upload, live status messages, and download buttons for the processed output.

---

## Privacy

- **Zero uploads.** Files are read using the browser's File API and processed with Canvas / Web Workers.
- **Zero tracking.** No analytics, no cookies, no external data collection.
- **Works offline** once the page and CDN scripts are cached.

---

## Tech Stack

| Library | Version | Purpose |
|---|---|---|
| [Tailwind CSS](https://tailwindcss.com) | CDN | Utility-class styling |
| [jsPDF](https://github.com/parallax/jsPDF) | 2.5.1 | PDF generation |
| [pdf.js](https://mozilla.github.io/pdf.js/) | 3.11.174 | PDF rendering |
| Google Fonts — Inter | latest | Typography |

---

## Local Development

No build step is required. Open `index.html` directly in any modern browser:

```bash
# Clone the repo
git clone https://github.com/codewithswastik13/photo-to-image-converter.git
cd photo-to-image-converter

# Open in browser (macOS / Linux)
open index.html

# Or serve locally to avoid CORS issues with pdf.js worker
npx serve .
```

---

## Deployment — GitHub Pages

The site is a single `index.html` file and deploys automatically via the included GitHub Actions workflow.

**Manual setup (first time):**
1. Go to **Settings → Pages** in your repository.
2. Set **Source** to `GitHub Actions`.
3. Push to `main` — the workflow (`.github/workflows/deploy.yml`) will publish the site.

**Live URL:** `https://codewithswastik13.github.io/photo-to-image-converter/`

---

## Repository Structure

```
.
├── index.html          # Single-file application
├── README.md           # This file
├── .gitignore
└── .github/
    └── workflows/
        └── deploy.yml  # GitHub Actions Pages workflow
```

---

## License

MIT — free to use, modify, and distribute.
