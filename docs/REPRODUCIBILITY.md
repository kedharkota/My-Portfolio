# Reproducibility and visual sources

## Scope

This guide describes what is available in the committed project and what is required to reproduce it. The documentation update inspected source and saved outputs; it did not rerun model training or hardware/simulation experiments.

## Required inputs

All page content lives in `index.html`. Before hosting, replace the machine-specific `file:///C:/...` background-image references with committed assets and relative URLs. Those background files are absent from this repository.

## Entry point

Requires Python 3 for the preview server and a modern browser. No Node.js build is required.

```bash
python -m http.server 8000
```

Open http://localhost:8000 and select **Enter Full Portfolio**. Internet access loads the Tailwind CDN, fonts, and icon stylesheet.

## Evidence and interpretation

The screenshot below was captured from the committed HTML served over HTTP. The contact form uses `mailto:` rather than a server-side message service. Research and achievement statements on the page are author-provided portfolio content; this documentation does not independently verify those claims.

## Visual provenance

All screenshots and experiment figures are tied to repository material. Workflow SVGs are explanatory illustrations. The full image inventory is in [assets/sources.json](assets/sources.json).

| Visual | Source |
| --- | --- |
| [overview.svg](assets/overview.svg) | New explanatory project-workflow diagram based on the committed source and documentation; not a screenshot or measured result. |
| [preview.png](assets/preview.png) | Screenshot of committed index.html served over local HTTP at a 1440x1000 viewport; captured 2026-11-02. Database/model integrations were not run. |

## Validation

```bash
python tools/check_docs.py
```

The standard-library checker validates README/docs local link destinations and SVG/PNG/JPEG headers. It makes no external requests and installs no project runtime dependencies. External web links, model accuracy, image semantics, and full application execution need separate review.

## Reproduction record

For a new experiment or demo, record the source commit, environment versions, data provenance and split, configuration, command/notebook order, and resulting artifacts. Only label a measurement as reproduced after completing that run. Keep credentials and restricted datasets outside version control.
