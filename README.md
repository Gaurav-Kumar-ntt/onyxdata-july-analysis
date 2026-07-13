# Onyx Data July Challenge Analysis

This repository contains data preparation and analysis for the Onyx Data July Challenge focused on workforce AI adoption metrics.

## Project Structure

```
├── data/                               # Raw data files
│   ├── dim_country.csv                # Country dimension (30 countries)
│   ├── dim_date.csv                   # Date dimension
│   ├── dim_industry.csv               # Industry dimension
│   ├── dim_skill_category.csv         # Skill category dimension
│   ├── fact_workforce_ai_index.csv    # Fact table with AI adoption metrics
│   └── star_schema_final.csv          # Final joined star schema
├── july_challenge_data_prep.ipynb     # Data preparation notebook
└── README.md                          # This file

## Data Model

The project implements a **star schema** design with:

* **Fact Table**: `fact_workforce_ai_index` - Contains workforce AI adoption metrics
* **Dimension Tables**:
  - `dim_country` - Country attributes (region, development tier, GDP, infrastructure)
  - `dim_date` - Time dimension
  - `dim_industry` - Industry classifications
  - `dim_skill_category` - AI skill categories

## Notebook Overview

`july_challenge_data_prep.ipynb` performs the following steps:

1. **Data Loading**: Reads all CSV files into pandas DataFrames
2. **Schema Inspection**: Examines data structure and types
3. **Star Schema Creation**: Joins fact table with dimension tables
4. **Data Cleaning**: Removes unnecessary ID columns
5. **Export**: Saves final denormalized table for analysis

## Key Columns in Final Dataset

* Country attributes: region, development tier, GDP per capita, digital infrastructure score
* Industry information
* Skill categories
* AI adoption metrics and indices
* Temporal data

## Usage

Open `july_challenge_data_prep.ipynb` in Databricks to run the data preparation pipeline.

## Author

Gaurav Kumar
