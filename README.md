
# NYC 2024 Marathon Analysis 🏃‍♂️🏃‍♀️

This project analyzes data from the **2024 NYC Marathon**, pulled directly from the official [NYRR Results site](https://results.nyrr.org/home).

## 📊 Project Overview

- **Data Collection**: Race result data is scraped from the NYRR website using Python.
- **Data Storage**: Collected data is stored in a local database to speed up retrieval and avoid repeated downloads.  
  ⚠️ Building the full dataset from scratch can take **~45 minutes** due to the volume of records. For convenience, you can:
  - Download a prebuilt database file from this repo
  - Or run the script with a smaller batch of runner results

## 🔍 Analysis Approach

- **Goal**: Estimate the **gender** of a runner based on their runtime using statistical modeling.
- **Method**: Applied **Kernel Density Estimation (KDE)** with a **Gaussian kernel** to model the distribution of runtimes and predict gender.
  - KDE helps visualize the probability distribution of the dataset by smoothing over individual data points.
  - This technique provides insight into runtime trends by gender across thousands of participants.

## 📁 Files Included

- `scraper.py`: Script to pull data from the marathon results site
- `database.db`: SQLite database of marathon runners (downloadable)
- `kde_analysis.py`: KDE implementation for gender prediction
- `README.md`: Project documentation (you’re reading it!)

## 📌 Notes

- This project is for exploratory data analysis and should not be used for sensitive or high-stakes classification.
- You can find the code in the .ipynb file

