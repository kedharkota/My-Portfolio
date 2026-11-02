# Reproducibility and visual sources

## Run the portfolio

Serve the repository with Python 3 and open http://localhost:8000:

```bash
python -m http.server 8000
```

The complete application and content are embedded in `index.html`. No build, package installation, API key, model, or database is required. Google Fonts may load over the network; fallback fonts work without it. The interactive graphics use browser-native canvas and CSS. Browser local storage retains theme and motion preferences when available.

## Verification scope

The redesign retained the original eight project entries, profile panels, three education records, two IEEE publication links, grades, and contact details. The original content was extracted into structured data before restyling. Research and achievement claims remain author-provided and were not independently certified.

Browser QA exercised desktop and phone layouts, theme and accent persistence after reload, motion controls, project filters, desktop grid/list switching, project dialogs, profile tabs, and mobile navigation. JavaScript syntax and HTML content/structure checks were also run. Browser error logs were empty during the exercised flows.

Email and WhatsApp actions prepare messages in external apps; final sending was not performed during QA. This site has no message backend.

## Visual provenance

| Visual | Source and interpretation |
| --- | --- |
| [Current portfolio preview](../portfolio-preview.jpg) | Browser screenshot of the redesigned HTML served locally, captured during desktop QA on 2026-11-03. |
| Orbital scene and project illustrations | Original procedural canvas/CSS/SVG visuals embedded in `index.html`; illustrative, not experiment evidence. |
| [Previous preview](assets/preview.png) | Historical screenshot of the portfolio before the redesign, captured 2026-11-02. |
| [Previous workflow](assets/overview.svg) | Historical explanatory illustration of the earlier gateway-based interface. |

The previous asset inventory, [assets/sources.json](assets/sources.json), describes the historical documentation assets. The current README uses the new root-level preview.

## Documentation checks

```bash
python tools/check_docs.py
```

The standard-library checker validates local documentation link destinations and image headers. It does not request external links, evaluate model accuracy, or reproduce the projects described in the portfolio.
