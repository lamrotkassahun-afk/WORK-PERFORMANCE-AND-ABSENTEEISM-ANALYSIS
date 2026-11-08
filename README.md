# WORK-PERFORMANCE-AND-ABSENTEEISM-ANALYSIS
A large Western Canadian retail organisation, Mega Supermart, has engaged you as a Business Intelligence Consultant. The company is undergoing a broader operational review focused on workforce optimisation, reducing absenteeism, and improving departmental staffing efficiency across its stores and business units. 
Workforce Performance & Absenteeism Analysis - Mega Supermart

Executive Summary & Overview

Mega Supermart, a major retail organisation operating across Western Canada, engaged a Business Intelligence Consultancy to conduct a comprehensive operational review. The initiative focuses on workforce optimization, departmental staffing efficiency, and mitigating absenteeism risks across its store network and business units.

This project delivers an in-depth Exploratory Data Analysis (EDA) on an anonymized workforce dataset of 1,200 employee records (cleaned to 1,198 complete records). The analysis evaluates workforce demographics, length-of-service structures, store/departmental staffing patterns, chronic absenteeism drivers, and retirement-risk segments to empower executive leadership with actionable, data-driven human capital strategies.

Key Business Insights & Analytical Findings

Front-Line Absenteeism Drivers: Absenteeism is disproportionately concentrated in customer-facing retail roles. Customer Service (averaging 62.99 absent hours/year, 3.57% absence rate) and Sales (averaging 57.45 absent hours/year, 3.36% absence rate) lead lost time compared to back-office or logistics functions such as Operations (26.19 hours) and Management (30.48 hours).

Acute Outlier Vulnerability: A statistical outlier cohort of 50 employees (4.17% of total staff) accounts for an extreme share of total lost hours, with individual absences reaching up to 720 hours/year due to chronic disengagement or extended medical leave.

Imminent Retirement & Skill Continuity Risk: A pool of 52 employees (4.34% of staff) meets critical tenure ($\ge 20$ years) or age ($\ge 60$ years) thresholds, primarily in leadership and senior administrative roles, highlighting the need for immediate succession planning.

Data Hygiene Optimizations: Data quality audits resolved missing values in Gender and absenteeism metrics while unifiying string casing issues (e.g., merging split departmental categories such as sales vs. Sales).

Project Repository Architecture

WORK-PERFORMANCE-AND-ABSENTEEISM-ANALYSIS/
│
├── data/
│   ├── raw/                 # Contains raw Excel dataset (Mega_Supermart_HR_Dataset_2025.xlsx)
│   └── processed/           # Processed & cleaned exports (CSV/Pickle)
│
├── notebooks/
│   └── Lamrot_Kassahun_Workforce_Analysis.ipynb  # Primary Jupyter Notebook containing data wrangling & EDA
│
├── outputs/
│   ├── figures/             # High-resolution generated charts (PNG, 300 DPI)
│   │   ├── department_distribution.png
│   │   ├── job_title_distribution.png
│   │   ├── age_histogram.png
│   │   ├── tenure_histogram.png
│   │   ├── cleaned_department_absenteeism.png
│   │   ├── absenteeism_by_department.png
│   │   └── correlation_heatmap.png
│   └── reports/             # Final executive briefing deliverables & deck
│       ├── Mega_Supermart_Workforce_Analysis_Report.md
│       └── Mega_Supermart_Workforce_Analysis_Deck.html
│
├── venv/                    # Python virtual environment (ignored in git)
├── .gitignore               # Git exclusion rules for large datasets & virtual environments
└── README.md                # Project documentation & execution guide


Installation & Local Execution Guide

Follow these steps to set up the environment and run the analysis locally:

Step 1: Clone the Repository & Navigate to Project Root

git clone https://github.com/lamrotkassahun-afk/WORK-PERFORMANCE-AND-ABSENTEEISM-ANALYSIS.git
cd WORK-PERFORMANCE-AND-ABSENTEEISM-ANALYSIS


Step 2: Create & Activate Python Virtual Environment

Windows (PowerShell):

python -m venv venv
venv\Scripts\Activate.ps1

Step 3: Install Required Dependencies

pip install pandas numpy matplotlib seaborn openpyxl jupyter


Step 4: Verify Data File Placement

Ensure the dataset Mega_Supermart_HR_Dataset_2025.xlsx is placed in the data/raw/ directory:

data/raw/Mega_Supermart_HR_Dataset_2025.xlsx


Step 5: Launch Jupyter Notebook

jupyter notebook notebooks/Lamrot_Kassahun_Workforce_Analysis.ipynb


Visualisation Suite Included

The analysis notebook automatically exports six primary visualizations to outputs/figures/:

Department Headcount Breakdown: Horizontal bar chart of employee distribution across standardized departments.

Top 10 Job Titles: Headcount ranking across core retail roles.

Age Distribution & KDE: Histogram overlaying age density ($18 - 66$ years).

Length of Service Distribution: Tenure density analysis ($0 - 27$ years).

Departmental Absenteeism Spread: Horizontal boxplot highlighting medians, IQRs, and outliers per department.

Correlation Heatmap: Seaborn matrix mapping relationships between Age, Tenure, Scheduled Hours, and Absent Hours.

Author & Submission Metadata

Author: Lamrot Kassahun Assefa

Role: Business Intelligence Consultant

Target Audience: Mega Supermart Executive Leadership Team

Course / Assignment: Workforce Performance & Absenteeism Analysis

Submission Date: November,09 2026