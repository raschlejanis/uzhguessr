# Photo MCQ Game

A small browser game: see a photo → pick the correct answer out of five options. A game session has 5 rounds.

## Live Demo (after you enable GitHub Pages)
Your site will be published at `https://<your-username>.github.io/<repo-name>/` once you enable GitHub Pages (see below).

## How to add your content
1. Put your images in **/images** (e.g., `images/cat.jpg`).
2. Edit **/data/questions.json** and add one object per image: `{ "image": "images/cat.jpg", "answer": "Cat" }`.
3. Open your published page and play.

## Local preview (optional)
If you just double-click `index.html`, some browsers block `fetch` for local files. You can either:
- Run a tiny local server: `python3 -m http.server 5173` then visit `http://localhost:5173/`, or
- Use this build as-is (it includes a small embedded dataset fallback).

## Deploy to GitHub Pages
1. Create a new repository on GitHub (e.g., `photo-mcq-game`).
2. Upload all files in this folder.
3. Go to **Settings → Pages**.
4. Under **Build and deployment**, set **Source** to **Deploy from a branch**.
5. Set **Branch** to **main** and **/ (root)**, then **Save**.
6. Wait 30–90 seconds. Your site URL appears at the top of the Pages screen.

## Embed in Wix
Use an **Embed → Embed a site** element and paste your GitHub Pages URL, e.g.:
```
https://<your-username>.github.io/<repo-name>/
```
Resize the frame to about 900×700.

## Configuration
- Rounds per game: `ROUNDS` in `app.js` (default 5).
- Options per question: `OPTIONS_PER_QUESTION` in `app.js` (default 5).

## Notes
- Keep answer labels distinct to avoid duplicates in wrong options.
- Works offline (fallback data), but JSON + images must be on the server for your real content.
