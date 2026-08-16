# Cannabis_CivicData
## Missouri Cannabis Data Cleaning Project

This project focuses on collecting, cleaning, validating, and preparing Missouri cannabis data for analysis and visualization in Tableau.

The goal is to build a reliable dataset that can support public education around Missouri's cannabis industry, including licensed facilities, market activity, product recalls, public health information, and geographic access.

### Project Goals

- Collect cannabis data from authoritative public sources.
- Preserve raw data before making changes.
- Clean inconsistent column names and text values.
- Standardize facility types, addresses, ZIP codes, and status fields.
- Identify missing values and duplicate records.
- Validate geographic and business-rule assumptions.
- Create quality-control reports before visualization.
- Export Tableau-ready datasets for geographic analysis.

### Data Cleaning Workflow

The project follows this general pipeline:

```text
Raw Data
   ↓
Data Profiling
   ↓
Column Standardization
   ↓
Text and Category Cleaning
   ↓
Missing Value Review
   ↓
Duplicate Detection
   ↓
Data Validation
   ↓
Quality-Control Reporting
   ↓
Tableau-Ready Dataset
```

### Project Structure

```text
missouri-cannabis-data/
│
├── data/
│   ├── raw/
│   │   └── Source files are stored here without modification
│   │
│   └── processed/
│       └── Cleaned datasets ready for analysis
│
├── reports/
│   ├── quality_report.csv
│   ├── duplicate_facilities.csv
│   └── rejected_rows.csv
│
├── scripts/
│   └── Python scripts used to clean and validate the data
│
├── tableau/
│   └── Tableau-related files and documentation
│
├── README.md
└── requirements.txt
```

### Data Integrity Principles

A major focus of this project is maintaining data traceability.

Raw source files are never overwritten. Instead, cleaned versions are created separately so transformations can be reproduced and reviewed.

Important fields may retain both their original and standardized versions, for example:

```text
facility_type_raw
facility_type
```

This makes it possible to verify how source values were transformed.

Missing values are also treated differently from zero values. A missing value means information is unknown, unavailable, or not reported, while a value of zero represents an actual observed value.

Duplicate records are reviewed before removal because repeated identifiers may represent legitimate updates, multiple locations, or source-data issues.

### Technology Stack

- **Python** — Data cleaning, transformation, and validation
- **Pandas** — Data manipulation and quality checks
- **Git/GitHub** — Version control and project documentation
- **Tableau** — Geographic visualization and interactive dashboards
- **CSV / GeoJSON** — Data exchange and spatial data formats

### Planned Data Sources

Potential data sources include:

- Missouri Department of Health and Senior Services — Division of Cannabis Regulation
- U.S. Census Bureau — American Community Survey
- Missouri geographic and open-data sources
- Public-health datasets from state and federal agencies

Only authoritative or clearly documented sources will be used for published analysis.

### Current Development Stage

The first phase focuses on creating a clean Missouri cannabis facility dataset suitable for mapping in Tableau.

Initial outputs will include:

```text
raw_facilities.csv
clean_facilities.csv
duplicate_facilities.csv
rejected_rows.csv
quality_report.csv
```

Future phases will incorporate additional datasets such as cannabis sales, recalls, demographic data, medical patient statistics, and public-health indicators.

### Long-Term Vision

The long-term goal is to create an independent Missouri cannabis data and education platform that helps residents, researchers, policymakers, and other stakeholders better understand the state's cannabis landscape through transparent data, interactive maps, and accessible educational tools.

This project is intended to prioritize evidence, data quality, and public understanding rather than cannabis marketing or product promotion.
