# WordWhiz 🐾 — Emoji Word Game

> A fun, colorful word guessing game for kids aged 9–13. Guess words from emoji clues, build streaks, and earn badges!

![WordWhiz Preview](https://raw.githubusercontent.com/alfredang/wordguessing/main/preview.png)

## 🎮 How to Play

1. **Look** at the emoji clues — they spell out a secret word
2. **Choose** the correct answer from 4 options
3. **Build** streaks for bonus points! 🔥
4. **Complete** all 3 tiers to become a WordWhiz champion! 🏆

## ✨ Features

- 🌟 **3 Tiers** — Beginner (Animals), Intermediate (Food), Advanced (Sports)
- 🔥 **Streak System** — Consecutive correct answers earn bonus points
- 💡 **Hints** — Reveal emoji clues when stuck (costs 30 points)
- ⏱️ **Speed Bonus** — Answer within 5 seconds for +50 points
- 🏅 **7 Badges** — Earn achievements like "Streak 5+" and "Score 1000+"
- 📱 **Mobile-Friendly** — Works on phones, tablets, and desktop
- 🔊 **Sound Effects** — Web Audio API pop, cheer, and buzz sounds
- 💾 **High Score** — Saved locally in your browser

## 🛠️ Tech Stack

- **Single HTML file** — No build tools, no dependencies
- **Pure CSS** — CSS animations, no canvas/JS for UI
- **Vanilla JavaScript** — ES6+, Web Audio API for sound
- **Google Fonts** — Fredoka One + Nunito

## 🚀 Run Locally

```bash
# Just open index.html in any browser
open index.html
```

Or serve with Python:

```bash
python3 -m http.server 8000
# Then visit http://localhost:8000
```

## 📂 Project Structure

```
wordguessing/
├── index.html   # The complete game
├── SPEC.md      # Design specification
└── README.md    # This file
```

## 🎯 Word Categories

| Tier | Category | Sample Words |
|------|----------|--------------|
| 🌟 Beginner | Animals | dog, cat, lion, eagle, shark |
| 🔥 Intermediate | Food | pizza, burger, sushi, mango, taco |
| 💎 Advanced | Sports | soccer, tennis, judo, surfing, boxing |

## 📦 Deploy to GitHub Pages

This repo includes a GitHub Action that auto-deploys to GitHub Pages on every push to `main`.

**Live Site:** https://alfredang.github.io/wordguessing/

**Topics:** `game` `html` `css` `javascript` `emoji` `kids` `word-game` `educational` `fun`

## 🤝 Contributing

Pull requests welcome! For major changes, please open an issue first.

## 📄 License

MIT — go wild! 🎉
---
Powered by [Tertiary Infotech Academy Pte. Ltd](https://www.tertiarycourses.com.sg/)
