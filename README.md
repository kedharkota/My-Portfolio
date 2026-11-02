# Kota Kedharnadh · Developer Portfolio

An interactive portfolio for AI, data science, and robotics projects.

**HTML · CSS · JavaScript · Tailwind CSS**

[![Documentation checks](https://github.com/kedharkota/My-Portfolio/actions/workflows/docs.yml/badge.svg?branch=main)](https://github.com/kedharkota/My-Portfolio/actions/workflows/docs.yml)

[Overview](#overview) · [Getting started](#getting-started) · [Repository guide](#repository-guide) · [Reproducibility](docs/REPRODUCIBILITY.md)

<p align="center">
  <img src="docs/assets/preview.png" alt="Kota Kedharnadh · Developer Portfolio: project preview" width="900" />
</p>

[Open full-size visual](docs/assets/preview.png)

*Portfolio main view rendered from the repository HTML.*

## Project at a glance

| Detail | Project information |
| --- | --- |
| **Focus** | Interactive project and research portfolio |
| **Start here** | [index.html](index.html) |
| **Run mode** | Static web page; Python HTTP server for local preview |
| **Explore** | Project cards, research links, theme controls, and contact links |

## Overview

A single-page personal portfolio that brings project work, research links, education, and contact options into one browsable interface. The page includes a gateway screen, theme controls, a developer-console interaction, and project detail modals.

## What this project includes

- Gateway and main portfolio views with section navigation.
- Three visual themes: Violet, Cyber, and Indigo.
- Project cards, research links, education timeline, and a command-style profile panel.
- Contact form that opens the visitor's email client, plus GitHub and LinkedIn links.

## Workflow

<p align="center">
  <img src="docs/assets/overview.svg" alt="Project workflow" width="900" />
</p>

[Open full-size visual](docs/assets/overview.svg)

*Explanatory diagram. Detailed implementation and availability notes follow below.*

## Getting started

Requires Python 3 for the preview server and a modern browser. No Node.js build is required.

```bash
python -m http.server 8000
```

Open http://localhost:8000 and select **Enter Full Portfolio**. Internet access loads the Tailwind CDN, fonts, and icon stylesheet.

### Required inputs and current constraints

All page content lives in `index.html`. Before hosting, replace the machine-specific `file:///C:/...` background-image references with committed assets and relative URLs. Those background files are absent from this repository.

## Repository guide

| File | Purpose |
| --- | --- |
| [index.html](index.html) | Complete page, styles, interactions, and project content. |

## Results and project status

The screenshot above was captured from the committed HTML served over HTTP. The contact form uses `mailto:` rather than a server-side message service. Research and achievement statements on the page are author-provided portfolio content; this documentation does not independently verify those claims.

## Next steps

- Commit the referenced background images or remove their local file paths.
- Check navigation, project links, and contact actions on mobile before deployment.

## Documentation maintenance

<details>
<summary>Run documentation checks and maintain visuals</summary>

Local documentation links and image headers are checked on pull requests and relevant pushes by the [documentation workflow](.github/workflows/docs.yml). Run the same check locally:

```bash
python tools/check_docs.py
```

See the [reproducibility guide](docs/REPRODUCIBILITY.md) for evidence, missing artifacts, and visual-source notes. The check validates documentation files; it does not train models or certify application behavior.

</details>

## Explore related projects

- [Video Deepfake Detection](https://github.com/kedharkota/AI-deep-fake-detection)
- [Gesture-Controlled Drone Simulation](https://github.com/kedharkota/Gesture-Controlled-Drone-)

---

[More projects by kedharkota](https://github.com/kedharkota?tab=repositories)
