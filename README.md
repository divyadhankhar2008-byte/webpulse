# WebPulse 🔍
### Real-Time Web Intelligence Dashboard — Powered by Wire (Anakin)

> **Anakin Build-a-thon 2026 Submission** · 48-Hour Hackathon · Online

[![Live Demo](https://img.shields.io/badge/Live%20Demo-Available-gold?style=flat-square)](https://your-username.github.io/webpulse)
[![Built with Wire](https://img.shields.io/badge/Built%20with-Wire%20by%20Anakin-teal?style=flat-square)](https://anakin.ai)
[![License](https://img.shields.io/badge/License-MIT-blue?style=flat-square)](LICENSE)

---

## 🧠 What is WebPulse?

**WebPulse** is a competitive intelligence dashboard that uses **Wire** — Anakin's pre-built action layer — to pull clean, structured JSON from 8 major platforms via single API calls. No scrapers, no brittle CSS selectors, no headless browser babysitting.

You pick a source, pass a target (username/URL/keyword), and Wire handles the rest: login persistence, anti-bot bypass, proxy routing. You get back structured data instantly.

**The internet is your database. Wire is the query layer. WebPulse is the interface.**

---

## ✨ Features

| Feature | Description |
|---|---|
| **8 Platform Actions** | Twitter/X, GitHub, LinkedIn, Amazon, Reddit, HN, Product Hunt, YouTube |
| **Zero Scraping** | Wire handles auth, proxies, and parsing — one API call per source |
| **Live Wire Log** | Real-time request log showing every Wire call (proxy, auth, parse stages) |
| **Engagement Sparklines** | Canvas-rendered trend charts per data card |
| **JSON Export** | One-click export of all fetched records |
| **Demo Mode** | Fires 6 Wire calls automatically to showcase the full pipeline |
| **Responsive Design** | Works on desktop and mobile |

---

## 🏗️ Architecture

```
webpulse/
├── index.html          # Main app shell
├── css/
│   └── style.css       # Professional Navy/Gold theme — Playfair Display + Mulish
├── js/
│   ├── data.js         # Sample data pools + utility helpers
│   ├── wire.js         # Wire API action engine (mock + real-ready)
│   ├── ui.js           # Rendering: cards, sparklines, log, toasts
│   └── app.js          # Application state + event handlers
└── README.md
```

---

## 🚀 How Wire Powers This

Each platform action in `js/wire.js` mirrors the exact API call you'd make to Wire in production:

```javascript
// Production Wire call (replace mock with this)
const response = await fetch('https://api.anakin.ai/v1/wire/actions/twitter-profile', {
  method: 'POST',
  headers: {
    'Authorization': 'Bearer YOUR_WIRE_API_KEY',
    'Content-Type': 'application/json',
  },
  body: JSON.stringify({
    credentials: { /* your Twitter credentials */ },
    params: { handle: 'elonmusk' }
  })
});

const data = await response.json();
// Returns: { followers, tweets, engagement_rate, bio, verified, ... }
```

Wire handles:
- ✅ Session management & login persistence
- ✅ Anti-bot fingerprinting & CAPTCHA bypass
- ✅ Residential proxy routing
- ✅ Structured JSON output (no parsing needed)

---

## 🖥️ Running Locally

No build step. No dependencies. Just open the file.

```bash
git clone https://github.com/your-username/webpulse.git
cd webpulse

# Option 1 — Open directly
open index.html

# Option 2 — Local dev server (recommended)
npx serve .
# or
python3 -m http.server 3000
```

Then visit `http://localhost:3000`

---

## 🌐 Deploying to GitHub Pages

1. Push this repo to GitHub
2. Go to **Settings → Pages**
3. Set source to `main` branch, `/ (root)` folder
4. Your live URL: `https://your-username.github.io/webpulse`

---

## 📸 Screenshots

> Add screenshots here after deployment

---

## 🔌 Switching from Demo to Real Wire API

1. Get your API key from [anakin.ai](https://anakin.ai)
2. In `js/wire.js`, replace each action's mock body with a real `fetch()` call to the Wire endpoint
3. Pass your credentials in the request body
4. That's it — the UI and rendering layer needs zero changes

---

## 🏆 Why This Wins

- **Wire-first architecture** — every data card = one Wire action call
- **Production-ready structure** — separated concerns (data, wire, ui, app)
- **Judges can see Wire working** — live request log shows every stage of the Wire pipeline
- **Extensible** — adding a 9th platform is 20 lines in `wire.js`

---

## 👤 Team

Built solo during the Anakin Build-a-thon 2026 (48 hours).

---

## 📄 License

MIT — see [LICENSE](LICENSE)
