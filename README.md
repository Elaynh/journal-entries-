# Mood Log

A guided daily journal for all aspects of my life: mood, mind, body, sleep, movement, spirit, and free writing.

## What's inside

- **Today:** a daily check-in. It starts with your nervous system state (safe & connected, mobilized,
  or shut down), your window of tolerance, and your glimmers and triggers. Then come mood ratings,
  feelings, mind, body, movement, spirit, and free writing.
- **Wisdom for today:** a philosopher card chosen for the state you checked in with (Stoics, Taoism,
  Buddhism, existentialists, Rumi, and more), with a small practice and space to respond.
- **Regulate:** short guided practices (breathing, orienting, butterfly hug, and more). You rate how
  settled you feel before and after, and "What works for you" ranks the practices by how much they
  actually help.
- **Look back:** past entries and simple patterns.

It's an installable web app (PWA). It works offline, and entries are saved privately on the device. Nothing is sent anywhere.

## Files

| File | What it is |
| --- | --- |
| `index.html` | The whole app: layout, styles, and logic. Most edits happen here. |
| `manifest.webmanifest` | App name, colors, and icons used when it's installed |
| `sw.js` | Service worker that lets the app open offline |
| `icons/` | Home-screen icons |

## Run it locally

```sh
python3 -m http.server 8000
```

Then open http://localhost:8000.

## Put it on your phone

1. Host it. The easiest way is **GitHub Pages**: in the repo on GitHub, go to **Settings → Pages**, choose
   "Deploy from a branch", pick `main` and `/ (root)`, and save. You'll get a URL like
   `https://<username>.github.io/journal-entries-/`.
2. Open that URL on your phone.
   - **iPhone (Safari):** Share → **Add to Home Screen**
   - **Android (Chrome):** ⋮ menu → **Install app**

## Your data

- Entries live in the browser storage of the device where you write them. They don't sync between devices.
- Use **Export journal** for backups, or to move your journal to another device. **Import** merges a file
  into what's already there and skips entries it already has.
- Clearing your browser's site data for the app also deletes your entries, so export now and then.

## After editing

When you change `index.html`, bump `CACHE` in `sw.js` (e.g. `mood-log-v1` → `mood-log-v2`) so installed
copies pick up the new version.
