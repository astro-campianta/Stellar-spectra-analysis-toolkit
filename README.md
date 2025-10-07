# Stellar-spectra-analysis-toolkit

This Python program provides tools to read, normalize, and analyze stellar spectra, including the comparison with synthetic models and the measurement of the equivalent widths of spectral lines.

---

## Functions

* **read_spectrum**: reads spectra from FITS or ASCII files, extracting fundamental parameters for the subsequent analysis;
* **normalize_continuum**: normalizes the continuum of the observed spectra;
* **correct_redshift**: corrects the observed spectra for redshift;
* **measure_equivalent_width**: measures the equivalent widths of spectral lines and computes the associated error;
* **match_resolution**: matches the spectral resolution between observed and model spectra;
* **chi2_fit**: computes chi-square between observed and model spectra;
* **compare_with_models**: compares the observed spectra with a grid of synthetic models and visualizes the best fit.

---

## Parameters

* **filename**: path to the FITS or ASCII file containing the spectrum;
* **hdu_index**: HDU index in FITS file to read the data from (default: 1);
* **lambda_column**: name of the wavelength column in a FITS table (default: 'WAVELENGTH');
* **flux_column**: name of the flux column in a FITS table (default: 'FLUX');
* **err_column**: name of the error column in a FITS table (default: 'ERROR');
* **lambda_obs**: array of observed wavelengths (Angstroms);
* **flux**: array of observed flux values;
* **flux_err**: array of flux uncertainties (can be None or NaN if unavailable);
* **order**: order of the polynomial used to fit the continuum (default: 3),
* **z**: redshift value used to correct observed wavelengths;
* **line_region**: tuple specifying start and end wavelength of the spectral line;
* **continuum_regions**: list of tuples specifying wavelength ranges for continuum fitting;
* **fwhm_obs**: full-width at half-maximum of the observed spectrum;
* **fwhm_model**: full-width at half-maximum of the model spectrum;
* **lambda_model**: wavelength array of the model spectrum;
* **flux_model**: flux array of the model spectrum;
* **models**: list of synthetic model spectra, each as a dictionary with keys `'lambda'`, `'flux'`, `'age'`, `'Z'`;
* **lines**: dictionary defining spectral lines and their continuum regions for equivalent width measurement.

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
```

## Development and collaboration histort

This Python code was developed by Camilla Pianta during her collaboration with Dr. Antonino Milone’s research group, as part of a research project on multiple stellar populations (see Milone et al. 2025, https://arxiv.org/abs/2503.19214).
