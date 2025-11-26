<p align="center">
  <img src="assets/banner.svg" alt="Stranger Things Countdown" width="980" />
</p>

<p align="center">
  <a href="https://011ap.github.io/stranger-things-countdown/" target="_blank">
    <img src="https://img.shields.io/badge/VIEW%20THE%20COUNTDOWN-Visit%20Now-E50914?style=for-the-badge&logo=netflix&logoColor=white" alt="View the countdown" />
  </a>
</p>

---

## Into the Upside Down

This project is a single-file, neon-styled countdown that shows days, hours, minutes and seconds until the Season 5 finale. The README includes a hero banner (above) — replace `assets/banner.svg` with your own image or video for the full effect.

**Quick highlights:**
- Live countdown timer — Days / Hours / Minutes / Seconds
- Neon, retro styling and responsive layout
- No build step — `index.html` is the whole app

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

## Make the README pop (add your video or banner image)

Want the README to look like a cinematic poster? Two options:

1) GIF / static banner (easy)

Place your image/gif in `assets/banner.gif` (or `assets/banner.jpg`) and the top of this README will show it automatically. Example markup (already used above):

```md
<p align="center">
  <img src="assets/banner.gif" alt="Countdown banner" width="980" />
</p>
```

<p align="center">
  <a href="https://011ap.github.io/stranger-things-countdown/" target="_blank">
    <img src="assets/Stranger_Things_neon_red_logo_in_retro_ITC_Benguiat_style.png" alt="Poster" width="520" style="max-width:100%;height:auto;" />
  </a>
</p>

<!-- Animated SVG fallback shown inline in README; works on GitHub and Pages -->
<p align="center">
  <img src="assets/banner-anim.svg" alt="Animated banner" width="520" style="max-width:100%;height:auto;" />
</p>

Click the image (or visit the Pages URL) to see the full hero video on the live site — GitHub README does not reliably autoplay videos, but the Pages site will.

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

## Shareable link (what to send to everyone)

After the workflow completes your site will be available at:

```
https://011ap.github.io/stranger-things-countdown/
```

Share that link and anyone can view the live countdown.

---

## Troubleshooting: "Permission to ... denied to github-actions[bot]"

If your workflow fails with a message like "Permission to <owner>/<repo>.git denied to github-actions[bot]", it's because the workflow's runner (the GitHub Actions bot) doesn't have permission to push the `gh-pages` branch. Fixes:

1) Allow Actions to write to the repository (recommended):

  - Go to your repo on github.com -> Settings -> Actions -> General
  - Under "Workflow permissions", select **Read and write permissions** (instead of Read repository contents only)
  - Click "Save"

2) If you have branch protection rules that prevent the bot from pushing to `gh-pages`, either relax those rules for the `gh-pages` branch or choose the manual Pages source (main branch) in Settings -> Pages.

3) If you prefer using a personal token (works even if repo-level workflow write access is restricted), create a Personal Access Token (classic) with `repo` scopes, then add it as a secret named `GH_PAGES_DEPLOY_TOKEN` in Settings -> Secrets -> Actions. Update `.github/workflows/deploy.yml` to use `token: ${{ secrets.GH_PAGES_DEPLOY_TOKEN }}` instead of `GITHUB_TOKEN`.

After changing the workflow permissions or adding the token, push a small change to `main` to re-run the workflow.


**What is a `LICENSE` file and why it matters**

A `LICENSE` file declares how others may use, modify, and distribute your code. Without a license, the default legal position is "all rights reserved" in many jurisdictions — people cannot legally reuse your code. Adding an open license (like MIT) makes your intent explicit and allows others to fork, reuse, or remix the project under the terms you choose.

Common choices:
- MIT: Permissive — reuse allowed with attribution.
- Apache-2.0: Permissive with grant of patent rights.
- GPL-3.0: Copyleft — derivatives must use same license.

If you want, I can add an `LICENSE` file with the MIT text for you.
---
