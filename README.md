# OCDCTDphase1

Code and selected input files used to reproduce the phase 1 OCD, CTD, and OCDCTD TADA gene discovery analyses.

## Contents

| File | Description |
|---|---|
| `OCD_CTD_TADA.qmd` | Quarto analysis notebook for the OCD, CTD, and OCDCTD TADA models. |
| `TADAfunctions.R` | TADA Bayes factor and Bayesian FDR functions from Fu et al. 2022. |
| `OCD_CTD_TADA_input.xlsx` | Input tables for cohort counts, priors, and mutability metrics. |

## Running

Run from the repository root so relative paths resolve correctly:

```r
quarto::quarto_render("OCD_CTD_TADA.qmd")
```

System requirements: R 4.2.3, `tidyverse` 2.0.0, `readxl` 1.4.2, and `quarto` for rendering. This code has been tested on macOS 13.3.1.

Expected output is a `tada_results` data frame with TADA results for OCD, CTD, and OCDCTD cohorts. Expected runtime on a standard desktop computer is under 5 minutes.

TADA functions are from Fu et al. 2022; see [TADA_2022](https://github.com/talkowski-lab/TADA_2022) and [Zenodo](https://doi.org/10.5281/zenodo.6496480).
