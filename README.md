# PL-MPC — Beyond Policy Alignment

Static project page for **Beyond Policy Alignment: Closing the Planning–Learning
Loop for Robot Control with Learned World Models**.

A static research page with locally hosted fonts, figures, and media.
Scientific content follows the current manuscript and the 17-slide,
179-second supplementary presentation prepared on September 23, 2026.
The paper is under review at ICRA 2027; author information remains anonymous.

## Preview

```bash
python -m http.server 8000
```

Visit `http://localhost:8000`. GitHub Pages serves the repository root;
no package installation or build step is required. A server supporting byte
ranges is useful for testing video seeking before the complete file downloads.

## Editing

- `index.html`: complete semantic page content and result tables.
- `static/css/index.css`: research-page presentation system.
- `static/css/pl-mpc.css`: PL-MPC layouts, responsive rules, accessibility refinements.
- `static/js/app.js`: mobile menu, keyboard-accessible tabs, video chapters,
  paired playback, and figure dialog. No runtime dependencies.
- `static/data/benchmark.csv` and `.json`: 17 current benchmark tasks.
- `static/data/hardware-results.csv`: per-size and pooled hardware results.
- `static/video/pl-mpc-overview.mp4` and `.vtt`: narrated film and captions.
- `static/paper/pl-mpc.pdf`: paper rebuilt from current manuscript LaTeX.
- `static/paper/pl-mpc-slides.pdf`: static supplementary presentation.
- `static/images/`: slide-derived figures, local poster frames, and favicon.
- `static/data/videos/` and `static/videos/real/`: original demonstration clips.

Keep visible result tables and downloadable data in sync. Benchmark cells
are TAR mean ± SD; humanoid best-seed success must remain explicitly labeled.
Hardware completion steps and pose errors summarize successful trials only.

The film and 25 individual demonstrations use native controls and no autoplay.
All tab content remains readable without JavaScript. All fonts and runtime
assets are local. Obsolete slides, result exports, and unused assets have been
removed from the published checkout. The public branch contains the current
anonymous release.
The earlier embedded code bundle has also been retired; the page explicitly
marks the current code release as forthcoming.

See `CONTENT_REVIEW.md` for narrative and claim alignment, `MEDIA.md` for source
provenance, `VALIDATION.md` for checks, and `NOTICE.md` for attribution and licensing.
