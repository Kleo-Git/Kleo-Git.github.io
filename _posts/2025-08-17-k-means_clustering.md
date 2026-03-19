---
layout: post
title: "K-Means Clustering for Image Sorting"
date: 2025-08-17
description: "A Computer Vision project using K-Means clustering to analyze, sort, and compress image color profiles across multiple color spaces."
---

# Project Overview
This project implements a custom K-Means Clustering algorithm to perform color quantization and image sorting. By treating every pixel as a data point in color space, the algorithm identifies the most dominant colors (centroids) and can reconstruct images using a reduced colour palette.

# Purpose
To use k-means clustering to simplify colour spaces for colour based image sorting. Additionally, opens up possibilities for future uses such as intelligent recolouring using the same clustering algorithm.

### 1. Multi-Color Space Processing
Unlike standard implementations that only use RGB, this project includes a conversion engine (`Image_To_Array`) that supports:
* **RGB, LAB, HSV, XYZ, and LUV.**
* **Insight:** During testing, I found that the **LAB color space** (which models human perception) maintained color integrity better than RGB, which often appeared "washed out" during heavy clustering.

### 2. K-Means Iterative Visualization
The project features a step-by-step visualization of the clustering process. It demonstrates how random centroid initialization converges toward the image's true dominant colors.
* **Low K-values (k=2 to 8):** Excellent for "Warm vs. Cool" sorting and dominant color extraction.
* **High K-values (k=16 to 128):** Used for image compression and near-perfect recreation.

### 3. Custom Color Mapping Object
I developed a `Colour_Map_Object` class to generate smooth, custom gradients from discrete color dictionaries. This allows for:
* **Gradient Generation:** Creating procedurally generated visuals.
* **Discrete Palettes:** Extracting HSV-based palettes for consistent visualization.

# Methodology
1. **Flattening:** 3D image arrays are flattened into 2D pixel-feature arrays.
2. **Clustering:** K-centroids are initialized; pixels are assigned to the nearest centroid; centroids are recalculated based on the mean of assigned pixels.
3. **Sorting:** The resulting dominant colors are used to categorize images (e.g., sorting a folder of pixel art into "Warm" and "Cool" categories).

[Link to Repo](https://github.com/Kleo-Git/k-means_clustering)