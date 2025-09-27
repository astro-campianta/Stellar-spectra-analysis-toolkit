# Stellar-spectra-analysis-toolkit

This Python program provides tools to read, normalize, and analyze stellar spectra, including the comparison with synthetic models and the measurement of the equivalent widths of spectral lines.

---

## Functions

* **read_spectrum**: reads spectra from FITS or ASCII files, extracting fundamental parameters for the subsequent analysis;
* **normalize_continuum**: normalizes the continuum of the observed spectra;
* **correct_redshift**: corrects the observed wavelengths for redshift;
* **measure_equivalent_width**: measures the equivalent widths of spectral lines and computes the associated error;
* **match_resolution**: matches the spectral resolution between observed and model spectra;
* **chi2_fit**: computes chi-square between observed and model spectra;
* **compare_with_models**: Ccompares the observed spectra with a grid of synthetic models and visualizes the best fit.

---

## Installation

Requirements:

- Python 3.x
- [NumPy](https://numpy.org/)
- [Matplotlib](https://matplotlib.org/)
- [Astropy](https://www.astropy.org/)
- [SciPy](https://scipy.org/)

These dependencies can be installed using:

```bash
pip install numpy matplotlib astropy scipy
