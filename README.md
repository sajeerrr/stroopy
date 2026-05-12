# 🎨 Stroop Challenge

A fast-paced browser game based on the **Stroop effect** — a color word appears in a mismatched ink color, and you must identify the **ink color**, not what the word says.

---

## 🚀 Features

- 20 rounds per game with a 2-second timer per round
- Bonus points for fast answers
- Streak counter with fire mode 🔥
- Global leaderboard — top 10 best scores across all players (powered by Firebase)
- Player name saved in browser (asked only once)
- Change name anytime from Settings
- Single HTML file — no install, no build step

---

## 🌍 Global Leaderboard Setup

The leaderboard uses [Firebase Realtime Database](https://firebase.google.com) (free tier, no credit card needed).

**One-time setup (~2 minutes):**

1. Go to [console.firebase.google.com](https://console.firebase.google.com)
2. Create a project (any name — disable Analytics if prompted)
3. Go to **Build → Realtime Database → Create Database → Start in Test mode**
4. Copy your database URL — it looks like:
   ```
   https://your-project-default-rtdb.firebaseio.com
   ```
5. Open `index.html` and find this line:
   ```js
   const FIREBASE_URL = 'YOUR_FIREBASE_URL';
   ```
6. Paste your URL:
   ```js
   const FIREBASE_URL = 'https://your-project-default-rtdb.firebaseio.com';
   ```
7. Re-upload the file

Every player who visits your hosted site will now share the same global leaderboard. Scores are stored with one entry per player name — only their personal best is kept.

---

## 🏗️ Hosting

**Vercel**
1. Go to [vercel.com/new](https://vercel.com/new)
2. Upload `index.html`
3. Deploy

---

## 📁 Files

```
index.html   — the entire game (HTML + CSS + JS in one file)
README.md    — this file
```

---

## 🛠️ Tech

- Vanilla HTML, CSS, JavaScript — zero dependencies, no frameworks
- [Firebase Realtime Database](https://firebase.google.com) — global score storage (best score per player)
- [Google Fonts](https://fonts.google.com) — Space Mono + Syne
- `localStorage` — saves player name between sessions

---

## 🎮 How to Play

1. Enter your name (saved for future visits)
2. A color word appears in a mismatched ink color
3. Tap the **ink color** — not what the word says
4. Answer before the 2-second timer runs out
5. Score is based on accuracy + speed (faster answers earn bonus points)
6. Chain correct answers for a streak 🔥

---

## 🧠 What Is the Stroop Effect?

The Stroop effect is a psychological phenomenon where your brain takes longer to process the ink color of a word when the word itself names a different color. For example, seeing <span style="color:red">**BLUE**</span> written in red ink creates cognitive interference — your reading instinct fights your color perception. This game trains you to override that instinct under time pressure.
