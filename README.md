# Pressure Build-Up (PBU) Analysis using Python

## Overview

This project performs **Pressure Build-Up (PBU) analysis** for a producing oil well using Python. The objective is to analyze shut-in pressure data and estimate important reservoir parameters such as:

* Average Reservoir Permeability (k)
* Skin Factor (S)
* Reservoir behavior near the wellbore

The analysis is carried out using the **Horner semi-log method**, which is a standard technique used in well test interpretation.


## Objectives

* Plot **Pressure vs Shut-In Time**
* Generate a **Horner Plot**
* Determine the **slope of the straight-line region**
* Calculate **reservoir permeability**
* Calculate **skin factor**
* Interpret wellbore conditions



## Methodology

### 1. Pressure Build-Up Plot

The recorded shut-in pressure data (Pws) is plotted against shut-in time (Δt).

### 2. Horner Time Ratio

The Horner time ratio is calculated using:

[
H = {t_p + Delta t}/{Delta t}
]

where:

* (t_p) = production time before shut-in
* (\Delta t) = shut-in time

### 3. Horner Semi-Log Plot

A semi-log plot of **Pws vs log(H)** is used to identify the straight-line region.

### 4. Permeability Calculation

[
k = \frac{162.6 , B_o , \mu_o , q}{m , h}
]

Where:

* (k) = permeability (md)
* (m) = slope of the straight line
* (B_o) = oil formation volume factor
* (\mu_o) = oil viscosity
* (q) = production rate
* (h) = reservoir thickness

### 5. Skin Factor Calculation

[
S = 1.151 [{P_{1hr}-P_{wf}}/{m} - \log_{10}/({k}/{phi mu c_t r_w^2}) + 3.23 \right]
]



## Results

Estimated results from the analysis:

| Parameter        | Value     |
| ---------------- | --------- |
| Permeability (k) | ~14.18 md |
| Skin Factor (S)  | ~10.08    |

### Interpretation

A **positive skin factor** indicates **formation damage near the wellbore**, which may be caused by:

* Drilling mud invasion
* Scale deposition
* Perforation damage
* Near-wellbore plugging


## Tools Used

* Python
* NumPy
* Pandas
* Matplotlib
* Google Colab
