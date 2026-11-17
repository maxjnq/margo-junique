# Notes for Claude

This repo is Margo Junique's personal artist website, maintained by Margo herself with Claude's help. Read `README.md` first.

- The whole site is `index.html`: CSS in the `<style>` block, the three.js scene and widget logic in the final `<script>`.
- Hosting is GitHub Pages from the `main` branch root. Pushing to `main` deploys it, so commit and push only when Margo asks.
- Keep it a single static page with no build step. Load any library from a CDN with a pinned version.
- Visual direction: stylized, cel-shaded 3D (soft toon shading, chunky swaying grass, painted clouds) at autumn golden hour, deep blue sky, warm orange and red leaves. Widgets copy iOS home-screen widgets: one neutral frosted-glass style, white text, no brand colors, no drop shadows, equal tile sizes.
- Main scene pieces, in order in the script: sky and clouds, ground, far hills and mountain, trees, villages, grass (custom shader), flowers, props (chair, lamp, mirror), optional 3D figure (`SHOW_MARGO`), autumn tree and falling leaves, camera framing, widgets, render loop.
- The mirror's reflection deliberately renders only the sky (layer 1).
- After changing anything visual, preview it with `python3 -m http.server 4173` and check both a desktop and a phone-sized window.
