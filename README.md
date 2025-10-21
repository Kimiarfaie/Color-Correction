# Automatic Color Correction using Colour-Checker Detection

## Overview
This repository implements an end-to-end color correction pipeline based on automatic ColorChecker detection.  
It uses the open-source `colour-science` and `colour-checker-detection` libraries to detect the ColorChecker and apply color correction to the image.

The workflow covers every stage of the color correction process: ColorChecker detection, patch sampling, RGB linearization, reference conversion, matrix derivation, and output verification.

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
cd Color-Correction