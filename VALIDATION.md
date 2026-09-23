# Redesign validation — September 23, 2026

## Browser and layout

Checked with headless Google Chrome through Playwright against a local HTTP
server supporting video byte ranges.

- No page overflow at 320, 390, 600, 768, 1024, 1025, 1100, 1200, or 1440 CSS pixels.
- Supporting text increased from 14 px to 18.2 px (30%). Body styles below
  that size were raised to the same minimum; mathematical superscripts retain
  their natural scale. Navigation, labels, controls, and section markers were
  checked with the larger type on desktop and phone layouts.
- Desktop and phone views visually inspected, including hero, architecture,
  paired humanoid demos, hardware section, and results tables.
- Mobile menu opens, closes on navigation, and dismisses with Escape.
- Four architecture tabs, three hardware-size tabs, and three results tabs
  expose the correct panels and support arrow keys, Home, and End.
- Direct component URLs and component links reveal the associated panel.
- Every architecture figure loads and opens in a native dialog; Escape closes
  it and returns focus to the opener. Controls do not obscure scientific labels.
- Transcript and disclosure sections open and close correctly.
- All content and result panels remain available with JavaScript disabled.
- No JavaScript or browser-console errors in the tested flows.

## Media and resources

- 26 native video players: one supplementary film and 25 individual demos.
- No video autoplay or video-data preloading on initial page load.
- Both humanoid pairs and all three hardware-size pairs play, pause, and restart.
- Switching a hardware tab pauses the hidden pair. Off-screen or closed-panel
  players pause, as do players when the browser tab is hidden.
- Film metadata: 179 seconds, 1920×1080, English caption track present.
- All four chapter shortcuts seek correctly, including before metadata loads.
- Caption cues load; transcript matches the supplied current narration.
- Every local video, poster, figure, PDF, CSV, stylesheet, script, font, and anchor
  resolves successfully. The page makes no third-party runtime asset requests.
- CSS and JavaScript URLs use content hashes to prevent stale cached resources
  from being mixed with the redesign.

## Accessibility

Axe-core 4.10.3, WCAG 2 A/AA and WCAG 2.1 AA rules:
**zero detected violations at 1440 px and 390 px** after fixing contrast in
inherited muted labels. This automated result is supplemented by manual
keyboard, focus-restoration, reduced-motion, and no-JavaScript checks; it is
not a claim of exhaustive accessibility certification.

## Content and data

- Current paper title, method names, setup, and claims checked against active
  manuscript LaTeX and the current supplementary slides.
- Benchmark table: 13 HumanoidBench tasks and four DMControl tasks, all six
  method columns. CSV and JSON agree across all 102 mean/SD pairs.
- Hardware table: training size, both unseen sizes, and pooled unseen-size
  results for both methods (eight rows).
- Best-seed humanoid success remains explicitly labeled and is distinguished
  from the 19% mean success and from TAR.
- Hardware success is reported as observed success; pose errors and completion
  steps are identified as successful-trial-only statistics.
- Hurdle leave-one-out results preserve the improvement without MTD.
- Main benchmark retains the 200K warmup; 750K is discussed as a sensitivity study.
- Current manuscript PDF builds to eight pages without unresolved references
  or citations. Only the temporary bibliography copy was deduplicated.
- The old public code URL returned HTTP 404. No placeholder paper or code links
  remain; code availability is explicitly marked as forthcoming.
- `git diff --check` passes.

## Manuscript-aligned editorial revision

The opening, mechanism explanations, demonstration captions, hardware narrative,
results commentary, and conclusions were reviewed against the active manuscript
and supplementary slide terminology. See `CONTENT_REVIEW.md` for claim mapping.

- Removed repeated trial bookkeeping and editorial/process notes from the main
  narrative; consolidated essential protocol details in the results disclosure.
- Kept every table body, all 26 video sources, and the film transcript unchanged
  from the completed redesign before the editorial revision.
- Retained best-seed versus mean success, observed hardware success, uncertainty,
  task-dependent ablations, and the evaluated-backbone boundary.
- Rechecked the revised copy at 320, 390, 600, 768, 1024, and 1440 CSS pixels,
  including expanded evaluation and future-directions disclosures: no page overflow.
- Visually inspected refreshed desktop and mobile captures, including full
  mechanism names and the new take-home section. No browser page errors.

The parent workspace's code-review graph did not index this website. Graph
queries and change review were therefore supplemented by direct source review
and actual browser checks rather than treating empty graph results as coverage.

## Final publication review

- Removed the personal-site attribution from the page and repository documents;
  retained the upstream Nerfies attribution, website license, and font licenses.
- Scanned all publishable text for personal identifiers, local home paths,
  credentials, and author trailers. No matches remained.
- Checked PDF text, document metadata, embedded files, and external links;
  current PDF author metadata is empty or `Anonymous Authors`. Current bitmap
  assets contain no EXIF data. Video metadata contains no personal author name.
- Visually reviewed 27 sampled frames across all nine real-robot clips and one
  frame from each of the 17 supplementary-film slides. No faces or identifying
  lab labels were found in those inspected frames.
- Independently compared all 102 benchmark mean/SD pairs and eight hardware
  rows against the active LaTeX, CSV/JSON exports, and HTML tables. Values agree.
- Confirmed the manuscript's mechanism definitions, unchanged backbone,
  observed hardware success, seed variability, and conditional ablation findings.
- Retired 307 unused legacy files, including outdated result exports and a
  hardware slide with inconsistent trial counts, plus the obsolete embedded
  code bundle. All 26 current videos and every linked resource remain available.
  Individual demo clips have no audio
  tracks; the supplementary film uses the supplied synthetic narration.
- Re-ran complete browser checks after cleanup: native media playback, captions,
  tabs, figure dialogs, keyboard navigation, downloads, no-JavaScript content,
  six viewport widths, and console errors. All checks passed.
- Publishing uses a repository-specific SSH deploy key; commit author and
  committer metadata are explicitly anonymous. The key's private half stays
  inside Git metadata and is never included in the website commit.
- The public main branch starts from one anonymous release commit. Personal
  contributor identities and automated-assistant author credits are absent
  from the release metadata and published source.

This records the checks performed, including the sampling limit of the visual
media review; it is not a guarantee against identification through inference.
