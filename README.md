# Customer Churn Analysis

**Authors:** Ava Cannatelli, Natalie Pond, Sarah Sizemore  
**Course:** ISA 616, Miami University (Fall 2026)

## Purpose

A telecom company is losing about 26.5% of its customers (1,869 of 7,043 in our data), so understanding why customers leave and identifying those most likely to leave is important. For this project, we cleaned and analyzed customer data, explored six research questions, and built simple models to predict churn. Our goal was to figure out which factors are most closely related to customers leaving and how the company could use this information to focus its retention efforts on those most at risk. We also looked at how many customers who actually churned the company could reach by contacting only the 20% with the highest predicted risk.

## Files and Folders

- `Churn_Project.ipynb` — the final notebook. It contains the project statement, research questions, data cleaning, all six research-question analyses with takeaways, the summary of findings, limitations, and a version history of the software used.
- `Churn_Project.html` — the knitted (exported) HTML version of the notebook. Open this to read the full workflow with all outputs and charts.
- `BVP (1).png` — the Business Value Proposition image shown at the top of the notebook and HTML. Keep it in the same folder as both files.
- `requirements.txt` — the package versions used (only needed if a package is missing; see below).
- `README.md` — this file.
- `.gitignore` — files excluded from version control.
- `data/` — input data:
	- `Churn_class_project.csv` — the original class-provided customer dataset read by the notebook.
	- `IBM_Telco_Churn_Data_Dictionary.pdf` — the data dictionary describing each field.
- `outputs/` — files the notebook writes:
	- `Churn_cleaned.csv` — the cleaned dataset created by the cleaning section.

The notebook uses project-relative paths, so run it with this folder as the working directory.

## Running the Project

The notebook runs on a standard Anaconda (or Jupyter) installation with Python 3.13; it uses only pandas, numpy, matplotlib, seaborn, scipy, scikit-learn, and statsmodels, which come with Anaconda. No other software is needed.

1. Open `Churn_Project.ipynb` from this folder in VS Code or Jupyter.
2. Choose **Restart & Run All**. The cells run in order from top to bottom; no other files need to be run first.
3. Confirm the notebook finishes without errors and writes `outputs/Churn_cleaned.csv`.

All random processes use a fixed seed (616) so the results are reproducible. The **Version History & Computing Environment** table at the top of the notebook lists the exact versions used.

If a package is missing, install the versions we used with `pip install -r requirements.txt`.

## GitHub

https://github.com/pondnatalie/616_Churn_Project