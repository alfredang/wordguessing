# Word Guessing Game — SPEC.md

## 1. Project Overview

**Name:** WordWhiz 🐾  
**Type:** Interactive word guessing game  
**Target Users:** Kids aged 9–13  
**Summary:** A vibrant, emoji-rich word guessing game where players decode animated emojis into words. Earn points, streak bonuses, and collect badges.  
**Target GitHub Repo:** `https://github.com/alfredang/wordguessing`

---

## 2. Visual & UI Specification

### Theme & Aesthetic
- **Style:** Playful, cartoonish, with bold colors and bouncy animations
- **Font:** "Fredoka One" (Google Fonts) — rounded, kid-friendly
- **Background:** Deep purple gradient (`#1a0533` → `#2d1b69`) with floating star particles (CSS animated)
- **Cards/panels:** Frosted glass effect with rounded corners (border-radius: 20px)

### Color Palette
| Element | Color |
|---|---|
| Primary accent | `#FF6B6B` (coral red) |
| Secondary accent | `#4ECDC4` (teal) |
| Correct highlight | `#6BCB77` (green) |
| Wrong highlight | `#FF9F43` (orange) |
| Background gradient | `#1a0533` → `#2d1b69` |
| Card bg | `rgba(255,255,255,0.12)` |
| Text primary | `#FFFFFF` |
| Text secondary | `#E0E0FF` |

### Layout
- **Header:** Logo "WordWhiz 🐾", score badge, streak flame counter
- **Main area:** 
  - Emoji puzzle card (large, centered, animated bounce-in)
  - 4 letter-option buttons below
  - Progress bar (level/tier)
- **Footer:** Hint button (limited), score multiplier indicator

### Animations
- Emoji card: `bounceIn` on new puzzle
- Correct answer: confetti burst + scale pulse
- Wrong answer: shake animation
- Streak: flame icon pulses
- Background: slow-drifting stars (CSS keyframes)

---

## 3. Game Mechanics

### Core Loop
1. A category is shown (e.g., "🐕 Animals")
2. 4–6 emoji clues are displayed representing the word
3. Player types their guess in an input field
4. 4 answer options appear (1 correct + 3 distractors)
5. Player selects an answer
6. Feedback: ✅ correct / ❌ wrong (with reveal)
7. Points awarded, next puzzle loads

### Scoring
- Base points per correct answer: **100**
- Streak bonus: +10 per consecutive correct (e.g., streak 5 → +50 bonus)
- Time bonus: +50 if answered within 5 seconds
- Wrong answer: 0 points, streak resets

### Progression
- 10 puzzles per tier
- 3 tiers: 🌟 Beginner, 🔥 Intermediate, 💎 Advanced
- Completing all 3 tiers shows a "You Win!" celebration screen

### Hints
- 3 hints total per game
- Using a hint costs 30 points and reveals one emoji clearly
- Hints reset each game

### Word Bank (categorized)
**Animals:** dog, cat, lion, eagle, shark, frog, horse, panda, whale, snake  
**Food:** pizza, burger, sushi, mango, grape, pasta, taco, donut  
**Space:** rocket, planet, star, moon, comet, galaxy, alien, saturn  
**Sports:** soccer, tennis, chess, judo, swim, golf, surfing, boxing  

---

## 4. Interaction Specification

### Controls
- **Mouse/Touch:** Tap answer buttons to select
- **Keyboard:** Type letters directly, Enter to submit guess
- **On-screen keyboard:** ABC buttons for mobile/touch users

### Screens
1. **Home/Start Screen** — Logo, "Play!" button, high score display
2. **Game Screen** — Category, emoji clues, options, score, streak, hint button
3. **Result Screen** — Final score, accuracy %, badges earned, "Play Again"

### Feedback
- Sound effects: pop on tap, cheer on correct, buzz on wrong
- Haptic: vibrate on mobile (if supported)

---

## 5. Technical Specification

### Stack
- **Single HTML file** with embedded CSS and JavaScript
- No build tools required — open directly in browser
- Canvas-free: pure DOM + CSS animations

### Data
- Word bank hardcoded as JS object (category → words → emoji clues)
- High score stored in `localStorage`

### Performance
- Lightweight: < 5MB total
- Loads under 1 second
- Works offline after first load

---

## 6. Acceptance Criteria

- [ ] App loads and shows start screen with animated background
- [ ] Tapping "Play!" starts a game with first puzzle
- [ ] Category and emoji clues display correctly
- [ ] 4 answer options shown, one is correct
- [ ] Correct answer → green highlight + confetti + points added
- [ ] Wrong answer → shake + reveal correct answer
- [ ] Streak counter updates and flame animates on streak ≥ 3
- [ ] Score updates in real-time
- [ ] Hint button reveals one emoji and deducts 30 points (if points ≥ 30)
- [ ] After 10 puzzles → next tier screen or result screen
- [ ] Result screen shows final score, accuracy %, play again button
- [ ] High score persists via localStorage
- [ ] Responsive: works on mobile (375px) and desktop (1920px)
- [ ] All animations smooth (60fps)