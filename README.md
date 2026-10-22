# medicare-fraud-oig-billing-analysis
Exploratory data analysis of CMS Medicare Part B physician billing patterns cross-referenced with HHS OIG exclusion lists in Python.

# Medicare Part B Billing Patterns & OIG Exclusion Analysis

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/YOUR_USERNAME/YOUR_REPO_NAME/blob/main/YOUR_NOTEBOOK_NAME.ipynb)

## Project Overview
An exploratory data analysis and anomaly detection project examining **Medicare Part B physician billing patterns** cross-referenced against the **Office of Inspector General (OIG) List of Excluded Individuals/Entities (LEIE)**. This project investigates service volume, beneficiary counts, and billing metrics to identify potential compliance risks and outlier utilization behavior among healthcare providers.

## Key Objectives
* **Dataset Integration:** Clean, standardize (NPI/ provider identifiers), and merge CMS Medicare Part B payment summary records with OIG exclusion records.
* **Utilization Analysis:** Evaluate total service volume against unique beneficiary counts across specialties and geographic regions.
* **Outlier & Anomaly Detection:** Visualize billing distributions using scatter plots and summary statistics to compare excluded or high-risk providers against peer benchmarks.

## Data Sources
Due to file size constraints on GitHub, the full raw CMS dataset is not stored in this repository. You can access the primary data sources below:
1. **CMS Medicare Physician & Other Practitioners Dataset:** [CMS Data Portal](https://data.cms.gov/)
2. **OIG LEIE Exclusion List:** [HHS OIG Exclusions Database](https://oig.hhs.gov/exclusions/exclusions_list.asp)

## Methodology & Tech Stack
* **Environment:** Google Colab (Python)
* **Libraries:** `pandas`, `numpy`, `matplotlib`, `seaborn`
* **Workflow:**
  1. Data ingestion and NPI validation across billing and exclusion records.
  2. Aggregation of healthcare service volume and beneficiary metrics at the provider level.
  3. Comparative visualization (service volume vs. beneficiary count scatter plots) to highlight anomalous billing ratios.
