continued at: [[Leavitt Law]]
### Cepheids
Pulsating variable stars. They expand and contract — a heat engine 
driven by the kappa mechanism: a layer of partially ionised helium 
that absorbs energy when compressed and releases it on expansion.

`Star compresses → heats → expands → cools → compresses again.`
Repeats like clockwork. Sawtooth light curve.

`Fast rise = compression, star hottest and smallest, maximum brightness.`
`Slow fall = expansion, star cools, brightness drops.`

### Phase Folding
Raw light curve = years of observations scattered in time.
Phase fold = collapse all cycles onto one using the known period.

**Result: one clean sawtooth shape. All observations from all cycles** 
**stacked on top of each other.**

## A clean Sawtooth
(see plots)


---

### OGLE-LMC-CEP-0227
Cepheid in the Large Magellanic Cloud — 160,000 light years away.
Period: 3.797 days.
Special: inside an eclipsing binary system.
Two signals visible in phase-folded plot:
- Tight upper track = Cepheid pulsation
- Scattered lower points = binary eclipses

Most precisely measured distance to LMC comes from this star — Cepheid pulsation + binary eclipse geometry cross-checked.

### The Leavitt Law
Plotted 2439 LMC Cepheids: log₁₀(period) vs mean magnitude.
**Result: a straight line.**

Longer period = bigger star = less dense = slower pressure waves = 
brighter star. Period-luminosity relationship from first principles:

P ∝ 1/√ρ̄

`Power law → straight line in log space.`  Same trick as convergence 
rate plots in numerical methods.
Why the line is tight: all LMC Cepheids at same distance from us.
No distance scatter. Apparent brightness = true brightness (relative).

## Leavitt's Law: plot from data

(see plots)

### Why it matters
`Measure period → know true brightness → compare to apparent brightness→ get distance.`  Works across the universe.

Hubble used this in 1924 to prove Andromeda was a separate galaxy.
Still used today to calibrate the Hubble constant.

Henrietta Swan Leavitt discovered it in 1908 from photographic plates.
Data before theory. Pattern before explanation.

### Magnitude scale
Counterintuitive: smaller magnitude = brighter. Historical accident 
from ancient Greek astronomers. Magnitude 1 > magnitude 2 in brightness.
Convention: invert y axis so bright stars sit at top of plot.

---

### Data source
OGLE-IV (Optical Gravitational Lensing Experiment)
1.3m Warsaw Telescope, Las Campanas Observatory, Chile
Running since 1992. ~1 billion stars monitored.
LMC Cepheid catalogue: 2439 fundamental mode Cepheids

### Next
- Fit the Leavitt Law line — extract slope and intercept
- Period finding from scratch — Lomb-Scargle periodogram
- Move to other variable star types: RR Lyrae, Miras

