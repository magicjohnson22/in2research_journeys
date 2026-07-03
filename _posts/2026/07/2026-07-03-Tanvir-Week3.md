---
title: Week 3 - Running Examples & Preparing Outputs
date: 2026-07-03
time: "15:30:00"
author: tanvir
categories: ["learning", "python", "tutorials", "examples"]
layout: post
---

### Highlights From This Week

At last, this week I managed to run some of the S2FFT examples from the already existing documentation.

Although I still didn't fully understand all the mathematical concepts behind the package, I was able to gain a much deeper intuition by actually running the package and varying different parameters and inputs, and observing how the output was affected.

A good starting point was the round-trip test: generating a random bandlimited signal, mapping it to the sphere with the inverse transform, and then transforming it straight back with the forward transform. Checking that the recovered coefficients matched the originals (to near machine precision) was a simple but reassuring way to confirm I had everything set up correctly and that I understood which direction each transform goes.

From there I started varying things to see what happened:
- Bandlimit (L): I've started to understand how varying the bandlimit affects both accuracy and cost — higher L captures finer detail on the sphere but noticeably increases the compute time and memory used.
- Sampling schemes: I compared different sampling schemes, such as the McEwen & Wiaux (MW) scheme and HEALPix. The equiangular MW sampling has an exact sampling theorem, so its round-trip error stays close to machine precision, whereas HEALPix doesn't, and so it shows a small error. It was useful to see that trade-off in practice rather than just reading about it.
- Numerical precision: I also noticed the effect of enabling 64-bit precision in JAX. Leaving it on the default 32-bit made the round-trip error much larger even at moderate L.

Alongside the code, I spent some time skimming the Price & McEwen paper that the package is based on, mainly to get a rough feel for where the recursions come from, even if the details are still beyond me for now.

### Plan For Next Week