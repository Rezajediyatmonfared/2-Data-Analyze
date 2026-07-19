# Titanic Dataset Analysis with NumPy

This project analyzes the Titanic dataset using only **NumPy** for data processing and **Matplotlib** for visualization.  
It is designed as a practice project for array operations, statistical analysis, data cleaning, filtering, sorting, and plotting.

## Technologies Used

- Python
- NumPy
- Matplotlib

## Dataset

The project uses the Titanic dataset stored in `titanic.csv`.

## Data Mapping

To make the dataset suitable for numeric analysis, the following value mappings are used:

### Sex
- `0` = Female
- `1` = Male

### Embarked
- `111` = Germany
- `222` = England
- `333` = Spain

## Project Tasks

This notebook performs the following tasks:

1. Read the Titanic dataset using NumPy.
2. Print the first 10 rows and the last 10 rows.
3. Calculate statistical features for each numeric column.
4. Replace zero values in each numeric column with the mean of that column.
5. Calculate the survival percentage of male and female passengers.
6. Split the array into two separate arrays for men and women, and add a sequential ID to each array.
7. Extract the array of survivors.
8. Count passengers by the `Embarked` column.
9. Find the passenger with the highest fare and display their ticket number.
10. Create a new column by summing `Parch` and `SibSp`.
11. Draw a bar chart showing the frequency of the new column values.
12. Sort the array by age.
13. Calculate the average age of male passengers.
14. Randomly select two passengers and compare their age, number of companions, and travel fare using a pie chart.
15. Sort the array by cabin class.

## How to Run

1. Make sure `titanic.csv` is in the same directory as the notebook.
2. Install the required libraries:
```bash
pip install numpy matplotlib
