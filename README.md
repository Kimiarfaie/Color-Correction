# Automatic Color Correction using Colour-Checker Detection

## Overview
This repository implements an end-to-end color correction pipeline based on automatic ColorChecker detection.  
It uses the open-source `colour-science` and `colour-checker-detection` libraries to detect the ColorChecker and apply color correction to the image.

The workflow covers every stage of the color correction process: ColorChecker detection, patch sampling, RGB linearization, color conversion, correction matrix derivation, and output verification.

## Objective

The aim of this exercise is to reproduce a practical camera color correction workflow in Python.  

It shows how to:

- Detect a ColorChecker automatically from a scene image.
- Extract patch values and compute average RGB data of each patch.
- Convert nonlinear sRGB values to linear RGB values.
- Compute both linear (3×3) and second-order polynomial (3×9) color correction matrices.
- Apply and evaluate the resulting correction matrices.

## Getting Started

### 1. Clone this repository
```bash
git clone https://github.com/<kimiarfaie>/Color-Correction.git
```

### 2. Install the required packages

Make sure you have Python 3.12 or later installed.
All dependencies are listed in requirements.txt. Install them with:
```bash
pip install -r requirements.txt
```

### 3. Run the Jupiter Notebook

Place your input images inside the Images/ folder and set the correct path inside the notebook.

Then open and run the notebook step by step.

## Output Files
After running the notebook or script, the following files will be generated inside the output directory:

- `rgb_mean_norm_colors.csv` — normalized RGB patch means  
- `rgb_mean_norm_linear_colors.csv` — linearized RGB patch means  
- `XYZ_reference_ccaft2014_D65.csv` — reference XYZ values (D65 adapted)  
- `Lab_reference_ccaft2014_D65.csv` — reference Lab values (D65 adapted)  
- `CorrMatrix_Linear.csv` — 3×3 linear correction matrix  
- `CorrMatrix_Poly2nd.csv` — 3×9 second-order polynomial correction matrix  


