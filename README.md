# European STEM Master's Exploration

An end-to-end data analytics project exploring European STEM master's programs using Python, Selenium, Oracle SQL, Power BI, and Vertex AI.

The project covers the full data pipeline: web scraping, data cleaning, relational data modeling, dashboard development, and an AI-powered web interface.

# European STEM Master's Exploration

An end-to-end data analytics project exploring European STEM master's programs using Python, Selenium, Oracle SQL, Power BI, and Vertex AI.

The project covers the full data pipeline: web scraping, data cleaning, relational data modeling, dashboard development, and an AI-powered web interface.

---

## Project Overview

Information about European STEM master's programs is often scattered across different sources, inconsistent in structure, and difficult to compare.

This project was created to collect, clean, standardize, model, and analyze European STEM master's program data within a single analytical workflow.

The final solution combines:

- Web scraping with Python and Selenium
- Data cleaning and transformation with Python
- Relational modeling and normalization with Oracle SQL
- Interactive analytics with Power BI
- An AI-powered web interface using Vertex AI

---

## Objectives

The main objectives of the project were to:

- Build a consolidated dataset of European STEM master's programs.
- Standardize academic, financial, structural, and admissions-related information.
- Transform scraped web data into an analysis-ready format.
- Build a relational data model using Oracle SQL.
- Analyze program distribution, tuition, study formats, language requirements, and employability-related indicators.
- Develop an interactive Power BI dashboard for exploring program options.
- Build a Vertex AI-powered interface for interacting with the dataset.

---

## Data Source

The program data was collected from:

**Mastersportal**

The original web data was scraped and structured using Python and Selenium before being cleaned and transformed for further analysis.

---

## Project Workflow

The project follows the pipeline below:

```text
Mastersportal
      ↓
Python + Selenium Web Scraping
      ↓
Raw Excel Dataset
      ↓
Python Data Cleaning & Transformation
      ↓
Processed Dataset
      ↓
Oracle SQL Normalization
      ↓
Relational / Normalized Tables
      ↓
 ┌───────────────────────┐
 ↓                       ↓
Power BI             Vertex AI
Dashboard            Web Interface

1. Web Scraping

The first stage of the project involved collecting European STEM master's program data using Python and Selenium.

The scraper extracted program-level information from Mastersportal and stored the collected data in an Excel dataset.

Main files:

python/programs_scraper.ipynb
data/raw/mastersportal_ai_all.xlsx
2. Data Cleaning and Transformation

The scraped dataset required cleaning and standardization before it could be loaded into the SQL database.

Python was used to transform and standardize fields related to areas such as:

Degree information
Program duration
Languages
Language requirements
Study and delivery formats
Program disciplines
Locations
Tuition and cost-related fields
Admissions-related attributes

The cleaned dataset was then exported for SQL processing.

Main files:

python/data_cleaning.ipynb
data/processed/master_programs_mid.xlsx
3. SQL Data Modeling and Normalization

The cleaned dataset was loaded into Oracle SQL and transformed into a relational data model.

The normalization process separated the original flat dataset into multiple related entities such as:

Programs
Universities
Locations
Degrees
Disciplines
Languages
Study modes
Delivery types
Program intakes
Application deadlines
Language requirements

Junction tables were also used where many-to-many relationships were required.

Main SQL files:

sql/normalization.sql
sql/normalization_2.sql

The normalized output tables are available in:
data/normalized/

4. Power BI Dashboard

The normalized SQL output tables were imported into Power BI and connected through a relational data model.

The dashboard was designed to explore European STEM master's programs from multiple analytical perspectives.

The analysis includes areas such as:

Program distribution across Europe
Country and regional comparisons
Tuition and living-cost patterns
STEM discipline distribution
Study formats and delivery types
Language and admissions requirements
Internship and employability-related indicators
University and program-level exploration

The dashboard contains dedicated analytical pages including:

Programs Overview
Geography
Ecosystem & Employability
Financials & Learning Formats
Language & Admissions

The Power BI project file is available in:
powerbi/

Dashboard Demo

A recorded walkthrough of the Power BI dashboard is available here:

Watch the Power BI Dashboard Demo

5. Vertex AI Interface

A Vertex AI-powered chatbot interface was developed to support interactive exploration of the European STEM master's dataset.

The frontend files are available in:
vertex-ai/

Web Interface

Open the Vertex AI Web Interface

Key Analytical Questions

The project was designed to support questions such as:

Which European countries offer the highest concentration of STEM master's programs?
How do tuition and living costs vary between countries?
Which STEM disciplines are most widely represented?
What study and delivery formats are available?
How do language and admissions requirements vary?
Which countries provide stronger employability-related ecosystems?
Target Audience

The project is designed for several potential user groups:

Students comparing STEM master's opportunities across Europe
Universities and program managers analyzing market positioning and program density
Scholarship and funding institutions working with academic and financial program information
Technologies Used
Technology	Purpose
Python	Data scraping, cleaning, and transformation
Selenium	Automated web data collection
Pandas	Data manipulation and preprocessing
Oracle SQL	Data normalization and relational modeling
Power BI	Data modeling, analysis, and dashboard development
Vertex AI	AI-powered dataset exploration
HTML	Web interface
GitHub Pages	Publishing the web interface
Excel	Intermediate and normalized datasets

Repository Structure
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
│   │   └── mastersportal_ai_all.xlsx
│   │
│   ├── processed/
│   │   └── master_programs_mid.xlsx
│   │
│   └── normalized/
│       └── normalized SQL output tables
│
├── powerbi/
│   └── Power BI dashboard file
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

A complete presentation covering the project motivation, methodology, scraping process, SQL normalization, data model, Power BI analysis, and AI chatbot is available in:
presentation/

End-to-End Process

In summary, the project demonstrates an end-to-end data analytics workflow:

Data Collection → Data Cleaning → Data Transformation → SQL Modeling → Business Intelligence → AI Interface

Rather than analyzing an already prepared dataset, the project begins with collecting raw web data and continues through each stage required to transform that data into an analytical product.
