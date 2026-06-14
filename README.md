# College Search Data Scraper

This repo contains a Selenium and BeautifulSoup data pipeline that collects college search results, follows each college profile, extracts admissions, academics, and campus-life fields, then writes the results to a structured CSV.

It is a compact data-engineering sample: the code handles dynamic page loading with Selenium, uses direct HTTP requests for detail pages, normalizes mixed profile fields, and saves a reusable dataset for downstream analysis.

## What it demonstrates

- Selenium automation for dynamic search result pages.
- BeautifulSoup parsing for structured profile extraction.
- CSV export with a stable schema across multiple college sections.
- Missing-field handling for partially populated source pages.
- A repeatable script that turns web content into analysis-ready tabular data.

## Tech stack

- Python
- Selenium
- BeautifulSoup
- Requests
- CSV

## Run locally

Install dependencies:

```bash
python -m venv .venv
.venv\Scripts\activate
pip install -r requirements.txt
```

Make sure Chrome and a compatible ChromeDriver are available, then run:

```bash
python app.py
```

The script writes results to `colleges_data.csv`.

## Output schema

The generated CSV includes college name, URL, admissions fields, academic fields, campus-life details, housing options, activity listings, and student-body summaries.

## Responsible use

This project is intended as a learning and portfolio example. Before running a scraper against any public site, review the site's terms, respect rate limits, and avoid collecting private or restricted data.

## Reviewer notes

The most relevant engineering signal is the pipeline shape: browser automation for dynamic discovery, lightweight HTTP parsing for detail pages, and a consistent CSV output that can feed search, ranking, or analytics features.
