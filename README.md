# Python Data Analysis and Machine Learning Projects

This repository contains three small-to-medium Python projects focused on data analysis, visualization, and machine learning.  
Each project is implemented independently and demonstrates practical use of Python libraries such as **NumPy**, **Pandas**, **Matplotlib**, and **Scikit-learn / SciPy**.

## Projects Included

### 1) Formula 1 Race Results Analysis
This project analyzes Formula 1 race results using **Pandas** and **Matplotlib**.

#### Features
- Read and preprocess F1 race data
- Extract year and month from race dates
- Find the first and last race year
- Visualize race distribution by month
- Identify top winning drivers
- Identify the most successful teams
- Find drivers with the most wins in a single season
- Analyze race frequency by Grand Prix
- Explore driver success in top 3 countries
- Find the first win year for random drivers
- Detect the driver with the longest gap between first and last win
- Plot the win trend of the most successful driver
- Calculate win probability by decade
- Export final results to Excel

#### Technologies
- Python
- Pandas
- Matplotlib
- OpenPyXL

#### Main Files
- `f1_results_analysis.py`
- `f1_results.csv`
- `question_13_win_probability_by_decade.xlsx`

---

### 2) Titanic Dataset Analysis with NumPy
This project analyzes the Titanic dataset using only **NumPy** for data processing and **Matplotlib** for visualization.

#### Features
- Load and inspect the Titanic dataset
- Display the first and last rows
- Compute statistical values for numeric columns
- Replace zero values with column means
- Calculate survival percentages by gender
- Split data into male and female arrays
- Extract survivors
- Count passengers by embarkation point
- Find the passenger with the highest fare
- Create a new feature from `Parch` and `SibSp`
- Plot frequency of the new feature
- Sort passengers by age
- Calculate average age of male passengers
- Compare two random passengers using charts
- Sort the dataset by cabin class

#### Technologies
- Python
- NumPy
- Matplotlib

#### Main Files
- `titanic.csv`
- `titanic_analysis.ipynb` or `titanic_analysis.py`

---

### 3) Image Classification by Color Using K-Means
This project performs automatic image preprocessing and unsupervised image classification based on dominant color groups: **Red**, **Green**, and **Blue**.

#### Features
- Read raw images and metadata
- Preview sample images
- Map labels into numeric categories
- Apply preprocessing:
  - Cropping
  - Blurring
  - Resizing
- Train a **K-Means** model with `K = 3`
- Classify images into color groups
- Visualize class distribution
- Calculate classification accuracy
- Save classified images into organized folders

#### Technologies
- Python
- NumPy
- Pandas
- Matplotlib
- OpenCV / Pillow
- SciPy / Scikit-learn

#### Main Files
- `main.py`
- `data/images/`
- `data/metadata.xlsx`

---

## Repository Structure
```text
.
├── f1-project/
│   ├── f1_results_analysis.py
│   ├── f1_results.csv
│   └── question_13_win_probability_by_decade.xlsx
│
├── titanic-project/
│   ├── titanic.csv
│   └── titanic_analysis.ipynb
│
├── image-classification-project/
│   ├── main.py
│   ├── data/
│   │   ├── images/
│   │   └── metadata.xlsx
│   └── output/
│
└── README.md
