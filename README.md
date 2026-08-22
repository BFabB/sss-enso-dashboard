# Watching ENSO Through Sea Surface Salinity

This repository contains the source files for an experimental web page demonstrating how satellite sea surface salinity (SSS) can be used as an independent indicator of El Niño–Southern Oscillation (ENSO) evolution.

The page is available at:

<https://bfabb.github.io/sss-enso-dashboard/>

## Purpose

The demonstrator focuses on the displacement of the western equatorial Pacific fresh-pool edge, tracked using the longitude of the 34.8-pss isohaline averaged between 2°S and 2°N.

Eastward displacement of this fresh-pool edge is interpreted as an SSS-based signature of El Niño conditions. The indicator is intended as a complementary ocean-salinity perspective alongside established ENSO monitoring systems.

## Status

This page is a scientific demonstrator and work in progress. It is not an operational ENSO product.

The page is developed in the framework of CCI+SSS / C3S-related work and is intended to be updated in near-real time, approximately monthly, as new SSS data become available.

## Repository structure

```text
.
├── _quarto.yml              # Quarto website configuration
├── _variables.yml           # Update dates and shared variables
├── index.qmd                # Main dashboard page
├── methods.qmd              # Methods and scientific basis
├── acronyms.qmd             # Acronym table
├── update-log.qmd           # Page update history
├── assets/
│   ├── animations/          # MP4 animations
│   ├── css/                 # Custom CSS
│   ├── data/                # Supporting data, if provided
│   ├── figures/             # Static figures and poster images
│   └── logos/               # Institutional logos
└── docs/                    # Rendered website published by GitHub Pages
```

## Main assets

The web page includes:

- a recent-evolution dashboard animation;
- a retrospective SSS/ENSO animation from 2010 to present;
- static diagnostics of the SSS-based ENSO indicator;
- comparisons with established ENSO indices;
- methodological notes and caveats.

## Build instructions

The site is built with [Quarto](https://quarto.org/).

From the repository root:

```bash
quarto render
```

The rendered website is written to:

```text
docs/
```

GitHub Pages is configured to serve the site from the `docs/` folder on the `main` branch.

## Updating the site

After updating figures, animations, text, or date variables:

```bash
rm -rf docs
quarto render
touch docs/.nojekyll

git add .
git commit -m "Update SSS ENSO dashboard"
git push
```

GitHub Pages will redeploy the site automatically after the push.

## Scientific caveat

The SSS-based ENSO indicator depends on methodological choices, including the selected isohaline, latitude band, longitude domain, product version, near-real-time data handling, and threshold definition. It should therefore be interpreted as a complementary observational diagnostic, not as an official ENSO classification.

## Credits

Scientific lead: Fabrice Bonjean — LOCEAN

This demonstrator builds on work related to ESA CCI+SSS and the transition toward Copernicus Climate Change Service activities.

## Licence

No explicit licence is currently defined for this repository. Reuse of the material should therefore be discussed with the repository owner.
