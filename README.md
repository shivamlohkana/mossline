# Mossline — Measure the Living Planet

A single-file, scroll-driven landing page for **Mossline**, a fictional environmental-data company.

The page is one long pinned scroll story:

1. **Hero** — a floating moss island in a misty sky, with ferns growing in front of the headline.
2. **Fly-in** — scrolling scrubs a cinematic video as the camera pushes into the island and lands at eye level facing a sensor mast. Two floating rocks fly past and the vision statement resolves out of blur.
3. **Landscape** — an accounting paragraph writes in word by word and four lime hotspots pop up on the moss, while a fog bank rolls in.
4. **Station** — a glass "Accumulated carbon balance" card with a count-up and a drawing sparkline, plus a five-row feature list.
5. **Solutions** — a white panel slides up with three tilting image cards and count-up stats.

## How it works

- Plain HTML, CSS and vanilla JS in one file — no libraries, no build step.
- The fly-in video plays once on load while every frame is cached as a JPEG blob; a canvas then draws the cached frame that matches the scroll position, so scrubbing is smooth in both directions.
- A high-res still and a transparent cut-out of the island hand off to video frame 0 without a visible jump.
- One `requestAnimationFrame` loop drives everything from smoothed scroll progress and pointer position.

## Run it

Open `index.html` in a browser, or serve the folder:

```bash
python -m http.server 8123
```

Then visit http://localhost:8123.

Imagery and video were generated with Higgsfield.
