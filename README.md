# Image Anomaly Detection Using LSH (Locality Sensitive Hashing)
## Description:

This project implements an Anomaly Detection system for images using Locality Sensitive Hashing (LSH). The system extracts features from a dataset of images (such as CIFAR-10) by computing histograms of pixel values for each channel (R, G, B), and uses LSHForest to detect anomalies in a new image by comparing it to the existing dataset.

## Features:

### Data Preprocessing:

Loads and resizes images from the CIFAR-10 dataset.

Normalizes pixel values and calculates histograms for each RGB channel.

Creates a feature vector by concatenating the histograms of each channel.

### Feature Extraction:

Computes histograms for the Red (R), Green (G), and Blue (B) channels of each image.

Converts the image data into feature vectors, representing the distribution of pixel intensities.

### Locality Sensitive Hashing (LSH):

Uses MinHashLSH to create hash tables for efficient similarity search.

Fits an LSH Forest model to the feature vectors of normal images.

### Anomaly Detection:

Computes the feature vector for a new image.

Queries the LSH Forest to find the nearest neighbors of the new image.

Measures the distance between the new image and its nearest neighbors.

Flags the image as an anomaly if its distance exceeds a predefined threshold.

Threshold-Based Anomaly Detection:

If the distance between the new image and its nearest neighbors is greater than a threshold, the image is flagged as an anomaly.
