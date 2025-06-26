# Interactive-Quality-Incident-Analysis


Overview

A comprehensive Excel-based analysis and interactive dashboard of quality incidents, covering December 2023 through June 2025 and 45,000+ records. This project identifies key drivers of quality issues, visualizes trends over time, and delivers actionable recommendations for process improvement.

## Project Structure
quality-incident-analysis/
├── README.md                         # This file
├── Quality_Incidents_Dashboard.xlsx  # Final interactive Excel workbook
├── Dashboard_Snapshot.pdf            # Exported PDF of the dashboard
├── Quality_Incident_Report.pdf       # Written report document summarizing findings and recommendations
└── Data/
    └── quality_incidents_cleaned.csv # Cleaned incident dataset (45k+ rows)

## Key Components
1. **Executive Summary**
   - Process incidents top at ~21%.
   - One-third of incidents remain **Open**; 17% have **Unknown** status.
   - 20% of records have **Unspecified** source systems.

2. **Data Cleaning & Prep**
   - Standardized date formats with Python (`pd.to_datetime`, `dayfirst=True`).
   - Mapped typos and variants in Category, Severity, Status, Department, and Source_System.
   - Filled missing values with explicit placeholders (e.g. `Unknown`, `No Action Recorded`).
   - Trimmed dataset to **June 30, 2025** and removed blank rows.

3. **Interactive Dashboard (Excel)**
   - **Timeline slicer** for flexible date filtering.
   - **Slicers** for Category, Severity, Department, and Source System.
   - **PivotCharts**: Time-series trend, Category breakdown, Department ownership, Source System analysis, Severity & Status distributions.

4. **Insights & Recommendations**
   - Prioritize root-cause analysis on **Process**, then split focus between **Mechanical** and **Electrical**.
   - Audit and reclassify **Unknown** categories and statuses to improve data quality.
   - Implement SLA targets to reduce **Open** backlog.
   - Tighten logging procedures to eliminate the **Unspecified** system gap.

## Getting Started
1. **Download** the `Quality_Incidents_Dashboard.xlsx` file.
2. **Enable macros** (if prompt appears) to activate slicers and timeline.
3. **Refresh** data: `Data → Refresh All` after replacing `quality_incidents_cleaned.csv` in the Data folder.
4. **Interact** using the slicers and timeline on the Dashboard sheet.

## Next Steps
- **Python Automation**: Convert the cleaning and pivot creation steps into a reproducible Python notebook.
- **Tableau Version**: Rebuild views in Tableau Public for advanced interactivity and web publishing.

---

*For any questions or feedback, please contact [Devin Richmond](richmonddevin13@gmail.com).*
