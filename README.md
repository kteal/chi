# Chi 🎲

**Chi** is a mobile-first statistical tracker for Catan (2d6) dice rolls. It uses a **Chi-Square Goodness of Fit** test to mathematically verify if your dice are "fair" or if they are behaving suspiciously.

Designed with an **iOS-native aesthetic**, it provides a smooth, haptic-style experience for tracking games in real-time.

## ✨ Features
- **Real-time Distribution:** A dynamic bar chart showing the frequency of every roll (2-12).
- **Statistical Engine:** Calculates the $\chi^2$ statistic and the exact **p-value** (likelihood) for 10 degrees of freedom.
- **Roll History & Editing:** Scroll through your recent rolls. Tap any roll to edit its value if you made a mistake.
- **Game Archive:** Save completed games to a local archive (stores the last 5 games). Supports **swipe-to-delete** for easy management.
- **System Theme Support:** Perfectly mirrors your device's theme (Light/Dark mode) including browser UI integration.
- **Local Persistence:** Data is automatically saved to your browser's `localStorage`. Refreshing or closing the tab won't lose your game.
- **Privacy First:** No backend, no cookies, no tracking. Your dice data never leaves your device.
- **Mobile Optimized:** Zero tap delay and disabled double-tap zoom for high-speed tracking during intense games.

## 📊 The Statistics
Chi evaluates your rolls against the theoretical triangular distribution of two 6-sided dice:
- **Total Degrees of Freedom:** 10 (11 possible outcomes minus 1).
- **Critical Value:** 18.31 (at $\alpha = 0.05$).
- **p-value:** The probability that a perfectly fair set of dice would produce a distribution at least as extreme as yours. A $p < 0.05$ (5% likelihood) is generally considered "Suspicious."

*Note: Statistical analysis requires at least 15 rolls to minimize small-sample errors.*

## 🛠 Tech Stack
- **Frontend:** Vanilla HTML5, CSS3, and JavaScript (ES6+).
- **Visualization:** [Chart.js](https://www.chartjs.org/) via CDN.
- **Styling:** iOS-inspired native CSS (Apple system fonts, squircle targets).
- **Deployment:** GitHub Pages.

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
