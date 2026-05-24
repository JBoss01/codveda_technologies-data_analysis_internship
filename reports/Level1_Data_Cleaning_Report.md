# Level 1 Report: Data Cleaning & Preprocessing

**Codveda Technologies Data Analysis Internship**
**Author:** Ozoeze Wilord Ugonna

---

## What I Did

In this task, I worked with the Iris dataset, a classic dataset containing measurements of 150 flower samples across three species: Setosa, Versicolor, and Virginica. My job was to inspect the raw data, identify any problems, and make sure it was clean and ready for analysis.

---

## Steps I Took

### 1. Loading the Data
I loaded the dataset using pandas and took my first look at its structure. The dataset had 150 rows and 5 columns: sepal length, sepal width, petal length, petal width, and species.

### 2. Checking for Missing Values
I checked every column for missing values. I found none. All 150 records were complete, meaning no information was missing anywhere in the dataset.

### 3. Checking for Duplicate Rows
I checked whether any rows were exact copies of each other. No duplicates were found, confirming that every record represented a unique flower measurement.

### 4. Checking Data Types
I confirmed that all four measurement columns were stored as decimal numbers (float64), which is exactly what they should be for numerical analysis. The species column was stored as text, which is also correct.

### 5. Standardising Category Labels
I inspected the species column for inconsistencies like extra spaces or mixed capitalization. I standardized all labels to lowercase and removed any surrounding whitespace to ensure consistency.

### 6. Outlier Inspection
I used boxplots to check for unusual values in each column. I noticed a few data points in the sepal width column for the Setosa species that sat outside the normal range. However, I kept these in the dataset because they represent real biological measurements, not mistakes.

---

## What I Found

- The Iris dataset arrived in very good condition with no major data quality issues.
- The most important discovery was that petal measurements (length and width) are far more useful for telling the three species apart than sepal measurements.
- The Setosa species is very clearly different from the other two across almost every measurement.

---

## What I Learned

Cleaning data is not always about fixing broken things. Sometimes it is about confirming that the data is trustworthy before moving forward. Going through each check systematically gave me confidence that every analysis I performed afterwards was built on a solid foundation.