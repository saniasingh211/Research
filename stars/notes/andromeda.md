### Quick intro

**What we're going to do:**

1. Get Cepheid data from Andromeda — periods and apparent magnitudes already measured by Hubble Space Telescope
2. Plug the periods into your Leavitt Law to get true magnitudes
3. Subtract true from apparent to get the distance modulus
4. Convert distance modulus to light years
5. Get the distance to Andromeda

Period → size. That's the physical content of the Leavitt Law.

And size → luminosity. Bigger star = more surface area = more light emitted.

So the full chain Henrietta accidentally encoded in her straight line:

period→size→luminosityperiod→size→luminosity

Measure one number — how fast it blinks — and you know two things about the star: how big it is and how bright it truly is.

---
## Distance to Andromeda — M31

Used Leavitt Law calibrated on LMC to measure distance to Andromeda.

Star used: M31-V1 — Hubble's original Cepheid in Andromeda.
Period: 31.91 days
Apparent magnitude (I band): 18.5

Steps:
1. Plug period into Leavitt Law → true magnitude = 12.46
2. Distance modulus = apparent - true = 18.5 - 12.46 = 6.04
3. Convert: d = 10^((μ+5)/5) parsecs

**Result: ~5 million light years**

Published value: 2.5 million light years

Why the offset:
- Reddening — dust makes star look dimmer → distance overestimated
- Filter mismatch — LMC calibration vs M31 observation not identical
- Metallicity — M31 Cepheids slightly different composition than LMC

With proper corrections: astronomers get 2.5 million light years at 1% precision.
Right ballpark. Right method. Wrong calibration details.

Distance modulus formula:
μ = 5*log10(d) - 5
d = 10^((μ+5)/5) parsecs