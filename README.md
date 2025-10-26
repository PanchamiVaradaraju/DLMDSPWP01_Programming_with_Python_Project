# Ideal Function Mapping Pipeline

This Jupyter Notebook (`DLMDSPWP01_Programming_with_Python.ipynb`) finds the best matching "ideal" functions for training data and maps test data points to them. It runs in Google Colab.

## What it does

1.  **Loads Data:** Reads `train.csv`, `ideal.csv`, and `test.csv` from an uploaded ZIP file.
2.  **Finds Best Fits:** For each function in `train.csv`, it selects the best matching function from `ideal.csv` using the least squares method.
3.  **Maps Test Points:** It takes points from `test.csv` and assigns them to one of the selected ideal functions if they fall within a calculated deviation threshold 
4.  **Stores Results:** Saves the original data and the mapped test results into an SQLite database (`results.db`).
5.  **Visualizes:** Creates plots (using Matplotlib and Bokeh) to show the training data, the chosen ideal functions, and how the test points were mapped.

## How to Run

1.  **Zip your data:** Put `train.csv`, `ideal.csv`, and `test.csv` into a single ZIP file (e.g., `data.zip`).
2.  **Open in Colab:** Upload and open the `.ipynb` file in Google Colab.
3.  **Run cells:** Execute the cells one by one.
4.  **Upload ZIP:** When prompted, upload your data ZIP file.
5.  **Check outputs:** The notebook will show plots, print results, and create `results.db`.
6.  **Download DB (Optional):** Run the last cell to download `results.db`.

## Inputs

* A ZIP file containing:
    * `train.csv` (Columns: x, y1, y2, y3, y4)
    * `ideal.csv` (Columns: x, y1...y50)
    * `test.csv` (Columns: x, y)

## Outputs

* `results.db`: An SQLite database with tables for training data, ideal functions, raw test data, and the final mapped test data.
* Inline plots (Bokeh and Matplotlib) showing the data and mapping results.

## Requirements

* Python 3 / Google Colab
* Packages: `pandas`, `sqlalchemy`, `bokeh`, `matplotlib`, `numpy`

---
*Generated based on the provided Jupyter Notebook.*
