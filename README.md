# mserhal.github.io

Personal academic website of **Mira Serhal**, served by GitHub Pages at
**https://miraserhal.github.io**.

Plain HTML/CSS/JS — no build step. Any change pushed to `main` goes live
automatically within a minute or two.

## How to update things

### Replace the CV or add a paper PDF
Overwrite `files/CV.pdf` with a newer version (keep the same filename), then
commit and push. Paper PDFs go in the `papers/` folder — in `index.html`,
each paper card has a commented-out "Paper (PDF)" button ready to uncomment
once the PDF exists.

```
git add -A
git commit -m "Update CV"
git push
```

### Add a paper / presentation / course
All content lives in `index.html`, organized into commented sections
(`<!-- ===== RESEARCH ===== -->` etc.). To add an entry, copy an existing
block and edit the text:

- **Paper**: copy a whole `<article class="paper-card">...</article>` block.
- **Presentation**: copy a `<li class="timeline-item">...</li>` line
  (add a new `<div class="timeline-year">` + `<ul class="timeline-list">` for a new year).
- **Course**: copy a `<li>` inside the relevant `teach-list`.

### Replace the photo
Overwrite `assets/headshot.jpg` with your own portrait (roughly 320×447 or
any similar portrait ratio; the CSS crops it into the frame).

### Change colors / fonts
Edit the CSS variables at the top of `css/style.css` (`:root` for light
mode, `[data-theme="dark"]` for dark mode).

## Layout

```
index.html      all page content
css/style.css   design (light/dark themes via CSS variables)
js/main.js      interactions (scrollspy, animations, accordions, theme toggle)
assets/         headshot, favicon
papers/         self-hosted paper PDFs
files/          CV
404.html        not-found page
```
