- [[R-process Enrichment Analysis — GALAH DR3]]
## Instrument
HERMES spectrograph at the Anglo-Australian Telescope.
Four cameras, four simultaneous wavelength windows.
Resolution R~28000 — high enough to resolve individual absorption lines.

## The Four Cameras

### Blue (B) — 4713 to 4903 Å
- Covers hydrogen H-beta at 4861 Å
- Noisier than red — lower signal to noise in this range
- Some metal lines but not the primary r-process window

### Green (G) — 5645 to 5873 Å  
- **Most important for r-process chemistry**
- Barium II line at 6142 Å — primary Ba abundance tracer
- Europium II line at 6645 Å — primary Eu abundance tracer
- Our star's green camera spectrum unavailable (Survey: other flag)

### Red (R) — 6475 to 6734 Å
- Cleanest spectrum — highest signal to noise
- Hydrogen H-alpha at 6563 Å — deepest line in our spectrum
- Good for radial velocity measurement
- Successfully downloaded for our star

### Infrared (I) — 7585 to 7887 Å
- Heavily contaminated by telluric lines
- Oxygen A-band around 7600 Å — atmospheric absorption forest
- Water vapour emission spikes throughout
- Not useful for stellar chemistry without telluric correction

## Our Star — GALAH 131120002001243
- Red camera: clean, downloaded successfully
- Blue camera: downloaded, noisy
- Green camera: server error — unavailable
- IR camera: downloaded but telluric contaminated

## Key Lines We Wanted to See
| Element | Wavelength (Å) | Camera | Status |
|---------|---------------|--------|--------|
| H-alpha | 6563 | Red | ✓ Visible |
| H-beta | 4861 | Blue | ✓ Visible |
| Ba II | 6142 | Green | ✗ Unavailable |
| Eu II | 6645 | Green | ✗ Unavailable |

## What Telluric Contamination Looks Like
Sharp upward spikes in the IR spectrum — emission from Earth's 
atmosphere, not the star. The oxygen A-band at 7600 Å produces 
a forest of lines that overwhelm stellar features entirely.
Telluric correction requires dividing by a standard star spectrum 
observed at the same airmass.

## Plots
- spectrum_red.png — red camera, clean H-alpha visible
- spectrum_blue.png — blue camera, H-beta visible, noisy
- spectrum_ir.png — IR camera, telluric contamination visible
