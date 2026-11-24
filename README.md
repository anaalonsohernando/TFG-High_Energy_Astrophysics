# Statistical Modeling & Signal Detectability Simulation (Fermi-LAT & CTA)

Quantitative data analysis and observability simulation pipeline developed in Python to model high-energy astrophysical sources (Active Galactic Nuclei) and estimate signal detection thresholds under background noise.

## Overview
This project processes public observational catalogs from the **Fermi-LAT 4FHL** dataset to parameterize spectral distributions and simulate future observational performance for the **Cherenkov Telescope Array (CTA-South)**. The core objective is to quantify expected signal-to-background ratios and compute the minimum observation exposure time required to achieve a **$5\sigma$ statistical detection**.

## Key Analytical & Quantitative Components
* **Data Ingestion & Catalog Processing:** Automated parsing, filtering, and validation of multi-dimensional FITS astronomical tables (`gll_psch_v14.fit`) using `Astropy`.
* **Parametric Spectral Modeling:** Implementation and comparison of multiple non-linear spectral models (*Power Law*, *Log-Parabola*, and *Exponential Cutoff*) alongside Spectral Energy Distribution (SED) confidence/butterfly uncertainty bands.
* **Observability & Monte Carlo-style Simulations:** Simulation of source excess photon rates versus background noise rates using `Gammapy` instrument response functions (IRFs) configured for CTA-South coordinates.
* **Statistical Significance Optimization:** Numerical computation of exposure time curves to determine exact thresholds required to reach $5\sigma$ statistical significance across varying flux regimes.

## Tech Stack
* **Language:** Python 3
* **Data & Scientific Computing:** `NumPy`, `SciPy`, `Astropy`, `Gammapy`
* **Visualization:** `Matplotlib`
* **Environment & Workflow:** Linux, Conda, Jupyter Notebooks, Git

## Repository Structure
```text
├── code_analysis.ipynb # Exploratory data analysis, spectral fitting, and 5-sigma simulation notebook
├── .gitignore          # Excludes local FITS data files (4FHL_catalog.fit, irf_file.fits) from version control
└── README.md           # Project documentation
```

## Setup & Reproducibility
1. Clone the repository:
   ```bash
   git clone [https://github.com/anaalonsohernando/fermi-cta-statistical-modeling.git](https://github.com/anaalonsohernando/fermi-cta-statistical-modeling.git)
   cd fermi-cta-statistical-modeling
   ```
2. Create and activate the Conda environment with the required scientific packages:
   ```bash
   conda create -n gamma-analysis python=3.11 numpy scipy matplotlib astropy gammapy jupyter
   conda activate gamma-analysis
   ```

## Author
**Ana Alonso Hernando** — B.Sc. in Physics, Universidad Complutense de Madrid (UCM)  
[GitHub](https://github.com/anaalonsohernando)