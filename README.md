# The Galilean

A historical inquiry into Jesus of Nazareth, read in stone, coin, papyrus, and light. One page, no build step, no framework.

**Read it:** open `index.html`, or visit the GitHub Pages site for this repository.

## What the page does

- **It moves through the hours of one day.** The palette is a set of CSS tokens selected by the `data-hour` attribute on `<html>`: `museum`, `afternoon`, `dusk`, `night`, `dawn`, `morning`. Scroll position sets the hour. Every photograph is shown in monochrome until the dawn station, when colour is allowed in.
- **Every station opens with a map.** Each chapter begins with an archival map of its ground, the chapter's places marked on it, and a timeline mark for its date: Labberton's 1884 atlas sheet of the Roman world, Kent and Madsen's 1912 *Palestine in the Time of Jesus* (Library of Congress) for the Levant and Galilee, its inset plan of Roman-period Jerusalem for the last night, and the sixth-century Madaba mosaic for the tomb. A thin strip at the top of the screen keeps the current place and date in view as you read. Marker positions are percentages of each map image, set in the `MAPS` object near the end of the file.
- **Every image is archival.** Museum objects, nineteenth-century glass plates (Salzmann 1854, Frith, Bonfils, the American Colony / Matson collection, Detroit Publishing photochroms), and two paintings. Nothing is machine-generated. Credits and licences are listed at the foot of the page and in `assets/credits.json`.

## Editing

Everything lives in `index.html`:

- The chapters are the `<section class="station">` blocks. Each opens with a `<figure class="stmap">` whose `data-view`, `data-marks`, and `data-year` attributes draw that chapter's map and timeline mark. Invisible `<span class="loc">` markers inside the text carry `data-place`, `data-hour`, and `data-when`, which update the top strip and the palette as the reader passes them.
- Places are named in the `STATIONS` object near the end of the file, and positioned on each map in `MAPS`; add a place to both before referencing it from a card.
- Figures use `<figure class="spec">` with a catalogue line (`.spec-label`), an interpretive caption (`.spec-note`), and a credit. Add `spec--colour` to exempt an image from the monochrome treatment.

## Sources

The inventory of objects, ancient witnesses, and scholarship is at the end of the page, including the evidence deliberately left out (the Nazareth Inscription, after Harper et al. 2020) and the reappraisals adopted (the Giv‘at ha-Mivtar heel, Zias and Sekeles 1985).

— Jacob E. Thomas, PhD
