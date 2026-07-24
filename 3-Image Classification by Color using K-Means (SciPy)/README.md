# Image Classification by Color: A SciPy & K-Means Approach

This repository contains a complete Python pipeline for automatic image processing and unsupervised color-based image classification (Red, Green, and Blue) using the **K-Means Clustering** algorithm.

---

## 📋 Project Overview
The objective of this project is to build an automated pipeline that:
1. Loads and prepares raw images alongside their metadata.
2. Applies essential image preprocessing techniques (cropping, blurring, and resizing) to enhance clustering performance.
3. Classifies images into their respective color groups using the **K-Means** algorithm.
4. Evaluates the classification performance by calculating accuracy against ground-truth labels.
5. Organizes and saves classified images into structured directories based on their assigned clusters.

---

## 🛠 Required Libraries & Tools
This project is built using:
* **Python 3.x**
* **NumPy** & **Pandas** (Data manipulation and metadata parsing)
* **OpenCV (cv2)** or **Pillow** (Image preprocessing)
* **SciPy** / **Scikit-learn** (Implementation of K-Means clustering)
* **Matplotlib** (Data visualization and charting)

---

## 🚀 Project Pipeline Steps

### Section 1: Data Reading and Preparation
* **Image Loading:** Reads image files dynamically from a designated system path.
* **Metadata Parsing:** Loads the corresponding Excel/CSV file containing the true labels (ground truth) for performance analysis.
* **Previewing:** Automatically displays three randomly selected images from the dataset to verify loading integrity.
* **Label Mapping:** Converts text-based color classes to numerical category codes:
  * `Red` $\rightarrow$ `0`
  * `Green` $\rightarrow$ `1`
  * `Blue` $\rightarrow$ `2`

### Section 2: Data Preprocessing
Each image undergoes three critical preprocessing steps before clustering:
1. **Cropping:** Removes background margins and focuses on the central regions containing the core color information.
2. **Blurring (Gaussian Blur):** Smooths high-frequency noise and pixel variations, making the overall color distribution more uniform.
3. **Resizing:** Standardizes all input images to a uniform dimension, ensuring consistent vector sizes for clustering.

### Section 3: Unsupervised Classification using K-Means
* **Clustering Implementation:** Trains a K-Means model with $K=3$ to segment the images based on their color features.
* **Distribution Check:** Outputs the exact count of images assigned to each color cluster.
* **Visualizing Results:** Generates and displays a bar chart representing the frequency of images in the Red, Green, and Blue classes.
* **Accuracy Assessment:** Calculates and prints the classification accuracy by comparing predicted cluster labels with the ground-truth Excel file.
* **Structured Saving:** Dynamically creates target directories (`red`, `green`, `blue`) and saves each image into its respective folder named sequentially (e.g., `blue_1.png` to `blue_n.png`).

---

## 🧠 Optimization & Theoretical Concepts

### How K-Means Optimization Works
K-Means is an iterative optimization algorithm that alternates between two steps until convergence:
1. **Expectation (Assignment) Step:** Each data point (image representation vector) is assigned to its nearest cluster center (centroid) based on Euclidean distance.
2. **Maximization (Update) Step:** The coordinates of each centroid are recalculated as the mean of all data points currently assigned to that cluster.

This loop repeats until the centroids no longer shift significantly or the maximum number of iterations is reached.

### Minimization vs. Maximization
K-Means is a **minimization** algorithm. Its goal is to minimize the **Within-Cluster Sum-of-Squares (WCSS)**, also referred to as **Inertia**. 

The objective mathematical function is defined as:
$$J = \sum_{i=1}^{k} \sum_{x \in C_i} ||x - \mu_i||^2$$

Where:
* $k$ is the number of clusters (which is 3 in our project).
* $C_i$ represents the set of points in the $i$-th cluster.
* $x$ is a data point vector representing an image.
* $\mu_i$ is the centroid of the cluster $C_i$.
* $||x - \mu_i||^2$ is the squared Euclidean distance between the point and the centroid.

The algorithm actively minimizes the total squared distance between points and their corresponding cluster centers to ensure tight, well-separated groups.

---

## 📂 Project Directory Structure
```text
├── data/
│   ├── images/          # Raw source images
│   └── metadata.xlsx    # Excel sheet containing actual labels
├── output/              # Classified output folders (generated dynamically)
│   ├── red/
│   ├── green/
│   └── blue/
├── main.py              # Main Python script containing the pipeline
├── requirements.txt     # List of project dependencies
└── README.md            # Project documentation

