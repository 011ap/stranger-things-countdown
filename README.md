# ðŸŒ‘ stranger-things-countdown
### **Last ride.**

> *A countdown to Hawkins' final chapter. Where every second brings us closer to the Upside Downâ€¦ and the end of an era.*

---

<p align="center">
  <img src="https://img.shields.io/badge/theme-stranger%20things-E50914?style=for-the-badge&logo=netflix&logoColor=white" alt="Stranger Things Theme">
  <img src="https://img.shields.io/badge/countdown-active-red?style=for-the-badge&logo=hourglass&logoColor=white" alt="Countdown Active">
  <img src="https://img.shields.io/badge/vibes-neon%20%26%20mysterious-000000?style=for-the-badge&logo=ghost&logoColor=E50914" alt="Neon Vibes">
</p>

---

## ðŸ”¦ Into the Upside Down

This project is a **Stranger Things Season 5 finale countdown**â€”a real-time ticker that captures the tension, nostalgia, and mystery of Hawkins' last ride. 

Built with passion for the show. Styled with retro neon. Designed to feel like stepping into 1986... or maybe something darker.

**Features:**
- â±ï¸ **Live countdown timer** â€“ Days, hours, minutes, seconds to the finale
- ðŸŽ¨ **Neon aesthetic** â€“ Pure black background + Netflix red branding
- ðŸ–±ï¸ **Interactive streaming button** â€“ Direct link to watch on Netflix
- ðŸ“± **Responsive design** â€“ Works on desktop, tablet, mobile
- ðŸŒ™ **Dark mode native** â€“ Hawkins vibes 24/7

---

## ðŸš¨ Quick Start

### View the Countdown (Live)
Simply visit the deployed link and watch the clock tick toward destiny.

### Run Locally
```bash
# Clone the repository
git clone https://github.com/011ap/stranger-things-countdown.git
cd stranger-things-countdown
# stranger-things-countdown

A small, single-file countdown to the Stranger Things Season 5 finale — styled with a neon / Netflix aesthetic.

Badges: theme, countdown status, vibes. (Decorative)

---

## Summary

Lightweight, no-build countdown built as a single `index.html`. It shows days, hours, minutes, and seconds until the release and includes a Netflix-style visual theme and responsive layout.

**Highlights:**
- Live countdown with smooth updates
- Retro / neon styling inspired by Stranger Things
- Single-file distribution: `index.html` contains HTML, CSS, and JS

---

## Quick start

View the countdown locally (two easy options):

- Open the file in your desktop browser:

```bash
# On Linux desktops
xdg-open index.html

# macOS
open index.html

# Windows (PowerShell)
start index.html
```

- Or run a tiny static server (recommended for consistent behavior):

```bash
# Python 3
python -m http.server 8000
# then open http://localhost:8000 in your browser
```

No build step required.

---

## Project structure

```
stranger-things-countdown/
├─ index.html        # Main interface (HTML + embedded CSS + JS)
└─ README.md         # This file
```

Everything is bundled in `index.html` for simplicity and portability.

---

## How it works

- The page calculates the time remaining until a configured release timestamp and updates the UI every second.
- The release timestamp is defined in `index.html` (variable `releaseDate`).
- When the timer reaches zero, the UI shows the finished state.

Tip: the current release shown in the UI is `November 27, 2025 • 6:30 AM IST`.

---

## Customization

- Change the target date/time: edit `releaseDate` inside `index.html` (look for a line like `const releaseDate = new Date('2025-11-27T06:30:00+05:30').getTime();`).
- Change visuals: update CSS variables near the top of the embedded `<style>` in `index.html` (colors, glow, spacing).
- Add or remove buttons, links, or text directly in `index.html` — the project is intentionally small and editable.

---

## Accessibility & improvements

Suggestions for contributors:

- Improve keyboard navigation and ARIA attributes
- Add a reduced-motion option for users who prefer no animations
- Provide localization for different timezones and formats

If you want to contribute, open an issue or submit a PR.

---

## License

This project is MIT licensed. See `LICENSE` if you add one — otherwise consider this permissive.

---

## Credits

- Inspired by: Stranger Things (Netflix)
- Built with: plain HTML, CSS, and JavaScript

---

If you'd like, I can also:

- add a short example showing exactly which lines to edit for the date/time
- add a tiny `LICENSE` file with the MIT text

Replace or remove any references to Netflix/Stranger Things branding where required by copyright or trademark policies.

---

**Where to change the release date (exact lines)**

Open `index.html` and look for the `releaseDate` definition in the embedded `<script>` near the bottom of the file. You should see a comment and a line like this:

```html
// Release date: November 27, 2025, 6:30 AM IST
const releaseDate = new Date('2025-11-27T06:30:00+05:30').getTime();
```

Edit the ISO timestamp inside `new Date('...')` to change the target date/time. Keep the `getTime()` call — only replace the date string.

---

**Automated preview (GitHub Pages)**

You can publish this repository as a public website using GitHub Pages. Two easy options:

- Quick (manual): In your repository settings -> Pages, set the source to the `main` branch and root (`/`). GitHub will serve `index.html` at:

  `https://<your-username>.github.io/<repo-name>/`

- Automated (workflow): I added a GitHub Actions workflow that builds and publishes the repository to the `gh-pages` branch on every push to `main`. This makes the site update automatically when you push changes.

The workflow file is at: `.github/workflows/deploy.yml` (created by the project).

After the first successful deployment, the site will be available at:

  `https://<your-username>.github.io/<repo-name>/`

Replace `<your-username>` and `<repo-name>` with your GitHub username and repository name (for example `011ap/stranger-things-countdown` → `https://011ap.github.io/stranger-things-countdown/`).

Steps to publish and make the site public:

```bash
# Commit files (if you haven't already)
git add .
git commit -m "Add GitHub Pages deploy workflow and README notes"
git push origin main
```

Then go to your repository on github.com -> Settings -> Pages and ensure the site is set to use the `gh-pages` branch (or the `main` branch if you prefer the manual option). If the repo is public, anyone visiting the Pages URL will see the countdown.

---

**What is a `LICENSE` file and why it matters**

A `LICENSE` file declares how others may use, modify, and distribute your code. Without a license, the default legal position is "all rights reserved" in many jurisdictions — people cannot legally reuse your code. Adding an open license (like MIT) makes your intent explicit and allows others to fork, reuse, or remix the project under the terms you choose.

Common choices:
- MIT: Permissive — reuse allowed with attribution.
- Apache-2.0: Permissive with grant of patent rights.
- GPL-3.0: Copyleft — derivatives must use same license.

If you want, I can add an `LICENSE` file with the MIT text for you.
---
