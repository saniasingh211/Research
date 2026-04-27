# Supernova Neutrino Burst Detection

**Date:** April 2026
**Status:** Complete — first working pipeline
**Tools:** Python, numpy, matplotlib, Jupyter
**Venv:** `particle_physics`

---

## What This Is

A simulation of a supernova neutrino burst detector — built from scratch, cell by cell.

The pipeline mirrors what Super-Kamiokande actually runs:
1. Model the background (quiet detector, no star dying)
2. Model the burst signal (star collapses, neutron star cools)
3. Combine them — this is what the detector records
4. Apply a sliding window filter to detect the burst in the noise

---

## The Physics

When a massive star collapses into a neutron star, it releases ~10⁵⁸ neutrinos in about 10 seconds. Most of the star's energy goes out as neutrinos, not light. The optical supernova you'd see in the sky comes later — the neutrino burst arrives first.

SN1987A (168,000 light years away) gave 24 events across three detectors. A galactic supernova at ~10 kpc would give thousands.

**Burst luminosity curve:**

$$L(t) \propto e^{-(t - t_0)/\tau}$$

Fast rise at $t_0$, exponential decay with timescale $\tau = 3$ seconds. This is the neutron star cooling.

**Background:** Poisson noise at 0.5 events/second — atmospheric neutrinos, radioactive decay in detector walls. Almost always 0 counts per 10ms bin.

---

## The Pipeline

### Time axis
- Bin width: 10ms
- Pre-burst window: 2 seconds (quiet, background only)
- Post-burst window: 15 seconds (burst + background)
- Total: 1700 bins

### Background model
- Rate: 0.5 events/second → 0.005 expected counts per bin
- Sampled from Poisson distribution
- Result: ~9 events across the full window. Sparse. No structure.

### Signal model
- Peak rate: 200 events/second at $t=0$
- Decays exponentially with $\tau = 3$s
- Result: ~607 events. 400x louder than background at peak.

### Detection filter
- Sliding window: 0.5 seconds (50 bins)
- Compute mean count rate in window
- Compare to expected background rate → detection ratio
- Threshold: 10x above background
- Peak ratio achieved: **424x**

---

## Results

| Quantity | Value |
|---|---|
| Background events (total) | 9 |
| Signal events (total) | 607 |
| Peak counts in single bin | 6 |
| Peak detection ratio | 424x |
| Detection threshold | 10x |

The burst is unambiguous. In real detectors the challenge is a weaker signal — either a more distant supernova, or a smaller detector.

---

## What's Simplified

- Real burst profiles are more complex (two-component: neutronisation burst + accretion + cooling)
- Real backgrounds are not flat — they have time-varying structure
- Real detection uses likelihood ratio tests, not just a ratio threshold
- Real neutrino energy spectra matter for detection efficiency (Fermi-Dirac distribution, $T \sim 4$ MeV for electron antineutrinos)
- Real detectors have energy reconstruction, vertex reconstruction, directionality

---

## Next Steps (if revisited)

- [ ] Add Fermi-Dirac energy spectrum to the signal model
- [ ] Replace threshold filter with proper Poisson likelihood ratio test
- [ ] Try with a weaker signal (more distant supernova) — where does detection fail?
- [ ] Look at real IceCube open data

---

## Files

- Notebook: `supernova_neutrino.ipynb`
- Venv: `particle_physics` (numpy, matplotlib, scipy, jupyter)

---

*First particle physics project. Built it from scratch. It works.*
