# Momentum Dynamics Across Project Lifecycles in Ethereum Ecosystems

This repository contains the data and code used in the paper:

**“Momentum Dynamics Across Project Lifecycles in Ethereum Ecosystems: A Panel Vector-Autoregression Approach”**  
Arsh Misra, Columbia University (2025)

The study analyzes the structural evolution of open-source developer activity in decentralized finance (DeFi) protocols using contributor–repository bipartite networks and rolling panel vector autoregression (PVAR).

---

## Repository Contents

The repository includes:

- **Data/**
  - Processed project-level datasets used in all empirical analyses
  - Network-level metric panels constructed from contributor–repository graphs

- **Code/**
  - Scripts for bipartite graph construction
  - Network metric computation (bus factor, Gini repo load, density, redundancy, critical fraction)
  - Rolling within-transformed PVAR estimation
  - Frobenius norm calculations and result aggregation

- **Figures/**
  - Scripts used to generate figures included in the manuscript

- **README.md**
  - Documentation describing data provenance and analysis workflow

---

## Data Availability and Provenance

All data used in the analysis are included directly in this repository and are publicly accessible.

The dataset was originally derived from a third-party platform aggregating open-source contribution data from publicly accessible GitHub repositories. That original data source has since been sunsetted and is no longer publicly accessible. As a result, the archived dataset provided here represents the **complete dataset underlying the findings reported in the paper**.

Because the original source is no longer available, the data cannot be regenerated independently. However, all processed data used in the analysis are preserved in this repository to ensure transparency and reproducibility of the reported results.

---

## Reproducibility

All figures and tables in the paper can be reproduced using the scripts provided in this repository, operating on the included datasets.

The analysis pipeline follows these steps:

1. Construction of contributor–repository bipartite graphs at each snapshot
2. Computation of project-level structural network metrics
3. Within-transformation of panel data to remove project fixed effects
4. Estimation of rolling panel vector autoregression (PVAR) models
5. Computation of Frobenius norms to summarize changes in system dynamics
6. Visualization and aggregation of results by project category

---

## Notes

- The analysis is descriptive and retrospective.
- The PVAR framework is used to characterize short-run structural momentum, not to establish causal effects or predictive classification.
- All code was executed using standard Python data science libraries.

---

## Contact

For questions regarding the data or analysis, please contact:

**Arsh Misra**  
Columbia University

