# IBM Data Analyst Capstone — Developer Ecosystem Analysis 2024

**Kwesi Designs | June 2026**  
IBM Data Analyst Professional Certificate Capstone Project

---

## Project Overview

This capstone analyzes technology trends from the **2024 Stack Overflow Developer Survey** to identify current and future preferences across programming languages, databases, cloud platforms, and web frameworks. Data was collected via REST API calls, web scraping, and survey datasets, then visualized using Python and IBM Cognos Analytics.

---

## Key Findings

- **PostgreSQL** dominates both current and desired database usage
- **JavaScript** remains the most widely used language, but desire is shifting toward TypeScript
- **Go and Rust** are rising fast in desired adoption despite lower current usage
- **AWS** leads cloud platform adoption; Cloudflare is the fastest-rising alternative
- **React and Node.js** lead web frameworks; **Next.js** shows strong future momentum
- Legacy tools (jQuery, PHP, Oracle) show declining desired usage — a hiring risk signal

---

## Repository Structure

```
ibm-data-analyst-capstone/
│
├── notebooks/
│   └── IBM_Capstone_Full_Analysis.ipynb   # Full analysis: API, scraping, survey processing
│
├── data/
│   ├── popular-languages.csv              # Scraped language salary data
│   ├── job-postings.xlsx                  # Job counts by city (from Jobs API)
│   └── job-skills.xlsx                    # Job counts by technology skill (from Jobs API)
│
├── exports/                               # Top-10 CSVs for IBM Cognos dashboards
│   ├── tab_1_csv_language_top10.csv
│   ├── tab_1_csv_database_top10.csv
│   ├── tab_1_csv_platform_top10.csv
│   ├── tab_1_csv_webframe_top10.csv
│   ├── tab_2_csv_language_want_top10.csv
│   ├── tab_2_csv_database_want_top10.csv
│   ├── tab_2_csv_platform_want_top10.csv
│   └── tab_2_csv_webframe_want_top10.csv
│
├── presentation/
│   └── Developer_Ecosystem_Analysis_2024.pdf
│
└── README.md
```

---

## Notebook Sections

| Part | Description | Output |
|------|-------------|--------|
| Part 1 — Jobs API | Fetches open job postings by technology skill and city | `job-postings.xlsx`, `job-skills.xlsx` |
| Part 2 — Web Scraping | Scrapes programming language average annual salary data | `popular-languages.csv` |
| Part 3 — Survey Processing | Processes Stack Overflow survey; generates top-10 counts per category | 8 CSV files in `exports/` |

---

## Tools & Technologies

- **Python** — pandas, requests, BeautifulSoup, openpyxl
- **IBM Cognos Analytics** — 3-tab interactive dashboard (Current Usage, Future Trends, Demographics)
- **Data Source** — [2024 Stack Overflow Developer Survey](https://survey.stackoverflow.co/)
- **IBM Skills Network** — Jobs API endpoint, hosted dataset

---

## Dashboard Tabs

| Tab | Charts |
|-----|--------|
| Current Technology Usage | Top 10 Languages (bar), Top 10 Databases (column), Top 10 Platforms (word cloud), Top 10 Web Frameworks (bubble) |
| Future Technology Trend | Top 10 Languages (bar), Top 10 Databases (column), Top 10 Platforms (tree map), Top 10 Web Frameworks (bubble) |
| Demographics | Age distribution (pie), Respondents by country (map), Education level (line), Age × Education (stacked bar) |

---

## How to Run the Notebook

1. Clone this repo
2. Download `survey_data_updated.csv` from the [IBM Skills Network dataset](https://cf-courses-data.s3.us.cloud-object-storage.appdomain.cloud/IBM-DA0321EN-SkillsNetwork/LargeData/m1_survey_data.csv) and place it in the root directory
3. Install dependencies:
   ```bash
   pip install pandas requests beautifulsoup4 openpyxl
   ```
4. Open `notebooks/IBM_Capstone_Full_Analysis.ipynb` and run all cells

---

## Certificate

IBM Data Analyst Professional Certificate — Coursera  
[View Certificate](https://coursera.org/share/7ff1b11bbe1327c2e8d815bbcdf52150)
