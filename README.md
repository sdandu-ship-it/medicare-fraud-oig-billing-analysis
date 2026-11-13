# Detecting Medicare Fraud: CMS Payment Data & OIG Provider Exclusions

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/YOUR_USERNAME/YOUR_REPO_NAME/blob/main/YOUR_NOTEBOOK_NAME.ipynb)

## Project Overview
An exploratory data analysis and anomaly detection project examining **Medicare Part B physician billing patterns** cross-referenced against the **Office of Inspector General (OIG) List of Excluded Individuals/Entities (LEIE)**. This project investigates service volume, beneficiary counts, and billing metrics to identify potential compliance risks and outlier utilization behavior among healthcare providers.

## Key Findings
* **Payment Concentration:** Medicare payments are highly concentrated, with the top 1% of providers accounting for 35.5% of all payments[cite: 1].
* **Utilization Behavior:** There is a strong positive relationship between beneficiary volume and service volume, showing a log-scale correlation of 0.74[cite: 1].
* **Exclusion Anomalies:** Providers matched with the OIG exclusion list demonstrated higher procedural intensity, with a median of 4.07 services per beneficiary compared to 2.87 for non-excluded providers[cite: 1].
* **High-Risk Outliers:** Among providers with at least 100 beneficiaries, 4,286 (0.57%) exceeded the 99th-percentile thresholds for both total Medicare payments and payment per beneficiary, though only one was actively OIG-matched[cite: 1].

## Key Objectives
- **Dataset Integration:** Clean, standardize (NPI/provider identifiers), and merge CMS Medicare Part B payment summary records with OIG exclusion records.
- **Utilization Analysis:** Evaluate total service volume against unique beneficiary counts across specialties and geographic regions.
- **Outlier & Anomaly Detection:** Visualize billing distributions using scatter plots and summary statistics to compare excluded or high-risk providers against peer benchmarks.

## Data Sources
Due to file size constraints, the full raw CMS dataset is not stored in this repository. You can access the primary data sources below:
1. **2024 CMS Medicare Physician & Other Practitioners Dataset:** [CMS Data Portal](https://data.cms.gov/) (1.3M rows)[cite: 1].
2. **OIG LEIE Exclusion List:** [HHS OIG Exclusions Database](https://oig.hhs.gov/exclusions/exclusions_list.asp) (80K rows)[cite: 1].

## Methodology & Tech Stack
- **Environment:** Google Colab (Python)[cite: 1]
- **Libraries:** `pandas`, `numpy`, `matplotlib`, `seaborn`[cite: 1]
- **Workflow:**
  1. Data ingestion and NPI validation across billing and exclusion records.
  2. Aggregation of healthcare service volume and beneficiary metrics at the provider level.
  3. Comparative visualization (service volume vs. beneficiary count scatter plots) to highlight anomalous billing ratios.

## Repository Structure

```text
├── data/                   # Data dictionary and sample datasets (full data excluded)
├── notebooks/              # Jupyter/Colab notebooks for exploratory analysis
├── src/                    # Python scripts for data cleaning and merging
├── visuals/                # Exported PNGs of scatter plots and distributions
└── README.md
```

## Project Team
Developed with equal contributions across Python coding, exploratory analysis, and visualization by Master of Science in Business Analytics (MSBA) candidates at Boston University Questrom School of Business:
- **Sree Dandu**
- **Ahan Nair**
- **Alice Yen**
- **Yuxin Li**
- **Ujjwala Kapoor**
