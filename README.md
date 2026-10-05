# Fast or Accurate? Deep-Learning vs Model-Based Wavefront Sensing

LaTeX source for a simulation study comparing a convolutional neural network (CNN) and a gradient-descent physics fit for focal-plane wavefront sensing from phase-diverse point-spread-function (PSF) images, and proposing a hybrid of the two.

**Authors:** Abiska Sharma, Pratikshya Kafle
Sunway College Kathmandu, Nepal (affiliated with Birmingham City University, UK)

## Summary

A 16-mode Zernike wavefront is estimated from a two-channel (in-focus + defocused) PSF input under Poisson and read noise. In a single-seed simulation, a 1.2M-parameter CNN cuts the mean residual wavefront RMS from 0.549 rad to 0.077 rad, while the physics fit reaches 0.024 rad but is about 53x slower on CPU. The paper also covers a channel ablation, photon-flux and turbulence robustness sweeps, and a proposed (not yet evaluated) CNN-initialised hybrid estimator.

Results are simulation-only, from one random seed and a reduced training profile.

## Contents

- `main.tex` - paper source
- `references.bib` - BibTeX references
- `images/` - figures (add the files below)

## Figures needed in `images/`

- `wavefront_reconstructions_comparison.png`
- `ablation_channels.png`
- `sweeps.png`

Missing figures appear as placeholder boxes.

## Build

```
pdflatex main
bibtex main
pdflatex main
pdflatex main
```
