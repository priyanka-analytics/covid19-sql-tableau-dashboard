# COVID-19 Global Analysis Dashboard

![COVID-19 Dashboard Thumbnail](![COVID-19 Dashboard Thumbnail](Images/covid_dashboard_thumbnail.png))

This project presents a comprehensive data analysis and visualization of the COVID-19 pandemic using SQL Server and Tableau. It explores global trends in infections, death rates, and vaccination progress to provide meaningful insights into how different regions were impacted.

---

## Project Overview

- **Objective:** Transform raw COVID-19 data into actionable insights through structured querying and interactive dashboards.
- **Tools Used:** SQL Server, Tableau Desktop, Microsoft Excel
- **Data Source:** [Our World in Data – COVID-19 Dataset](https://ourworldindata.org/coronavirus)

---

## Repository Structure

| Folder/File | Description |
|-------------|-------------|
| `data/`     | Raw Excel data files: CovidDeaths.xlsx and CovidVaccinations.xlsx |
| `sql/`      | SQL scripts used for cleaning and analysis |
| `images/`   | Thumbnail for dashboard branding |
| `README.md` | Project overview, SQL highlights, and dashboard link |

---

## Key Analytical Focus Areas

- Global and regional death rate analysis
- Infection rates as a percentage of population
- Top countries by total deaths
- Vaccination trends by location and over time
- Time-series visualization of new cases, deaths, and vaccine rollout

---

## SQL Development Highlights

The SQL script (`sql/covid_analysis_queries.sql`) includes:

- Joins between death and vaccination datasets
- Aggregations by location and time
- Rolling totals using window functions
- Population-normalized metrics like infection and death percentage


**Sample Query:**

SELECT 
    SUM(new_cases) AS total_cases,
    SUM(CAST(new_deaths AS INT)) AS total_deaths,
    SUM(CAST(new_deaths AS INT)) * 100.0 / SUM(new_cases) AS DeathPercentage
FROM PortfolioProject..CovidDeaths
WHERE continent IS NOT NULL;




## Tableau Dashboard
The final dashboard includes:

- KPI metrics for global COVID-19 impact  
- Filters for region, date, and population size  
- Visualizations of death counts, infection spread, and vaccination progress

**Live Dashboard:**  
[View the Tableau Dashboard](https://public.tableau.com/app/profile/saipriyanka.annadasus/viz/CoronavirusCOVID-19Dashboard_17522507164750/Dashboard1?publish=yes)




## Author

**Sai Priyanka Annadasu**  
Graduate Student | Data Analyst | BI Enthusiast  
[Tableau Public Profile](https://public.tableau.com/app/profile/saipriyanka.annadasus)

---

You can use this version in your GitHub README.  
Let me know once you’ve updated it and then we’ll move on to publishing your Medium blog!


