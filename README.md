# ZyaFinance — Clean Financial Dashboard PWA

A minimalist, offline-capable budget tracker with hardware savings goal tracking. Built as a Progressive Web App — installable on **Android, iOS, Windows, macOS, Linux** without app store.

![ZyaFinance Preview](https://raw.githubusercontent.com/xyuhnlianzy/ZyaFinance/main/docs/preview.png)

## Features

- 🌙 **Dark mode** — Easy on the eyes, clean SaaS-grade UI
- 💰 **Income & Expense tracking** — Auto-calculated totals
- 🎯 **Hardware savings goal** — Visual progress bar (ThinkPad, GPU, etc.)
- 📱 **PWA** — Install like native app, works offline
- 💾 **Local-first** — All data in `localStorage`, no accounts, no cloud
- ⚡ **Zero build** — Single HTML file + manifest + service worker

## Install Guide

### Android (Chrome / Edge / Firefox / Brave)

1. Buka: **https://xyuhnlianzy.github.io/ZyaFinance/** (atau URL deploy kamu)
2. Menu browser (⋮) → **"Install app"** / **"Add to Home screen"**
3. Konfirmasi → Ikon muncul di **App Drawer / Home Screen**
4. Buka dari launcher — full-screen, no address bar

> **Firefox:** ⋮ → "Install" → "Add to Home screen"

### iOS / iPadOS (Safari only)

1. Buka URL di **Safari** (wajib Safari, bukan Chrome/Firefox iOS)
2. Tap **Share** (⬆️ kotak + panah) → **"Add to Home Screen"**
3. Nama: `ZyaFinance` → **Add**
4. Ikon di Home Screen → buka seperti app native

> ⚠️ iOS tidak support `beforeinstallprompt` event — harus manual via Share menu.

### Desktop (Windows / macOS / Linux)

**Chrome / Edge / Brave / Vivaldi:**
1. Buka URL → ikon **install** (📥) di **address bar** kanan
2. Atau: Menu (⋮) → **"Install ZyaFinance..."**
3. Konfirmasi → App muncul di **Start Menu / Applications / App Launcher**

**Firefox:**
- Firefox tidak support PWA install natively. Gunakan Chrome/Edge untuk install, atau buat shortcut manual.

## Local Development

```bash
# Clone
git clone git@github.com:xyuhnlianzy/ZyaFinance.git
cd ZyaFinance

# Serve locally (HTTPS required for SW install, but localhost works)
python3 -m http.server 8080
# Buka http://localhost:8080/zyafinance.html
```

## Deploy Free (HTTPS + Custom Domain Ready)

| Platform | Steps |
|----------|-------|
| **GitHub Pages** | Settings → Pages → Source: `main` branch / root → Save |
| **Netlify** | Drag folder ke app.netlify.com/drop → Done |
| **Vercel** | `npx vercel` di folder project → Follow prompts |
| **Cloudflare Pages** | Connect repo → Build: none, Output: `/` |

Setelah deploy, ganti URL di atas ke URL production kamu.

## Tech Stack

- **HTML5** — Single file, no framework
- **Tailwind CSS** (CDN) — Utility-first styling
- **Alpine.js** (CDN) — Reactive state management
- **Lucide Icons** (CDN) — Clean SVG icons
- **Service Worker** — Cache-first offline strategy
- **Web App Manifest** — Install metadata

## File Structure

```
ZyaFinance/
├── zyafinance.html   # Main app
├── manifest.json     # PWA manifest
├── sw.js             # Service Worker
└── .gitignore        # Clean repo rules
```

## Privacy

- **Zero tracking** — No analytics, no external requests except CDN libs
- **Local-only data** — `localStorage` di browser user
- **Works fully offline** — After first load

## License

MIT — Free to use, modify, distribute.

---

**Made with ☕ by [xyuhnlianzy](https://github.com/xyuhnlianzy)**