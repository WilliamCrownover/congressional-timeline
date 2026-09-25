# Congressional Timeline
A timeline of all the past and current United States representatives, senators, and presidents/vice presidents, visualized by seat, state, party, gender, and age.

**Live site:** https://williamcrownover.github.io/congressional-timeline/

## Running locally
This app fetches JSON/image files with `fetch()`, so it must be served over HTTP - opening `index.html` directly via `file://` will fail. From the project root, run a static server, for example:

```
npx serve .
```
or
```
python -m http.server
```

Then open the printed local URL in your browser.

## Data sources
- `current-congress.json` / `presidential-data.json` - congressional and presidential biographical/term records (bioguide, govtrack, wikidata IDs; names; terms; party affiliations).
- `images/*.jpg` - member portraits, downloaded via `portrait-downloader.html` from [bioguide.congress.gov](https://bioguide.congress.gov) (US government work, public domain) with a Wikipedia/Wikipedia Commons fallback for members missing an official portrait. Wikipedia-sourced images may carry their own licenses/attribution requirements - if you plan to redistribute this dataset beyond internal sharing, spot-check the Wikipedia-sourced portraits before doing so.
- Portraits in this repo are resized to ~200px (the largest size actually displayed by the UI) to keep the repository small; `portrait-downloader.html` can be used to fetch full-resolution replacements if needed.

## Tools
- `portrait-downloader.html` - a standalone utility for finding and downloading missing member portraits.
