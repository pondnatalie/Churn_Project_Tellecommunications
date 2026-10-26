# Customer Churn Analysis

**Authors:** Ava Cannatelli, Natalie Pond, Sarah Sizemore
**Course:** ISA 616, Miami University (Fall 2026)

## Purpose

This project analyzes customer churn for a telecommunications company using the class-provided IBM Telco-style dataset (7,043 customers, response variable `Churn`). We clean and preprocess the data, then answer six research questions: how tenure and satisfaction relate to churn, whether tech support reduces churn, which customer segments are highest risk, whether contract and payment method effects hold up after adjusting for other factors, how accurately we can predict churn, and how many churners the company would catch by contacting only its riskiest customers. The notebook is written for a fellow analyst or practitioner who wants to reproduce or extend the analysis.

## Folder Structure

```
616_Churn_Project/
├── data/
│   ├── Churn_class_project.csv     # original class dataset (input)
│   └── (data dictionary PDF)
├── outputs/
│   └── Churn_cleaned.csv           # cleaned dataset written by the notebook
├── Churn_Project.ipynb             # analysis notebook (run this)
├── Churn_Project.html              # knitted HTML version of the notebook
├── BVP (1).png                     # Business Value Proposition image shown in the notebook
├── requirements.txt                # pinned Python package versions
├── .gitignore
└── README.md
```

`data/` contains `Churn_class_project.csv`, the raw dataset the notebook reads. The notebook uses relative paths, so run it from the project folder.

## Setting Up the Environment

The notebook was produced with Python 3.13 (Anaconda). The exact software versions are printed in the "Version History & Computing Environment" section at the top of the notebook.

With conda:

```bash
conda create -n churn python=3.13
conda activate churn
pip install -r requirements.txt
```

Or with a virtual environment:

```bash
python -m venv .venv
.venv\Scripts\activate        # Windows
source .venv/bin/activate     # macOS/Linux
pip install -r requirements.txt
```

## Running the Notebook

From the project folder, open the notebook with `jupyter lab` or `jupyter notebook` (or VS Code) and choose **Restart & Run All**. To run it from the command line instead:

```bash
jupyter nbconvert --to notebook --execute --inplace Churn_Project.ipynb
```

Running the notebook rewrites `outputs/Churn_cleaned.csv`. All random steps use fixed seeds (`random_state=616` for the split and models, `random_state=42` for the imputer), so results are reproducible.

## Exporting the HTML

```bash
jupyter nbconvert --to html --embed-images Churn_Project.ipynb
```

`--embed-images` stores the Business Value Proposition image inside the HTML file, so it displays without the PNG alongside it.

## Business Value Proposition

### Project Overview

Our project focuses on customer churn in a telecommunications company. We want to identify customers who are likely to leave, understand the characteristics associated with churn, and determine which customer groups generate the most revenue. Looking at churn risk and revenue together will help leadership decide where to focus retention efforts and budget.

### Customer Segment

This project is for the executive leadership of the telecommunications company. Their main goals are to develop effective customer retention strategies, protect customer revenue, and support profitability.

### Business Problem

Leadership may have difficulty identifying customers who are likely to leave and understanding the factors associated with churn. They may also have limited visibility into which customer groups generate the most revenue.

When customers leave, the company loses revenue and faces the expense of acquiring replacement customers. Without a clear understanding of customer risk and value, it can be difficult to decide where to spend the retention budget.

### Value Proposition

Our churn analysis and predictive model will help telecommunications leaders identify customers likely to leave, understand factors associated with churn, and recognize customer groups that generate higher revenue. These insights can guide targeted retention strategies and resource allocation to help preserve revenue and improve profitability.

### Products and Services

- Comparisons of churn and revenue across customer groups.
- A classification model that estimates customer churn risk.
- A framework for prioritizing retention outreach using estimated churn risk and available revenue information.
- A presentation of findings and actionable recommendations.
- An analysis of customer characteristics associated with churn.

### Pain Relievers

Our churn prediction model will estimate which customers are most likely to leave, helping leadership prioritize retention outreach.

We will analyze demographic, account, service, and contract characteristics to identify patterns associated with churn. This will help leadership better understand the factors that may be relevant to retention decisions.

Our customer-segment revenue analysis will identify which groups generate the most revenue and help clarify the financial impact of losing those customers. Combining churn risk and revenue into a scoring framework will help leadership focus the retention budget on high-value accounts at risk of leaving.

### Gain Creators

We will segment customers based on their expected value and use a consistent framework that combines churn risk and revenue information.

Comparing customer groups will help reveal differences in service, contract, and churn patterns. These findings can support more personalized retention recommendations for different groups.

Simple visual dashboards will communicate customer risk and revenue patterns, along with recommendations to help leadership decide where to focus retention efforts.

### Expected Gains

- Identify and prioritize the most valuable customers.
- Develop more personalized retention strategies for different customer groups.
- Make more informed, faster decisions about where to spend the retention budget.
- Identify opportunities to preserve customer revenue and improve profitability.

### Overall Goal

Our goal is to help leadership use customer churn risk and revenue information to make better retention decisions. By identifying valuable customers who are at risk of leaving, we can provide recommendations for where to focus outreach and retention resources.
