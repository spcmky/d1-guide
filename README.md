# ⚔️ Diablo I — Companion Codex

A comprehensive single-page companion app for Diablo I (1996). Everything you need to survive the labyrinth beneath Tristram — character builds, monster resistances, shrine effects, leveling routes, gear strategies, and an interactive character builder.

![HTML](https://img.shields.io/badge/Pure-HTML%2FJS%2FCSS-e34c26)
![No Dependencies](https://img.shields.io/badge/Dependencies-None-brightgreen)
![License](https://img.shields.io/badge/License-MIT-blue)

## 🔥 Live Demo

**[https://spcmky.github.io/d1-guide/](https://spcmky.github.io/d1-guide/)**

## 📖 What's Inside

### Reference
- **Character Classes** — Warrior, Rogue, Sorcerer with full stat tables, max stats, per-level gains, tips, and weaknesses
- **Dungeon Levels** — All 16 levels across Church, Catacombs, Caves, and Hell with monster lists and strategies
- **Monster Bestiary** — 20+ monsters with HP, damage, XP, resistances, immunities, and combat tips (searchable)
- **Items & Gear** — Quality tiers, best prefixes/suffixes, and BiS (best-in-slot) loadouts per class
- **Unique Items** — Full unique item database with stats, sources, and special properties
- **Spells & Magic** — All spells with mana costs, magic requirements, and usage strategies (filterable by element)
- **Quests** — Every quest with triggers, rewards, and detailed walkthrough strategies

### Environment
- **Shrines** — All shrine types with effects, risk ratings (Safe/Risky/Avoid), and detailed descriptions
- **Fountains & Pools** — Every fountain type and whether to use them

### Strategy
- **Leveling & XP Guide** — Best farming areas for every level range with XP/hour estimates
- **Class Builds** — 2 optimized builds per class with stat priorities, gear, and playstyle breakdowns
- **Scenario Strategies** — Detailed tactics for Butcher, Skeleton King, Succubi packs, Blood Knights, Diablo fight, and more
- **Resistances & Immunities** — Complete monster resistance table showing what damage works against every enemy
- **Tips & Tricks** — Combat, items, exploration, survival, and advanced tech

### Tools
- **Character Builder** — Interactive character sheet styled like the in-game UI
  - Pick class, set level (1–50), allocate stat points
  - Equip/unequip gear from a database of normal, magic, and unique items
  - See real-time updates to Life, Mana, AC, Damage, To Hit, Resistances
  - Gear bonuses highlighted in green, penalties in red
  - Paper doll equipment display with 7 slots

## 🚀 Deployment

### GitHub Pages (Recommended)

This repo is configured for automatic GitHub Pages deployment:

1. **Push to GitHub:**
   ```bash
   git init
   git add .
   git commit -m "Initial commit — Diablo I Companion Codex"
   git branch -M main
   git remote add origin https://github.com/spcmky/d1-guide.git
   git push -u origin main
   ```

2. **Enable GitHub Pages:**
   - Go to your repo → **Settings** → **Pages**
   - Under **Source**, select **GitHub Actions**
   - The included workflow (`.github/workflows/deploy.yml`) handles the rest
   - Your site will be live at `https://spcmky.github.io/d1-guide/`

   **Alternative (simpler):** Under Source, select **Deploy from a branch** → pick `main` / `/ (root)` → Save. No workflow needed.

### Local

Just open `index.html` in any browser. No server, no build step, no dependencies.

### Electron (Desktop App)

To wrap it as a standalone desktop app:

```bash
npm init -y
npm install electron --save-dev
```

Create `main.js`:
```js
const { app, BrowserWindow } = require('electron');
const path = require('path');

app.whenReady().then(() => {
  const win = new BrowserWindow({ width: 1280, height: 900, title: 'Diablo I Codex' });
  win.loadFile('index.html');
  win.setMenuBarVisibility(false);
});

app.on('window-all-closed', () => app.quit());
```

Add to `package.json`:
```json
"main": "main.js",
"scripts": { "start": "electron ." }
```

Run: `npm start`

## 🛠️ Tech

- **Zero dependencies** — pure HTML, CSS, and vanilla JavaScript in a single file
- **~2000 lines** — entire app is self-contained in `index.html`
- Fonts loaded from Google Fonts (Cinzel, Crimson Text, MedievalSharp)
- No build step, no framework, no bundler

## 📝 License

MIT — do whatever you want with it. Stay a while and listen.
