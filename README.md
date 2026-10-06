# Coin Segmentation and Canny Edge Detection

Python notebook implementing a classical image-processing pipeline for coin segmentation and counting, together with a custom Canny edge detector.

## What the notebook covers

- **Coin segmentation (`coin_mask`):** separates coins from a green background using the Lab color space, median filtering, and Otsu thresholding.
- **Connected components (`bw_label`):** assigns labels to regions using 8-connected pixel neighborhoods.
- **Coin classification (`coin_classification`):** distinguishes smaller 1-dinar and larger 5-dinar coins by region area and returns their counts.
- **Canny edge detection (`canny_edge_detection`):** Gaussian smoothing, image gradients, magnitude and direction, non-maximum suppression, double thresholds, and edge linking by hysteresis.
- **Parameter experiments:** compares edge maps for different thresholds and discusses the effects of noise and lost detail.

## Getting started

Requires Python 3, JupyterLab, NumPy, SciPy, Matplotlib, and scikit-image.

```bash
python -m venv .venv
source .venv/bin/activate
python -m pip install jupyterlab numpy scipy matplotlib scikit-image
jupyter lab
```

Open [domaci3_20_662.ipynb](domaci3_20_662.ipynb) and run the cells in order from the repository directory.

## Input data

The original assignment images are **not included in this repository**. To rerun the experiments, supply the following files at the paths expected by the notebook:

- `coins/coins1.jpg through coins/coins9.jpg (see the notebook's image loop)`
- `lena.tif`
- `van.tif`
- `camerman.tif`

The notebook contains saved figures and outputs that can be viewed without rerunning it. The notebook text and comments are primarily in Serbian.

## Project context

Academic image-processing coursework (DOS), with implementations, parameter experiments, visual comparisons, and discussion. This repository preserves the original notebook; it is not a packaged library. Dependencies are not version-pinned, and compatibility with current releases has not been verified. Full execution requires the missing input images.

## Scope

The coin experiment uses background color and object area; it is intended for the supplied controlled-background images. The notebook shows intermediate Canny results alongside final edge maps.
