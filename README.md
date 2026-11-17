# Margo Junique

The website of Margo Junique, singer-songwriter from Görlitz.

It is a single page: a live 3D meadow from the video for her debut single *Stuck in my mind* (autumn, golden hour, falling leaves), with iPhone-style widgets on the right for her photo, location, music player, bio, contact, socials and releases.

**Live site:** https://maxjnq.github.io/margo-junique

## How it works

Everything lives in `index.html`. No build step, no dependencies to install. The 3D scene uses [three.js](https://threejs.org) (r158), loaded from a CDN.

Any change pushed to `main` goes live automatically within about a minute (GitHub Pages).

## Things you can drop in

These files are optional. The page uses them automatically when they exist next to `index.html`:

| File | What it does |
|---|---|
| `margo.jpg` | Margo's profile picture in the **Photos** widget. Square works best. Until it exists, the widget shows a snapshot of the scene. |
| `track.mp3` | The song for the **Playing now** player. Until it exists, the play button opens the song on Spotify. While it plays, the lamp glows with the music. |

## Settings in `index.html`

Search for these names:

- `EMAIL`: Margo's booking/press email. While empty, the Contact button reads "Email coming soon".
- `PHOTO_URL`, `TRACK_URL`: file names for the photo and song above.
- `SHOW_MARGO`: set to `true` to show a stylized 3D figure of Margo sitting on the chair (hidden for now).

## Edit it with Claude

Open this folder in Claude Code and just describe what you want, for example:

- "Add my new single to the Releases widget"
- "Make the sky pinker"
- "Put my email in the Contact button"

Claude edits `index.html`, and once you push, the site updates.

## Preview locally

```bash
python3 -m http.server 4173
```

Then open http://localhost:4173.
