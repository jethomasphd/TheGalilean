# The Galilean

A historical inquiry into Jesus of Nazareth, read in stone, coin, papyrus, and light. One page, no build step, no framework.

**Read it:** open `index.html`, or visit the GitHub Pages site for this repository.

## What the page does

- **It moves through the hours of one day.** The palette is a set of CSS tokens selected by the `data-hour` attribute on `<html>`: `museum`, `afternoon`, `dusk`, `night`, `dawn`, `morning`. Scroll position sets the hour. Every photograph is shown in monochrome until the dawn station, when colour is allowed in.
- **It carries a map.** The right-hand panel (a bottom bar on phones) follows the reader through geography and time: a Mediterranean view for Rome and Egypt, the Levant, the lake country, and a schematic plan of Jerusalem in about 30 CE for the last night. Geometry is clipped from Natural Earth public-domain data and inlined in the page; the Jerusalem plan is drawn by hand.
- **Every image is archival.** Museum objects, nineteenth-century glass plates (Salzmann 1854, Frith, Bonfils, the American Colony / Matson collection, Detroit Publishing photochroms), and two paintings. Nothing is machine-generated. Credits and licences are listed at the foot of the page and in `assets/credits.json`.

## Editing

Everything lives in `index.html`:

- The chapters are the `<section class="station">` blocks. Each contains one or more invisible `<span class="loc">` markers whose `data-place`, `data-hour`, `data-when`, `data-year`, and `data-found` attributes drive the map, the timeline, and the palette as the reader passes them.
- Places are defined in the `STATIONS` object near the end of the file; add a place there (with `lon`/`lat` and a `view`) before referencing it from a marker.
- Figures use `<figure class="spec">` with a catalogue line (`.spec-label`), an interpretive caption (`.spec-note`), and a credit. Add `spec--colour` to exempt an image from the monochrome treatment.

## Sources

The inventory of objects, ancient witnesses, and scholarship is at the end of the page, including the items withdrawn since the first edition (the Nazareth Inscription, after Harper et al. 2020) and the corrections adopted (the Giv‘at ha-Mivtar reappraisal, Zias and Sekeles 1985).

— Jacob E. Thomas, PhD
