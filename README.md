# European STEM Master's Exploration

**An end-to-end data analytics project that transforms raw European STEM master's program data collected from the web into a normalized relational model, an interactive Power BI dashboard, and a Vertex AI-powered exploration interface.**

[Power BI Demo](demo/powerbi_dashboard_demo.mp4) • [AI Web Interface](https://time4lord.github.io/vertex-widget/) • [Project Presentation](presentation/european_stem_masters_presentation.pptx)

---

## Overview

European STEM master's program information is often scattered across different sources and difficult to compare consistently.

This project builds a complete analytics pipeline from raw web data to an interactive analytical product. Program information was collected from Mastersportal, cleaned and standardized with Python, normalized into relational tables using Oracle SQL, analyzed in Power BI, and connected to a Vertex AI-powered web interface.

**Tech Stack:**  
Python · Selenium · Pandas · Oracle SQL · Power BI · Vertex AI · HTML · GitHub Pages

---

## Project Pipeline

```text
Mastersportal
      ↓
Python + Selenium
Web Scraping
      ↓
Raw Dataset
      ↓
Python
Cleaning & Transformation
      ↓
Processed Dataset
      ↓
Oracle SQL
Normalization & Relational Modeling
      ↓
Normalized Tables
      ↓
 ┌───────────────────────┐
 ↓                       ↓
Power BI             Vertex AI
Dashboard            Web Interface
```

---

## What I Built

### 1. Web Scraping

Program-level data was collected from Mastersportal using Python and Selenium.

The scraping workflow captured raw master's program information and exported it into an Excel dataset for further processing.

**Files**
- [`programs_scraper.ipynb`](python/programs_scraper.ipynb)
- [`mastersportal_ai_all.xlsx`](data/raw/mastersportal_ai_all.xlsx)

---

### 2. Data Cleaning & Transformation

The scraped dataset was cleaned and standardized with Python and Pandas before being loaded into SQL.

The transformation process included fields related to:

- Degree types
- Program duration
- Languages
- Language requirements
- Study and delivery formats
- Disciplines
- Locations
- Tuition and cost-related information
- Admissions-related attributes

**Files**
- [`data_cleaning.ipynb`](python/data_cleaning.ipynb)
- [`master_programs_mid.xlsx`](data/processed/master_programs_mid.xlsx)

---

### 3. Oracle SQL Data Modeling

The cleaned flat dataset was transformed into a normalized relational model in Oracle SQL.

The final model separates major entities including:

- Programs
- Universities
- Locations
- Degrees
- Disciplines
- Languages
- Study modes
- Delivery types
- Program intakes
- Application deadlines
- Language requirements

Junction tables were used to model many-to-many relationships between entities.

**SQL Scripts**
- [`normalization.sql`](sql/normalization.sql)
- [`normalization_2.sql`](sql/normalization_2.sql)

The resulting normalized tables are stored in:

[`data/normalized/`](data/normalized/)

---

### 4. Power BI Dashboard

The normalized SQL output tables were imported into Power BI and connected through a relational data model.

The dashboard provides multiple analytical views of the European STEM master's landscape.

**Dashboard Pages**
- Programs Overview
- Geography
- Ecosystem & Employability
- Financials & Learning Formats
- Language & Admissions

**Analysis Areas**
- Program distribution across European countries
- Tuition and living-cost patterns
- Discipline distribution
- Study modes and delivery formats
- Language and admissions requirements
- Internship-related indicators
- Employability-related patterns
- University and program-level exploration

**Power BI File**  
[`powerbi/`](powerbi/)

**Dashboard Walkthrough**  
[Watch the Power BI Dashboard Demo](demo/powerbi_dashboard_demo.mp4)

---

### 5. Vertex AI Interface

A Vertex AI-powered web interface was developed to support interactive exploration of the European STEM master's dataset.

The frontend implementation is included in:

[`vertex-ai/`](vertex-ai/)

**Web Interface**  
[Open the Vertex AI Interface](https://time4lord.github.io/vertex-widget/)

---

## Key Analytical Questions

The project supports exploration of questions such as:

- Which European countries have the highest concentration of STEM master's programs?
- How do tuition and living costs vary across countries?
- Which STEM disciplines are most widely represented?
- How do study formats, language requirements, and admissions conditions differ across programs?
- Which countries show stronger employability-related ecosystems?

---

## Repository Structure

```text
european-stem-masters-analysis/
│
├── python/
│   ├── programs_scraper.ipynb
│   └── data_cleaning.ipynb
│
├── sql/
│   ├── normalization.sql
│   └── normalization_2.sql
│
├── data/
│   ├── raw/
│   ├── processed/
│   └── normalized/
│
├── powerbi/
│   └── Power BI dashboard
│
├── demo/
│   └── powerbi_dashboard_demo.mp4
│
├── presentation/
│   └── project presentation
│
├── vertex-ai/
│   ├── index.html
│   └── vercel.json
│
└── README.md
```

---

## Project Presentation

The complete presentation covers the project motivation, scraping process, data transformation, SQL normalization, data model, Power BI analysis, and AI interface.

[View the Project Presentation](presentation/european_stem_masters_presentation.pptx)

---

## Summary

This project demonstrates a complete analytics workflow starting with raw web data and ending with a structured analytical solution.

**Web Data Collection → Data Cleaning → SQL Modeling → Power BI Analysis → AI-Powered Exploration**
