🇺🇸 U.S. County-Level Emissions Analytics | Databricks




An end-to-end analytics project exploring U.S. county-level greenhouse-gas emissions and related demographic and energy indicators using Databricks. The project turns a county-level 2023 dataset into an interactive dashboard for geographic exploration, comparisons, and identification of high-emitting counties and states.
Dashboard: Open the published Databricks dashboard
Access to the live dashboard may depend on Databricks workspace permissions.

Dashboard preview

The dashboard currently presents:
- Emissions by location: geographic distribution across U.S. counties.
- Emissions vs. population: a county-level comparison of emissions per person and population.
- State emissions share: a donut chart comparing state-level contributions.
- Highest-emitting counties: a ranked view of counties by total emissions.
Project highlights
The supplied CSV contains 3,142 county-level records and 58 fields, including geography, population, employment, energy consumption, utility customers, greenhouse-gas emissions, water consumption, and vehicle miles travelled.

A quick validation of the supplied source file shows:
- 562.46 million metric tons CO₂e in total across the county records.
- Maricopa County, Arizona has the highest recorded emissions in the supplied file, at approximately 9.81 million metric tons CO₂e.
- The ten highest-emitting states in aggregate account for approximately 50.9% of the total emissions represented in the file.
These figures are calculated from the supplied Emissions_Data_2023.csv file. They describe the dataset and should not be interpreted as independently verified national inventory estimates.
Business questions explored
1. How are greenhouse-gas emissions distributed geographically across U.S. counties?
2. Which counties contribute the largest total emissions?
3. How does population relate to county-level emissions and emissions per person?
4. How concentrated are emissions across states?
5. Which locations may warrant deeper investigation based on their emissions profile?
Dataset
File: Emissions_Data_2023.csv
Coverage shown in dashboard: U.S. county-level emissions data collected by the Environmental Protection Agency (EPA) for 2023.

The dataset includes fields such as:
- Geography: state, county, county identifier, latitude and longitude.
- Demographics: population and employment.
- Energy: electricity and natural-gas consumption, utility customers and expenditure measures.
- Environment: greenhouse-gas emissions in metric tons of CO₂ equivalent.
- Other activity indicators: water consumption and vehicle miles travelled.
The original dataset contains some columns that are entirely blank (for example, buildings, area (sq. ft.), and establishments). These should be treated as unavailable in this extract rather than as zero values.
Workflow and architecture
The project follows this analytical flow:
EPA 2023 county-level dataset (CSV)
                 |
                 v
        Databricks workspace
                 |
                 v
     Data preparation & analysis
                 |
                 v
     Analytical queries / metrics
                 |
                 v
      Databricks AI/BI Dashboard
                 |
                 v
       Geographic & business insights
The repository documentation and notebooks should describe the exact ingestion, cleaning, transformation, and modelling steps implemented in the workspace. Avoid describing a Bronze/Silver/Gold architecture, Delta Lake pipeline, or production deployment unless those components are present in the actual implementation.
Technology
Technology	Role in this project
Databricks	Data workspace and dashboard platform
Databricks AI/BI Dashboards	Interactive data visualization
CSV	Source data format
SQL / PySpark	Add the specific language(s) used in your notebooks


Repository structure
databricks-us-emissions-analytics/
├── README.md
├── data/
│   └── Emissions_Data_2023.csv
├── notebooks/
│   └── add-your-exported-databricks-notebooks-here
├── assets/
│   └── emissions-dashboard.png
└── docs/
    └── data-dictionary.md
If the source dataset is large or subject to redistribution restrictions, do not commit it to GitHub. Instead, add instructions describing where to obtain it and how to upload it to Databricks.

Reproducing the project
1. Clone this repository.
2. Upload the source CSV to your Databricks workspace or an accessible volume.
3. Open and run the exported notebooks in the documented order.
4. Confirm that the resulting analytical tables or views are created.
5. Import or recreate the dashboard using the documented queries and data sources.
Note: Add the actual notebook names, execution order, catalog/schema/table names, and required permissions before presenting this as a fully reproducible project.
Key takeaways
This project demonstrates how a broad county-level environmental dataset can be organized into an interactive analytical experience. It combines geographic analysis, emissions benchmarking, population comparisons, and state-level contribution analysis to make the data easier to explore and interpret.
Author
Mohit Dutta
People Analytics | Data & Business Analytics | Databricks | SQL | Power BI | Microsoft Fabric
- LinkedIn: (https://www.linkedin.com/in/dmohit1/)
