# HyuckJoon Kwon — Personal Portfolio

🌐 **Live site:** [https://DARKXIGN.github.io](https://DARKXIGN.github.io)

Personal portfolio website built with React (CDN) — no build step required.  
Supports **English / Korean** language toggle.

---

## 📁 File Structure

```
DARKXIGN.github.io/
├── index.html   ← Main portfolio (all-in-one)
├── 404.html     ← Redirects unknown URLs back to index
└── README.md    ← This file
```

## 🚀 Deployment

This site deploys automatically via **GitHub Pages**.

1. Push changes to the `main` branch
2. GitHub Pages serves `index.html` at `https://DARKXIGN.github.io`
3. Changes go live within ~1 minute

## ✏️ How to Update Content

All content lives inside `index.html` in the `T` (translations) object and the data arrays near the top of the `<script>` tag.

### Update project GitHub links
Find each project in `T.en.projects` and `T.ko.projects` and replace the `github` field:
```js
{ id: 1, name: "Pilot ...", github: "https://github.com/DARKXIGN/your-repo", ... }
```
Set `github: null` for private repos — they'll show a 🔒 Private badge automatically.

### Add LinkedIn recommendations
Find `T.en.recs` and `T.ko.recs` and replace the placeholder text with your actual recommendations.

### Add a new project
Add an object to both `T.en.projects` and `T.ko.projects`:
```js
{
  id: 6,
  featured: false,           // set true to span 2 columns
  name: "Project Name",
  date: "Month Year",
  stack: ["React", "Python"],
  desc: "Short description of what you built.",
  github: "https://github.com/DARKXIGN/repo",
  demo: null                 // or "https://your-demo-url.com"
}
```

## 🛠 Tech Stack

- **React 18** — loaded via CDN (no npm install needed)
- **Babel Standalone** — JSX transpiled in-browser
- **Google Fonts** — DM Serif Display + Outfit
- **GitHub Pages** — free static hosting

---

Built by HyuckJoon Kwon · briankwon1004@gmail.com
