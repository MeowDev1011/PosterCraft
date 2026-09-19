
# PosterCraft

> **Free Poster Maker** — Split any image into multi-page sheets and export a print-ready PDF. Turn any picture into a giant wall poster using only a regular home printer.

[![Live Demo](https://img.shields.io/badge/Live%20Demo-PosterCraft-4f8cff?logo=githubpages&logoColor=white)](https://meowdev1011.github.io/PosterCraft/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://github.com/MeowDev1011/PosterCraft/blob/main/LICENSE)
[![Made with JavaScript](https://img.shields.io/badge/Made%20with-JavaScript-F7DF1E?logo=javascript&logoColor=black)](#)
[![jsPDF](https://img.shields.io/badge/Powered%20by-jsPDF-red)](#)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](#contributing)

---

## 🌐 Live Demo

**Try it now:** [**https://meowdev1011.github.io/PosterCraft/**](https://meowdev1011.github.io/PosterCraft/)

No installation, no download. Everything runs in your browser.

---

## 📖 Overview

**PosterCraft** is a lightweight, dependency-free web application that takes one or more images and slices them into a **grid of printable sheets**. Each sheet is exported as a page in a PDF, so you can print them on any standard home or office printer and glue them together to create a giant poster — no plotter required.

Think of it as **Blockposters** in a single HTML file, but with more paper sizes, better quality control, and full multilingual support.

Everything runs **100% in the browser**. No server, no uploads, no tracking. Your images never leave your device.

---

## ✨ Features

### 🖼️ Image handling
- Upload **1 to 500 images** at once
- Single image → fills the entire poster and gets split into sheets (true puzzle mode)
- Multiple images → composed into a customizable grid
- Support for **JPEG, PNG, WebP, GIF, BMP, and SVG**
- Automatic image validation (max 30,000 px per side, 250 MP per image)

### 📐 150+ paper sizes
- **ISO A series** (A0–A10)
- **ISO B series** (B0–B10)
- **ISO C series** (envelopes)
- **US / ANSI** (Letter, Legal, Tabloid, Ledger, ANSI A–F)
- **ARCH** (A–E1)
- **Canadian** (P1–P6)
- **JIS** (Japanese B series)
- **Chinese GB/T**
- **French classics** (Cloche, Carré, Cavalier, Colombier…)
- **DIN** (German)
- **Traditional Japanese** (Kiku, Shirokuban…)
- **Photo sizes** in inches and cm (including ⭐ exact **4 × 6 in**)
- **Square sizes** for social media
- **Posters, plafonds, billboards**
- **Custom dimensions** (any width × height in mm)
### 💾 Export & Print
- **Real physical size** on the PDF (A4 stays A4, 4×6 stays 4×6)
- **Required name dialog** before download — output saved as `{yourname}_poster.pdf`
- **Filename sanitization** (safe for all operating systems)
- **Cancel button** during generation
- **Progress bar** with real-time percentage

### 🖨️ One-click printing
- **Print directly** from the browser — no need to open the PDF manually
- Uses the **native browser print dialog** (`window.print()` via jsPDF `autoPrint()`)
- Works on Chrome, Edge, Firefox, and Safari
- Pick printer, paper size, orientation, and scale from the system dialog
- **Animated post-download prompt** appears after each successful download:
  > *"Tired of printing? We do it for you. Just tap the button and we print it on your printer."*
- **One click** on "Print now" opens the print dialog instantly
- **Close with X** — dismiss the prompt and return to the app
- Fully translated into all 5 languages

### 🧩 Smart layout
- **Two modes**:
  - By number of sheets (columns × rows)
  - By final physical size (define the target poster and let it calculate)
- **Overlap (glue margin)** to prevent content loss when cutting
- **Individual margins** (top, bottom, left, right)
- **Crop marks** with adjustable thickness, length, and color
- **Page numbering** on every sheet

### 🎨 Composition (multi-image mode)
- Configurable **columns × rows** grid
- Adjustable **spacing** between cells
- **Borders** with customizable color
- Three **fit modes** per cell: `cover`, `contain`, `stretch`

### ⚙️ Quality control
- Resolution up to **1200 DPI**
- **Progressive downscaling** for high-quality resampling (avoids aliasing)
- **jsPDF compression** modes: `SLOW`, `MEDIUM`, `FAST`, `NONE`
- **JPEG quality** slider (50–100%)
- Choice between **JPEG** (small) and **PNG** (lossless)
- **Transparent background** support (auto-forces PNG)
- Live **PPI/DPI quality indicator** per sheet

### 🌐 Internationalization
- **5 languages** built in:
  - 🇪🇸 Spanish
  - 🇬🇧 English
  - 🇧🇷 Portuguese
  - 🇫🇷 French
  - 🇩🇪 German
- **Automatic detection** from `navigator.language`
- **Fallback to English** if the detected language isn't supported
- **Manual switcher** in the sidebar (applies instantly, no reload)

### 🔍 Preview
- **Live poster preview** with grid overlay
- **Per-sheet thumbnail preview** (verifies the puzzle before generating)
- **Grid overlay** showing cut lines and sheet boundaries
- Page numbers rendered directly on the preview

### 💾 Export
- **Real physical size** on the PDF (A4 stays A4, 4×6 stays 4×6)
- **Required name dialog** before download — output saved as `{yourname}_poster.pdf`
- **Filename sanitization** (safe for all operating systems)
- **Cancel button** during generation
- **Progress bar** with real-time percentage

### 🚀 Performance
- **Single reusable canvas** — avoids memory leaks
- **Master canvas** — renders the whole poster once, then slices
- **`toBlob()` async** instead of `toDataURL()` — no UI freezing
- **Batched rendering** with `setTimeout(0)` between sheets
- Handles **500 images × 9 sheets** smoothly

### 📱 Responsive UI
- **Progressive disclosure**: basic → advanced → expert
- Collapsible `<details>` sections keep the interface clean
- Works on **desktop, tablet, and mobile**
- Dark theme by default

### 🔒 Privacy
- **Zero network requests** after initial load (only jsPDF from CDN)
- **No analytics, no telemetry, no cookies**
- **No server-side processing** — everything happens locally

---

## 🚀 Quick Start

### Option 1 — Use the live version
Just visit **[https://meowdev1011.github.io/PosterCraft/](https://meowdev1011.github.io/PosterCraft/)** and start making posters.

### Option 2 — Run it locally
```bash
git clone https://github.com/MeowDev1011/PosterCraft.git
cd PosterCraft
```

Then open index.html in any modern browser. That's it.

Option 3 — Local server (optional)

```bash
# Python 3
python -m http.server 8000

# Node.js (with npx)
npx serve
```

Then visit http://localhost:8000/index.html.

---

📋 Usage

Basic workflow

1. Upload one or more images
2. Choose a paper size (e.g., ⭐ Foto 4 × 6 in · 10,2 × 15,2 cm)
3. Set how many sheets: columns × rows (e.g., 3 × 3 = 9 sheets)
4. (Optional) Open Advanced settings to tune margins, overlap, or grid
5. (Optional) Open Expert settings to adjust DPI, compression, or crop marks
6. Click Preview sheets to verify the puzzle is correct
7. Click Download PDF → type a name → the file saves as {name}_poster.pdf
8. Print each page, cut along the crop marks, and glue them together

Example: making a 60 × 80 cm poster with A4 sheets

1. Paper: A4 · 210 × 297 mm
2. Mode: By final size → Width: 60 cm, Height: 80 cm
3. Overlap: 10 mm (default)
4. Margins: 10 mm on all sides (default)
5. Result: 3 × 3 = 9 sheets → poster of exactly 60.4 × 80.3 cm

Example: making a giant wall poster with 4 × 6 photo sheets

1. Paper: ⭐ Foto 4 × 6 in · 10,2 × 15,2 cm
2. Mode: By number of sheets → Columns: 4, Rows: 6
3. Result: 24 sheets → final poster of 39.6 × 90.4 cm

---

🖼️ Adding your own logo

PosterCraft looks for a file called postercraft_logo.png in the same folder as index.html.

· If found: it's displayed as the app logo (transparent background recommended)
· If missing: an inline SVG logo is used instead

You can drop in your own logo (recommended height: 80–120 px, transparent PNG).

---

🛠️ Tech Stack

Layer Technology
UI Vanilla HTML + CSS (no framework)
Logic Vanilla JavaScript (ES6+)
PDF generation jsPDF 4.2.1
Icons Inline SVG (Lucide-style)
i18n Custom lightweight system
Hosting GitHub Pages

No build step. No npm install. No bundler. Everything is in a single HTML file.

---

📁 Project structure

```
PosterCraft/
├── index.html             ← the entire application
├── postercraft_logo.png   ← optional logo (transparent PNG)
├── README.md              ← this file
├── LICENSE                ← MIT License
└── screenshots/
    ├── main.png
    ├── preview.png
    └── pdf-output.png
```

---

🌍 Translations

Currently supported locales:

Code Language Status
es Spanish ✅ Complete
en English ✅ Complete
pt Portuguese ✅ Complete
fr French ✅ Complete
de German ✅ Complete

Adding a new language

1. Open index.html
2. Find the I18N object
3. Copy the en block and translate all values
4. Add the new <option> to the #langSelect element
5. Make sure the key matches the ISO 639-1 two-letter code (e.g., it, ru, ja)

---

🚀 Deploying to GitHub Pages

This project is already deployed on GitHub Pages from the main branch root.

To deploy your own fork:

1. Go to your repository on GitHub
2. Open Settings → Pages
3. Under Source, select Deploy from a branch
4. Choose Branch: main and folder: / (root)
5. Click Save
6. Wait ~1 minute — your site will be live at https://<your-username>.github.io/PosterCraft/

Because the entry file is named index.html, GitHub Pages serves it automatically.

---

🔒 Security & privacy

· No image upload: everything is processed locally in your browser
· No external calls except loading jsPDF from the official CDN
· Input validation: image dimensions capped at 30,000 × 30,000 px and 250 MP
· Defensive clamping: prevents out-of-bounds reads during the tiling process
· Filename sanitization: strips OS-reserved characters (\/:*?"<>|)
· Safe URLs: external links use rel="noopener noreferrer"

---

🐛 Known limitations

· Very large posters (>200 sheets) will prompt a confirmation before generating
· Safari < 15 may struggle with 1200 DPI on huge posters (use 300 DPI instead)
· Transparent backgrounds require PNG format (auto-switched)
· Requires an internet connection on first load (to fetch jsPDF from CDN)

---

🗺️ Roadmap

☐ Offline mode (bundle jsPDF locally)
☐ Save/load project settings as JSON
☐ Additional export formats (SVG, PNG per sheet)
☐ Preset templates ("A2 poster on A4", "Instagram grid"…)
☐ More languages (Italian, Russian, Japanese, Chinese, Arabic)
☐ PDF metadata customization
☐ Print directly from the browser

Have an idea? Open an issue.

---

🤝 Contributing

Contributions, bug reports, and feature requests are welcome!

1. Fork the repository
2. Create a branch: git checkout -b feature/my-feature
3. Commit your changes: git commit -m "Add some feature"
4. Push to the branch: git push origin feature/my-feature
5. Open a Pull Request

Please make sure:

· The code stays framework-free
· New UI strings are added to all 5 languages
· You test on Chrome and Firefox before submitting

---

📄 License

This project is licensed under the MIT License — see the LICENSE file for details.

You are free to use, modify, and distribute this software, including for commercial purposes, as long as the original copyright notice is preserved.

---

👤 Author

[![GitHub - MeowDev1011](https://img.shields.io/badge/GitHub-MeowDev1011-181717?logo=github)](https://github.com/MeowDev1011)

---

🙏 Acknowledgments

· jsPDF — client-side PDF generation
· Lucide — icon inspiration
· Blockposters — the original inspiration
· GitHub Pages — free static hosting
· Everyone who reported bugs and suggested features

---

⭐ Show your support

If PosterCraft saved you from buying an expensive plotter, consider giving it a star on GitHub. It helps others discover the project.

[![GitHub stars](https://img.shields.io/github/stars/MeowDev1011/PosterCraft?style=social)](https://github.com/MeowDev1011/PosterCraft)

---

<p align="center">
  Made with ❤️ by <a href="https://github.com/MeowDev1011">MeowDev1011</a>
  <br>
  <sub>PosterCraft — Free Poster Maker · MIT Licensed</sub>
</p>
