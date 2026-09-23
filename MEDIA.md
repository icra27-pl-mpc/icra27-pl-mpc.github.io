# Content and media provenance

## Sources

The authoritative source package contains the active manuscript and
supplementary presentation. The relevant source files are:

- `manuscript/preamble.tex`: current paper title and terminology.
- `manuscript/sections/00_abstract.tex`, `01_introduction.tex`,
  `02_preliminaries.tex`, `03_method.tex`: motivation, architecture, mechanisms.
- `manuscript/sections/04_experiments.tex`: 13 HumanoidBench and four DMControl
  tasks, leave-one-out study, best-seed success, and warmup sensitivity.
- `manuscript/sections/05_real_robot.tex`: setup, training, hardware protocol,
  per-size and pooled results.
- `slides/story-v6.json`, `slides/README.md`, `slides/terminology-review.md`:
  current 17-slide presentation and exact narration.
- `slides/related-work-sources.md`: source-checked comparison of TD-M(PC)²,
  BMPC, BOOM, and PO-MPC.

The root and extended PDFs originally included in that source package had an
older title. `static/paper/pl-mpc.pdf` was rebuilt from the current LaTeX in a
temporary directory. A duplicate `wen2024foundationpose` bibliography entry
was removed only from the temporary build so BibTeX could complete. The source
manuscript was not modified. Final output: eight pages, no unresolved citations
or references.

## Film and diagrams

- `static/video/pl-mpc-overview.mp4` is an unchanged copy of
  `video/Beyond-Policy-Alignment-179s.mp4`: 1920×1080, 179 seconds, English
  narration, 25 moving demonstration clips. The source README identifies the
  narration as the synthetic Kokoro `af_heart` voice.
- The `.vtt` captions are converted from `video/narration.srt`.
- The transcript uses the current `slides/story-v6.json` verbatim.
- `static/paper/pl-mpc-slides.pdf` is an unchanged copy of the final slide PDF.
- `planning-loop.webp`, `mtd.webp`, `ate.webp`, and `rad.webp` are rendered
  excerpts of slides 6–9 at 2.5× resolution. Scientific colors are preserved.
- `video-poster.webp` is rendered from slide 14, the hardware comparison.
- `hardware-setup.webp` comes from `slides/assets/setup-hardware.png`.
- `architecture.webp` is a web export of the complete manuscript figure.
- Poster images derive from the slide package's existing clip posters.

## Demonstrations

The page includes the film plus 25 individual original clips:

| Group | Clips | Presentation |
| --- | ---: | --- |
| Balance-hard | 2 | PL-MPC success and baseline failure |
| Hurdle | 2 | PL-MPC success and baseline failure |
| Other HumanoidBench tasks | 6 | Run, crawl, balance-simple, pole, slide, sit-hard |
| Main hardware comparisons | 6 | Three sizes; both methods succeed in the shown size-1 trials |
| Additional PL-MPC hardware trials | 3 | Two training-size trials and one unseen-size trial |
| Simulation insertion comparisons | 6 | Original scenes 1, 3, 4; scene 4 includes baseline success |

Standalone videos play at the original file speed. The supplementary film
retains its displayed acceleration factors. The humanoid and hardware sections
identify the clips as representative executions; reported success percentages
come from the evaluation. Pair labels show the method and outcome, with original
playback speed below each pair. Sample counts and evaluation protocol are
consolidated with the results rather than repeated throughout the galleries.

## Results

The 17-task benchmark CSV and JSON were extracted from the active LaTeX table,
excluding commented historical tables. HTML cells use the same values.
Hardware rows are transcribed from the active hardware table, including
95% Wilson confidence intervals and successful-trial-only metrics.
The old website's broader task tables, older/digitized baseline figures, and
outdated hardware slide have been removed from the published checkout. The
current page and downloads use the active manuscript.

Reported best-seed success is 50.9% on balance-hard and 58.0% on hurdle;
mean success across three seeds is 19% on each. Matching baseline seeds have
0% success. TAR and environment success are not interchangeable.

The obsolete embedded code bundle from the earlier site has been retired from
the published checkout. No current method repository is linked; the page marks
the code release as forthcoming.
