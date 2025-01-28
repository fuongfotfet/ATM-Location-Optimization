# ATM-Location-Optimization

## Overview
This project applies **data-driven optimization** to determine the **best ATM placements** for **maximizing population coverage** within a **15-minute walking distance**.

Using **Pyomo** for optimization and the **HiGHS solver**, we efficiently solve the **location-allocation problem** while leveraging **isochrone analysis** for accessibility assessment.

The population dataset is sourced from **Meta Data for Good**, ensuring a real-world, data-driven approach.

## Running the Project

This project consists of **two Jupyter Notebooks**, which must be executed in sequence.

### 1. Prerequisites
Ensure you have **Python 3.8+** installed. Then, install the required dependencies.
```bash
pip install pyomo osmnx geopandas highspy numpy pandas matplotlib folium jupyter
```

Make sure the **HiGHS solver** is installed. Alternatively, you can download it manually from the HiGHS GitHub repository.
``` bash
conda install -c conda-forge highs
```

### 2. Running the Notebooks
Start Jupyter Notebook, then open and run the following notebooks **in order**:

1. **`eda.ipynb`** - **Exploratory Data Analysis (EDA)**
    - Loads the dataset from **Meta Data for Good**.
    - Generates **population density heatmaps**.
    - Computes **existing ATM coverage** using **isochrones**.

2. **`optimize.ipynb`** - **Optimization Model for ATM Placement**
    - Implements the **Pyomo-based mathematical model**.
    - Uses **HiGHS solver** to find the best ATM locations.
    - Visualizes the **optimized ATM placements** and coverage improvements.

## Results
The project generates:
- **Optimized ATM Locations**: The most efficient placements based on population accessibility.
- **Isochrone Maps**: Accessibility heatmaps before and after optimization.
- **Comparative Analysis**: Evaluating ATM efficiency before and after applying optimization.

## Report
For a detailed explanation of the methodology, dataset, and results, please refer to the **report folder**.

## Acknowledgment
I would like to express my gratitude to the author of the article **"Optimizing Retail Location Selection Using Spatial Interpolation: Part 1,2,3"**. Their research provided valuable insights into using **Isochrone Analysis** for location optimization, serving as a critical reference for this project.

## Contributing
We welcome contributions! If you'd like to improve the model, optimize performance, or enhance the visualization, feel free to:
1. **Fork the repository**:
2. **Create a feature branch**:
```bash
git checkout -b feature-branch
```
3. **Commit your changes**:
```bash
git commit -m "Describe your changes"
```
4. **Push to your branch**:
```bash
git push origin feature-branch
```
5. **Submit a pull request** for review.

For inquiries or suggestions, feel free to open an issue! 🚀