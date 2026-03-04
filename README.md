# Chi 🎲

**Chi** is a mobile-first statistical tracker for Catan (2d6) dice rolls. It uses a **Chi-Square Goodness of Fit** test to mathematically verify if your dice are "fair" or if they are behaving suspiciously.

Designed with an **iOS-native aesthetic**, it provides a smooth, haptic-style experience for tracking games in real-time.

## ✨ Features
- **Real-time Distribution:** A dynamic bar chart showing the frequency of every roll (2-12).
- **Ghost Bars:** Semi-transparent gray bars sit behind your actual rolls, showing exactly where the "fair" distribution should be.
- **Luck Tracker (Efficiency):** Add players and assign them numbers. Chi calculates each player's **Production Efficiency %** (Actual Hits vs. Expected Hits), tracking exactly when each number was acquired.
- **Statistical Engine:** Calculates the $\chi^2$ statistic and the exact **p-value** (likelihood) for 10 degrees of freedom.
- **Game Sharing:** Generate a unique link to share your current game state and player setup with others.
- **Detailed Game Archive:** Save completed games to a local archive.
    - **Swipe Left:** Delete a game.
    - **Swipe Right:** View detailed info, including the final distribution and player luck rankings.
- **Haptic Feedback:** Subtle vibrations and scaling animations on button taps for a native feel.
- **System Theme Support:** Perfectly mirrors your device's theme (Light/Dark mode).
- **Mobile Optimized:** Zero tap delay, disabled double-tap zoom, and iOS safe-area support.

## 📊 The Statistics
Chi evaluates your rolls against the theoretical triangular distribution of two 6-sided dice:
- **Total Degrees of Freedom:** 10 (11 possible outcomes minus 1).
- **Critical Value:** 18.31 (at $\alpha = 0.05$).
- **p-value:** The probability that a perfectly fair set of dice would produce a distribution at least as extreme as yours.

*Note: Statistical analysis requires at least 15 rolls to minimize small-sample errors.*

## 🚀 Local Development
Since this is a standalone static site, you don't need `npm` or any build tools.

1. Clone the repository:
   ```bash
   git clone https://github.com/kteal/chi.git
   ```
2. Open `index.html` in any browser, or use Python to spin up a local server:
   ```bash
   python3 -m http.server 8000
   ```
3. Visit `http://localhost:8000`.

## 📜 License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
