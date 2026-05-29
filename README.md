# Pediatric Asthma Risk Analysis: South Carolina

## Project Overview
Exploring South Carolina **pediatric asthma problem set, as it is the fourth leading cause of hospitalizations** across the state. This project utilizes machine learning and geospatial analysis to identify risk drivers and localized clusters.

## Methodology

### Geospatial Interpolation
To ensure precision in pollutant estimates, I utilized **Ordinary Kriging with a Spherical Variogram**. 
* **Border Bias Mitigation:** Integrated "anchor sensors" from Georgia and North Carolina to eliminate edge-effect inaccuracies in air quality modeling.

### Feature Engineering
* **Pediatric Total Housing Vulnerability Index:** A custom-engineered feature combining densities of mobile homes, renters, and group quarters to measure socio-environmental risk.

## Machine Learning 
After comparing multiple models, **Bayesian Ridge Regression** was selected as the champion.


| Model | Metric | Result |
| :--- | :--- | :--- |
| **Champion** | Mean Absolute Error (MAE) | **15.67** |
| **Key Advantage** | Stability | Superior generalization across diverse SC counties |

## Key Discoveries

*   **Housing Signal:** The engineered housing index accounted for **52.1% of model importance**, surprisingly surpassing outdoor pollutants like PM10.
*   **Double Burden:** Identified a critical high-risk cluster along the **I-95 "Corridor of Shame."**
*   **Utilization Gaps:** Model over-predictions in border counties suggest a "healthcare leak," where children likely seek care across state lines, indicating higher actual risk than records show.
