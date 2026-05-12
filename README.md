# 🎨 Stroop Challenge

A fast-paced browser game based on the Stroop effect — a color word is shown in a mismatched ink color, and you must identify the **ink color**, not the word.

---

## 🚀 Features

- 20 rounds per game with a 2-second timer per round
- Bonus points for fast answers
- Streak counter with fire mode 🔥
- Global leaderboard — top 10 best scores across all players
- Player name saved in browser (asked only once)
- Change name anytime from Settings
- Single HTML file — no install, no build step

---

## 🌍 Global Leaderboard Setup

The leaderboard uses [JSONBlob](https://jsonblob.com) (free, no account needed).

**After deploying, do this once:**

1. Open your hosted site and play one full game
2. Open DevTools → Application → Local Storage
3. Copy the value of `stroop_blob_id`
4. Open `index.html` and find this line:
   ```js
   const BLOB_ID = '';
   ```
5. Paste your ID:
   ```js
   const BLOB_ID = 'your-id-here';
   ```
6. Re-upload the file

Now every visitor shares the same global leaderboard.

---

## 🏗️ Hosting

**Netlify Drop** (easiest)
1. Go to [netlify.com/drop](https://netlify.com/drop)
2. Drag and drop `index.html`
3. Done — live URL instantly

**Vercel**
1. Go to [vercel.com/new](https://vercel.com/new)
2. Upload `index.html`
3. Deploy

**GitHub Pages**
1. Push `index.html` to a GitHub repo
2. Go to Settings → Pages → select branch
3. Your site is live at `https://yourusername.github.io/repo-name`

---

## 📁 Files

```
index.html   — the entire game (HTML + CSS + JS in one file)
README.md    — this file
```

---

## 🛠️ Tech

- Vanilla HTML, CSS, JavaScript — no frameworks
- [JSONBlob API](https://jsonblob.com/api) — global score storage
- [Google Fonts](https://fonts.google.com) — Space Mono + Syne
- localStorage — saves player name per browser

---

## 🎮 How to Play

1. Enter your name (saved for future visits)
2. A color word appears in a mismatched ink color
3. Tap the **ink color** — not what the word says
4. Answer before the timer runs out
5. Score is based on accuracy + speed
