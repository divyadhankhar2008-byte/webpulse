# WebPulse 🔍
### Real-Time Competitive Intelligence — Powered by Wire (Anakin)

> **Anakin Build-a-thon 2026 Submission** · 48-Hour Hackathon · Online · Solo

[![Live Demo](https://img.shields.io/badge/Live%20Demo-Available-c9a84c?style=flat-square)](https://divyadhankhar2008-byte.github.io/webpulse)
[![Built with Wire](https://img.shields.io/badge/Built%20with-Wire%20by%20Anakin-2dd4bf?style=flat-square)](https://anakin.ai)
[![License](https://img.shields.io/badge/License-MIT-blue?style=flat-square)](LICENSE)
[![Hackathon](https://img.shields.io/badge/Anakin-Build--a--thon%202026-gold?style=flat-square)](https://unstop.com)

---

## 🧠 What is WebPulse?

**WebPulse** is a competitive intelligence dashboard that uses **Wire** — Anakin's pre-built action layer — to pull clean, structured JSON from 8 major platforms via single API calls.

No scrapers. No brittle CSS selectors. No headless browser babysitting. No maintenance.

> **The internet is your database. Wire is the query layer. WebPulse is the interface.**

You pick a source, pass a target (username / URL / keyword), and Wire handles everything: login persistence, anti-bot bypass, proxy routing. You get back structured data in ~1 second.

---

## ✨ Features

| Feature | Description |
|---|---|
| **8 Platform Actions** | Twitter/X, GitHub, LinkedIn, Amazon, Reddit, Hacker News, Product Hunt, YouTube |
| **4 Use Case Presets** | Track Competitor, Monitor Launch, Research Founder, Market Snapshot |
| **Compare Mode** | Fetch two targets and view them side by side |
| **Wire Explainer** | Live panel showing exactly how Wire processes each request |
| **Real-World Impact Cards** | 3 documented use cases for founders, growth teams, researchers |
| **Live Wire Log** | Real-time request log: proxy routing, auth, anti-bot, parse stages |
| **Engagement Sparklines** | Canvas-rendered trend charts on every data card |
| **JSON Export** | One-click export of all fetched records |
| **Demo Mode** | Fires 6 Wire calls automatically to showcase the full pipeline |
| **Responsive Design** | Works on desktop and mobile |

---

## 🌍 Real-World Use Cases

### 🏢 Startup Founders
Track competitors across GitHub, Product Hunt and Reddit simultaneously. Know when they ship, what people say, and how fast they grow — all via Wire, updated in seconds. No expensive tools. No manual tab-switching.

### 📣 Growth Teams
Monitor a product launch in real time across LinkedIn, Twitter/X and Hacker News. See sentiment, engagement and reach the moment it happens — wire one call per platform, get everything back as structured JSON.

### 🔬 Researchers & Analysts
Profile any founder, creator or brand across platforms in one workflow. Export structured JSON for further analysis. Wire eliminates weeks of manual data collection and months of scraper maintenance.

---

## 🏗️ Architecture

```
webpulse/
└── index.html          # Complete self-contained app
                        # Includes: HTML + CSS + JS (all-in-one)
                        # Sections:
                        #   · Professional Navy/Gold UI (Playfair Display + Mulish)
                        #   · Wire API engine (mock + real-ready)
                        #   · Use case preset system
                        #   · Compare mode
                        #   · Card renderer + sparkline charts
                        #   · Wire request log
                        #   · JSON export
```

Single-file architecture — zero build step, zero dependencies, deployable anywhere.

---

## ⚡ How Wire Powers This

Every "Fetch" click fires a **Wire action** — Anakin's pre-built connector that handles the full pipeline automatically:

```
Step 1 → Pick the Wire action (twitter-profile, github-profile, amazon-product…)
Step 2 → Pass your credentials once
Step 3 → Wire handles: auth · anti-bot · proxy routing · JSON parsing
Step 4 → You get clean structured data back in ~1 second
Step 5 → Build your product on top — WebPulse is one example
```

### What Wire eliminates:
- ❌ Writing CSS selectors
- ❌ Reverse-engineering auth flows
- ❌ Managing headless browsers
- ❌ Babysitting scrapers
- ❌ Handling proxy rotation
- ❌ Bypassing CAPTCHAs manually

### What you get instead:
- ✅ One API call
- ✅ Clean structured JSON
- ✅ ~1 second response
- ✅ Zero maintenance

### Production Wire call example:
```javascript
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
// Returns: { followers, tweets, engagement_rate, bio, verified, avg_likes, ... }
// Wire handled: login, anti-bot, proxy, parsing — all of it.
```

---

## 🚀 Running Locally

No build step. No npm install. No dependencies.

```bash
git clone https://github.com/divyadhankhar2008-byte/webpulse.git
cd webpulse

# Option 1 — open directly in browser
open index.html

# Option 2 — local server (recommended)
npx serve .
# or
python3 -m http.server 3000
# then visit http://localhost:3000
```

---

## 🌐 Live Demo

**[https://divyadhankhar2008-byte.github.io/webpulse](https://divyadhankhar2008-byte.github.io/webpulse)**

Try these on the live site:
1. Click **🔍 Track a Competitor** — fires 3 Wire calls across GitHub, Twitter, Product Hunt
2. Click **⚡ Demo** — fires 6 Wire calls automatically
3. Click **≡ Wire Log** in sidebar — see every stage of the Wire pipeline
4. Click **⇔ Compare** — fetch two items and view side by side
5. Click **↓ Export JSON** — download all fetched data

---

## 🏆 Judging Criteria Alignment

| Criterion | Weight | How WebPulse addresses it |
|---|---|---|
| 💡 Idea | 40% | Unified intelligence layer on top of Wire — one dashboard, 8 platforms, 4 real-world workflows |
| ⚙️ Execution | 30% | Fully deployed, responsive, single-file, zero dependencies, live Wire log showing the pipeline |
| 🌍 Real-world impact | 30% | 3 documented use cases (founders, growth teams, researchers) with concrete before/after value |

---

## 🔌 Switching from Demo to Real Wire API

1. Get your API key from [anakin.ai](https://anakin.ai)
2. In `index.html`, find the `WIRE.actions` object
3. Replace each mock function body with a real `fetch()` call to the Wire endpoint
4. Pass your credentials in the request body
5. The entire UI, rendering, log, export — zero changes needed

---

## 👤 Builder

**Divya Bharti**
Banasthali Vidyapith (BU), Jaipur · Engineering · 2029
Built solo during the Anakin Build-a-thon 2026 (48 hours)

---

## 📄 License

MIT — see [LICENSE](LICENSE)
