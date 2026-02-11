# Panic-Attack-Data-Analysis
This project analyzes a Panic Attack Dataset using a complete data pipeline—from ingestion and cleaning in Snakeflow (SQL workspace) to building a multi-page Power BI report. The goal was to clean the dataset, prepare analytical features, and build an interactive dashboard to uncover patterns in age groups, symptoms, triggers, and attack frequency.


## Project Overview

The goal of this project was to clean, model, and visualize a real-world panic attack dataset to uncover insights into:
- Symptom frequency and severity
- Age-group-specific behavior and panic patterns
- Lifestyle factors influencing panic attacks
- Trigger reasons and medical history impact
- Demographic differences (gender, age, etc.)

This is an end-to-end BI project demonstrating SQL skills, data modeling, Power Query transformations, and advanced Power BI reporting.

## Project Workflow

### 1. Data Ingestion (Snakeflow)

- Uploaded raw Panic Attack Dataset into Snakeflow workspace.
- Performed initial inspection (column types, missing values, outliers).
- Created staging tables for clean data processing.

### 2. Data Cleaning & Transformation (SQL – Snakeflow)

Used SQL to clean and prepare data:
- Removed duplicates and invalid rows
- Standardized numeric and date fields
- Cleaned inconsistent category labels
- Filled missing values where appropriate
- Validated distribution of cleaned fields
- Created final cleaned table for BI reporting

### 3. Connecting Power BI to SQL Server (Snakeflow)

- Established a direct connection from Power BI to Snakeflow server.
- Imported final cleaned table(s).
- Ensured refreshable, server-based data pipeline.


### 4. Power Query Transformations (Power BI)
Performed final shaping and data quality checks:

- Corrected data types
- Removed errors & duplicates
- Handled nulls
- Used Column Distribution, Column Quality, and Column Profile
- Ensured fields were optimized for DAX modeling (numeric → whole/decimal, date, text)

These steps ensured a clean, reliable model before building the dashboard.

### 5. DAX Modeling

Created multiple calculated columns and measures for analysis:
- Calculated Columns
- Age Group categorization (Teen, Young Adult, Adult, Senior)
- Panic score buckets
- Binary flags for symptoms, triggers, and medical conditions
- DAX Measures
    - COUNTROWS() – for number of patients
    - FILTER() – conditional filtering of symptoms/triggers
    - DIVIDE() – safe division for percentage metrics
    - IF() & SWITCH() – category creation and logic branching

### 6. Power BI Dashboard

The final Power BI report consists of four detailed analytical pages, each addressing a specific part of the dataset.

#### Symptoms Analysis

- Deep dive into the physical symptoms associated with panic attacks.
- Symptoms analyzed:
    - Dizziness
    - Trembling
    - Sweating
    - Shortness of breath
    - Chest pain
- Charts used:
    - Bar charts for symptom prevalence
    - Clustered charts comparing symptom frequency by gender or age
    - Cards showing total cases with each symptom
- Purpose:
    - Identify which symptoms are most common
    - Compare symptom patterns across demographics
    - Understand symptom clusters connected to severe panic scores

#### Filters, Lifestyle Factors & Panic Patterns

This page highlights interactive exploration:

- Slicers Added
    - Gender
    - Panic Score Scale
    - Trigger Reason
    - Medical History

- Visualizations
    - Number of Sleep Hours (bar chart)
    - Patients by Panic Attack Duration (minutes)
    - Patients by Drinks Per Week
    - Additional charts tied dynamically to slicers

- Purpose:
    - Understand how lifestyle variables (sleep, alcohol intake) influence attacks
    - Explore medical history & triggers in combination
    - Correlate panic severity with behavioral metrics

This page is heavily interactive and built for exploratory analysis.

#### Age Group Analysis

A complete age-segmented breakdown created using DAX-based Age Groups.
- Metrics Compared by Age Group
    - Average Sleep Hours
    - Average Panic Score
    - Panic Attack Frequency

- Visuals Used
    - Clustered bar charts for side-by-side comparison
    - KPI cards summarizing age-specific values

- Purpose:
    - Identify which age category faces the most severe panic attacks
    - Compare lifestyle habits (e.g., sleep) by age
    - Understand age-related psychological patterns

### Tools & Technologies
- SQL (Snakeflow)
- Power BI Desktop
- Power Query
- DAX
- ETL Concepts
- Data Profiling & Validation
- Data Modeling

### Key Outcomes & Insights
- Identified major physical symptoms associated with panic disorder
- Highlighted lifestyle contributors such as low sleep hours and higher drinking frequency
- Showed how demographic factors influence symptom severity
- Revealed age groups most vulnerable to severe panic patterns
- Built a completely interactive and dynamic BI report for stakeholders
