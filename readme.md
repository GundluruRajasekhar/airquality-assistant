# 🌿 Urban Air Quality Assistant

A lightweight, accessible, offline-first web app that turns an AQI reading into a clear category and personalised health advice for city residents.

**Live demo:** `https://<your-github-username>.github.io/Urban-Air-Quality-Assistant/`
**Author:** Gundluru Rajasekhar

---

## ✨ Features
- **AQI Checker:** enter 0-500 and get category, description, colour, and gauge.
- **Personalised advice:** general public, children, elderly, respiratory conditions, outdoor workers.
- **History:** last 10 checks as a table and bar chart (stored only on your device).
- **AQI scale and daily tips:** quick reference built into the page.
- **Dark mode** and **reduced-motion** support.
- **Zero dependencies:** no API keys, no frameworks, no tracking.

## 🧱 Project Structure
```
Urban-Air-Quality-Assistant/
├── index.html        # Complete app (HTML + CSS + JS in one file)
├── requirements.md   # Problem, requirements, acceptance criteria
├── readme.md         # This file
└── tasks.md          # Task breakdown and test checklist
```

## 🚀 Run Locally
1. Download or clone the repository.
2. Double-click `index.html`. That's it.

## 🌐 Deploy to GitHub Pages (one shareable link)
1. Create a **public** repository named `Urban-Air-Quality-Assistant`.
2. Upload the four files to the root of the repository.
3. Go to **Settings → Pages → Build and deployment**.
4. Set **Source: Deploy from a branch**, **Branch: main**, **Folder: / (root)**, then **Save**.
5. After about a minute your link is `https://<username>.github.io/Urban-Air-Quality-Assistant/`.

## 🧠 How It Works
Rule-based logic maps the AQI to one of six standard EPA categories. Advice is data-driven: each category has base actions, and the selected audience adds a targeted tip once the risk level is high enough for that group.

| AQI | Category |
|-----|----------|
| 0-50 | Good |
| 51-100 | Moderate |
| 101-150 | Unhealthy for Sensitive Groups |
| 151-200 | Unhealthy |
| 201-300 | Very Unhealthy |
| 301-500 | Hazardous |

## ♿ Accessibility
- Semantic landmarks (`header`, `nav`, `main`, `section`, `footer`) and a skip link
- Every input has a visible `<label>`; errors use `role="alert"`
- Results announced via `aria-live="polite"`
- High-contrast colours; category is always shown as text, not colour alone
- Full keyboard support with visible focus outlines
- Responsive from 320px up; scrollable tables on small screens

## 🔒 Security and Privacy
- User text is written with `textContent` (no `innerHTML`), preventing XSS
- Input validated and length-limited
- No external scripts, fonts, or network calls
- History stays in your browser; clear it any time

## 🧪 Testing
See the test checklist in [`tasks.md`](tasks.md). Sample values to try: `42`, `87`, `135`, `178`, `245`, `340`. Invalid values (`-5`, `600`, `12.5`, blank) show an error.

## 🔮 Future Enhancements
Live AQI via public APIs, city search and maps, multilingual support, PWA install, and alert notifications.

## ⚠️ Disclaimer
This tool provides general information, not medical advice. Consult a healthcare professional for personal health concerns.

## 📄 License
MIT: free to use and learn from.
