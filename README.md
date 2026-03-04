# Music Timer

A Progressive Web App that acts as a countdown timer for music practice. The timer **only counts down while music is detected** (using the microphone and MediaPipe audio classification), so it effectively measures time spent playing.

## Features

- Set any duration (minutes and seconds)
- Countdown runs only when the classifier detects "Music"
- 5-second grace period: if music stops briefly, the timer keeps running until 5s without music, then rewinds to the value when it stopped
- Alarm when the countdown reaches zero (repeats until you press Clear)
- Works as a PWA: installable, runs in standalone window

## Deploy

The app is deployed to GitHub Pages via GitHub Actions. Every push to `main` triggers a deploy.

- **Live site:** https://gokikamukow.github.io/musictimer/

**First-time setup:** If the repo does not exist on GitHub yet, follow **[SETUP_GITHUB.md](SETUP_GITHUB.md)** to create it and push.

## Local development

Open `music-timer.html` in a browser (Chrome/Edge recommended). For microphone access over `file://` some browsers may require serving the file (e.g. `npx serve .` or `python3 -m http.server 8000`).

## Tech

- Single HTML file, no build step
- MediaPipe Tasks Audio (YAMNet) for music detection
- Web Audio API for microphone and alarm
