\# XPS-Based Wettability Analysis of Zirconia Surfaces



\## Overview

This project analyzes how surface chemistry and processing sequences affect wettability (water contact angle, WCA) of zirconia surfaces using XPS data and machine learning.



\## Dataset

\- 16 samples (ZrNT and ZrCO)

\- Features:

&#x20; - C 1s, O 1s, P 2p, Zr 3d (XPS)

&#x20; - Experimental descriptions (processing steps)

&#x20; - WCA mean and standard deviation



\## Feature Engineering

Experimental descriptions were converted into structured features:

\- Surface type (ZrNT vs ZrCO)

\- Soaking condition (OA, ODPA, Mix)

\- Rinsing step (Yes/No)

\- Stamping molecule (OA, ODPA)



Additionally, a \*\*process sequence feature\*\* was created:

\- Example: `OA\_to\_ODPA`

\- Captures the order of surface treatments



\## Data Expansion

To account for experimental variability:

\- Dataset expanded using WCA mean and standard deviation

\- Simulated multiple measurements per sample



\## Machine Learning Model

\- Model: Random Forest Regressor

\- Target: WCA (contact angle)

\- Performance:

&#x20; - R² ≈ 0.96

&#x20; - MAE ≈ 3°



\## Key Findings



\### 1. Surface Morphology Dominates

\- ZrNT surfaces show significantly higher WCA than ZrCO

\- Due to nanostructure and surface roughness



\### 2. Chemistry is Critical

\- P 2p (phosphorus) strongly correlates with high WCA

\- Indicates successful ODPA binding



\### 3. Processing Sequence Controls Outcomes

\- Final functionalization step plays a dominant role

\- ODPA as final step leads to highest hydrophobicity

\- Example:

&#x20; - OA soak → ODPA stamp → highest WCA



\### 4. ML Insight vs Physical Insight

\- ML highlights chemistry and morphology as key predictors

\- However, these are controlled by processing sequence

\- Shows importance of feature engineering



\## Tools Used

\- Python

\- pandas

\- matplotlib

\- scikit-learn



\## Author

Nikki

