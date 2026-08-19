# Mureithi_RPI_Rangeland_Governance_Comparison

This repository contains the data and code used to reproduce the analyses, figures and tables presented in:

Mureithi, I.N., et al. (2026). Relative Productivity Index reveals contrasting rangeland condition trajectories across governance types in southern Kenya. *African Journal of Range and Forage Science*.

A permanent version of this repository is archived at [https://zenodo.org/records/14843888](https://zenodo.org/records/14843888)

Use of this code is licensed under the GNU General Public License v3 (GNU GPL v3).

Contact Isaac Nduta Mureithi at [I.N.Mureithi@exeter.ac.uk]

---

### Project overview

This research investigates how spatial patterns and long-term trends in relative vegetation productivity (RPI) reveal variations in rangeland condition across governance regimes in the Amboseli-Tsavo ecosystem of southern Kenya. The repository integrates multi-decadal GPP satellite data with quantile regression forest modeling and non-parametric trend analysis across national parks, conservancies, group ranches, and settled areas. It provides the full computational workflow to reproduce all spatio-temporal performance assessments, Theil-Sen slope estimates, and comparative governance figures presented in the manuscript.

---

### Repository contents

The primary code and spatial data components included in this repository are listed below.

#### Scripts

| Script | Description |
| --- | --- |
| *Kenya's Rangeland Protected Areas.Rmd* | Main R Markdown document containing the complete analysis workflow including spatial data import, raster processing, metric calculation (MAE, RMSE, $R^2$), Theil-Sen slope estimation, and figure generation across governance zones. |

#### Data

| File | Description |
| --- | --- |
| *actual_gpp_ea_v2.tif* | Integrated annual GPP estimates for 22 hydrological years (Sept 2000–Aug 2023) based on the PML_V2 dataset. |
| *potential_gpp_ea_v2.tif* | Estimated potential GPP for each grid cell derived from a quantile regression forest model (90th percentile). |
| *rpi_ea_v2.tif* | Relative Productivity Index raster layer defined as the ratio between actual and potential GPP. |
| *rpi_ea_temporal_performance.tif* | Three-band quality control raster reporting pixel-level MAE, RMSE, and $R^2$ model metrics. |
| *Amboseli_Conservation_Areas/* | Shapefiles for AET conservancies and community lands (*AET_Conservancies*, *AET_Other_Conserved_Areas*); sourced from Sustain East Africa Ltd. / Dr. Peter Tyrrell. |
| *Tsavo_Conservation_Areas/* | Shapefiles for ranches and settled areas (*RanchesTTWCA*, *SettledAreas*); sourced from Amos Chege Muthiuru (King’s College London). |
| *WDPA_Amboseli_Tsavo/* | National Park boundary shapefiles sourced from the World Database on Protected Areas (WDPA; UNEP-WCMC & IUCN, 2025). |

---

### Getting started

Clone this repository and review the project overview and repository structure before running the analysis.

TESS Lab projects typically use `renv` to record package dependencies and software versions. Where an *renv.lock* file is included, restore the project environment before running any analyses. Always open this project via the *.Rproj* file in RStudio so that *.Rprofile* is sourced automatically:

```R
renv::restore()

```

---

### Running the analysis

Open and knit the main R Markdown script:

* *Kenya's Rangeland Protected Areas.Rmd*

Rendered HTML outputs are excluded from version control to manage repository size, but are automatically compiled when the pipeline is executed.

---

### Funding acknowledgement

This work was developed under the Oppenheimer Programme in African Landscape Systems (OPALS) ~ Terrestrial Ecosystem Science and Services (TESS) Labs, building upon initial research conducted at the University of Exeter.
