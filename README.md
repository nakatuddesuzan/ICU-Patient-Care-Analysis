# ICU Patient Outcomes and Care Delivery Analysis

## Project Overview

This project analyzes intensive care unit (ICU) patient data to better understand factors associated with patient outcomes, treatment and care patterns, and healthcare resource utilization.

The analysis uses the **MIMIC-IV Clinical Database Demo**, an open-access subset of MIMIC-IV containing deidentified electronic health record data for 100 patients. The data include hospital admissions, ICU stays, diagnoses, laboratory measurements, medications, procedures, transfers, and other clinical events.

---

## Project Objectives

The primary objective of this project is to improve understanding of factors associated with ICU outcomes and care delivery to support evidence-based clinical practice, quality improvement, and operational decision-making.

The analysis focuses on three main areas:

1. **Patient Outcomes**
   - Examine patient and clinical characteristics associated with outcomes.
   - Explore ICU and hospital length of stay.
   - Examine hospital mortality and discharge disposition.

2. **Treatment and Care Patterns**
   - Describe medication and procedure utilization.
   - Examine ICU interventions, inputs, outputs, and monitoring patterns.
   - Explore how treatment patterns vary across patients and encounters.

3. **Resource Utilization**
   - Examine variation in ICU and hospital length of stay.
   - Evaluate procedure, prescription, transfer, and ICU intervention utilization.
   - Identify patterns associated with higher levels of healthcare resource use.

Because the MIMIC-IV Demo contains a relatively small sample, the project emphasizes **descriptive and exploratory analysis**. Relationships identified in the data are interpreted as associations rather than causal effects.

---

## Dataset

The project uses the **MIMIC-IV Clinical Database Demo**, derived from electronic health records collected during routine clinical care at Beth Israel Deaconess Medical Center (BIDMC).

The demo dataset contains records for **100 patients** while preserving the relational structure of the full MIMIC-IV database.

The data are primarily organized into two modules:

- **HOSP** – hospital-level information including patients, admissions, diagnoses, laboratory measurements, prescriptions, procedures, and transfers.
- **ICU** – ICU-specific information including ICU stays, charted clinical measurements, inputs, outputs, and procedures.

Important identifiers used to connect records include:

- `subject_id` – patient
- `hadm_id` – hospital admission
- `stay_id` – ICU stay

The ICU stay is the primary analytical level for ICU-specific analyses, while some analyses are performed at the patient or hospital-admission level depending on the research question.

---

## Project Structure

```text
project_name/
│
├── README.md
│   └── Project overview and navigation guide
│
├── pyproject.toml
│   └── Python dependencies and project configuration
│
├── data/
│   ├── raw/
│   │   └── Original MIMIC-IV Demo data files (READ ONLY)
│   │
│   ├── processed/
│   │   └── Cleaned, transformed, or analysis-ready datasets
│   │
│   └── CONTEXT.md
│       └── Project background, objectives, assumptions, and context
│
├── notebooks/
│   ├── 01-exploration.ipynb
│   │   └── Data understanding and exploratory data analysis
│   │
│   ├── 02-preparation.ipynb
│   │   └── Data cleaning, transformation, joining, and feature creation
│   │
│   ├── 03-modeling.ipynb
│   │   └── Statistical analysis and/or modeling
│   │
│   └── [other notebooks]
│
├── reports/
│   └── business and data understanding
│
│
├── results/
│   ├── figures/
│   │   └── Charts and visualizations generated during analysis
│   │
│   ├── models/
│   │   └── Saved models, if applicable
│   │
│   └── [other outputs]
│
└── src/
    └── Reusable Python scripts and helper functions, if applicable

```
