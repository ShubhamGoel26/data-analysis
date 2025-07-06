# COVID-19 Data Analysis and Visualization

This project analyzes the global impact of COVID-19 using SQL and Tableau, leveraging the [Our World in Data COVID-19 dataset](https://github.com/owid/covid-19-data). It demonstrates advanced data analysis with complex SQL queries (including joins, CTEs, and subqueries) executed in DBeaver and interactive visualizations created in Tableau.

## Project Overview
- **SQL Analysis**: Developed 10 SQL queries to uncover trends such as case growth, policy impacts, testing efficiency, and economic correlations.
- **Tableau Visualizations**: Built two interactive dashboards (`covid_dashboard.twb` and `covid_dashboard_2.twb`) with charts like scatter plots, line charts, and heat maps to visualize key insights.
- **Tools**: DBeaver (SQLite), Tableau Desktop, GitHub.
- **Dataset**: `owid-covid-data.csv` from Our World in Data.

## Dataset
- **Source**: [Our World in Data COVID-19 Dataset](https://github.com/owid/covid-19-data)
- **Key Columns**: `date`, `location`, `continent`, `total_cases`, `new_cases`, `total_deaths`, `new_deaths`, `new_tests`, `stringency_index`, `gdp_per_capita`, `population`.
- **Structure**: Data was split into three SQLite tables (`cases`, `demographics`, `policies`) for relational analysis with joins.

## SQL Analysis
The SQL analysis includes:
1. **Simple Queries** (`/sql/covid_analysis.sql`):
   - Total cases and deaths by country.
   - Daily new cases trend (global).
   - Death rate by country.
2. **Advanced Queries with Joins** (`/sql/advanced_covid_joins.sql`):
   - Case growth vs. economic wealth (joining `cases` and `demographics`).
   - Policy stringency vs. case trends (joining `cases` and `policies`).
   - Continent-level case density (aggregating with joins).
   - Testing efficiency in high-population countries (cross join).
   - Death rates by income level (join with subquery).
   - Policy change impact on cases (self-join on `policies`).
   - Peak case periods by continent (join with subquery).

## Tableau Dashboards
Two dashboards were created to visualize the SQL insights:
- **covid_dashboard.twb**:
  - Visualizations: Line chart (daily new cases), bar chart (total cases by country), and map (case density).
  - Focus: Basic trends from `covid_analysis.sql`.
- **covid_dashboard_2.twb**:
  - Visualizations: Scatter plot (case growth vs. GDP), line chart (stringency vs. cases), area chart (cases per million by continent), bar chart (testing efficiency), line chart (death rates by income), table (policy impact), and heat map (case surges).
  - Focus: Advanced trends from `advanced_covid_joins.sql`.
- **Interactivity**: Filters for `location`, `continent`, and `date`; parameters for metric toggling.
- **View Online**: [Tableau Public Link](your-tableau-public-link) (replace with your published URL if applicable).

## Setup Instructions
1. **Download Dataset**:
   - Download `owid-covid-data.csv` from the dataset source.
2. **Set Up SQLite in DBeaver**:
   - Install DBeaver from [dbeaver.io](https://dbeaver.io).
   - Create a new SQLite database (`covid.db`).
   - Import the CSV into a `covid_data` table using SQLite command line:
     ```bash
     sqlite3 covid.db
     .mode csv
     .import owid-covid-data.csv covid_data
     ```
   - Create relational tables (`cases`, `demographics`, `policies`) by running the table creation queries from `advanced_covid_joins.sql` in DBeaver’s SQL Editor.
3. **Run SQL Queries**:
   - Open `covid_analysis.sql` and `advanced_covid_joins.sql` in DBeaver.
   - Execute each query (Ctrl+Enter) to view results.
4. **View Tableau Dashboards**:
   - Open `covid_dashboard.twb` and `covid_dashboard_2.twb` in Tableau Desktop.
   - Alternatively, view on Tableau Public (link above).

## Files
- `/sql/covid_analysis.sql`: Initial simple SQL queries.
- `/sql/advanced_covid_joins.sql`: Advanced queries with joins, CTEs, and subqueries.
- `/tableau/covid_dashboard.twb`: Basic dashboard with core visualizations.
- `/tableau/covid_dashboard_2.twb`: Advanced dashboard with complex visualizations.
- `/data`: (Optional) Reference to `owid-covid-data.csv`.

## Resume Highlight
This project showcases proficiency in:
- **SQL**: Complex queries with joins, CTEs, and subqueries for relational data analysis.
- **Tableau**: Interactive dashboard creation with advanced visualizations and storytelling.
- **Tools**: DBeaver for database management, Tableau for visualization, GitHub for version control.

## Future Improvements
- Add time-series forecasting for case trends.
- Incorporate additional datasets for deeper analysis (e.g., vaccination data).
- Enhance the Tableau story with more narrative points.

For questions or feedback, contact [Your Name] at [Your Email] or via [LinkedIn](your-linkedin-link).