# British Airways Passenger CSAT Dashboard

## Project Overview
This project analyzes British Airways passenger satisfaction survey data to uncover patterns in customer experience across service categories, aircraft types, seat classes, traveller types, and geographic regions. The goal was to build an interactive Tableau dashboard that allows stakeholders (Flight Operations, Maintenance, and Business Analyst teams) to explore CSAT (Customer Satisfaction) data and identify actionable insights for improving flight operations.

This was completed as part of a Data Analytics internship project with Labmentix.

## Business Problem
British Airways collects large volumes of customer feedback through surveys covering categories such as overall rating, seat comfort, cabin staff service, food, ground service, value for money, and entertainment. The goal of this dashboard is to:
- Detect patterns in passenger satisfaction and dissatisfaction
- Support flight operations decisions using CSAT data segmented by aircraft, seat type, and traveller type
- Provide an interactive, filterable view for non-technical stakeholders

## Datasets
- **ba_reviews.csv** — Individual passenger reviews with ratings across 7 service categories (~[X] rows)
- **Countries.csv** — Reference table mapping country, region, and continent, used for geographic visualization

The two datasets are connected via a relationship on `Place` (ba_reviews) and `Country` (Countries).

## Tools Used
- **Tableau Desktop / Tableau Public** — dashboard build and visualization
- **Data cleaning** — handled within Tableau (data type correction, geographic role assignment)

## Data Preparation
- Assigned `Place` a Geographic Role (Country/Region) to enable map plotting
- Set correct aggregation (Average) for all rating measures
- Connected `ba_reviews.csv` and `Countries.csv` via relationship (Place = Country)

## Dashboard Components
1. **Summary KPI Cards** — Average rating across 7 categories: Overall Rating, Cabin Staff Service, Entertainment, Food & Beverages, Ground Service, Seat Comfort, and Value for Money
2. **Interactive Map** — Country-level average rating, color-coded (dark blue = higher satisfaction, red/pink = lower satisfaction)
3. **Filters** — Aircraft, Traveller Type, and Seat Type, allowing users to drill down into specific segments
4. **Trend Line Chart** — Average rating by month, showing satisfaction trends over time
5. **Aircraft Rating Bar Chart** — Average rating broken down by aircraft type

## Key Insights
- **Declining satisfaction over time**: Average rating has trended downward from around 7.0 in 2015 to approximately 2.5–4.0 in recent years, suggesting a need to investigate service quality changes over time.
- **Category-level gaps**: Overall Rating (4.19) scores notably higher than categories like Entertainment (1.4), indicating in-flight entertainment as a potential area for improvement.
- **Aircraft-level variation**: Average ratings vary by aircraft type, which may reflect differences in cabin configuration, age of aircraft, or crew assignment.
- **Geographic spread**: Reviews span 200+ countries, with a visible concentration of both reviews and lower ratings in specific regions, useful for route-level investigation.

## Known Data Limitations
- The `Aircraft` field contains inconsistent entries (e.g., combined values like "A319/Boeing 787-8"), which affects the granularity of the aircraft-level analysis. These were not deep-cleaned in this iteration to preserve authenticity of the raw survey data.

## Files in This Repository
- `BA_CSAT_Dashboard.twbx` — Packaged Tableau workbook (data + dashboard)
- `README.md` — This documentation file

## Author
Leshyatha
B.Tech CSE, Sasi Institute of Technology and Engineering
Data Analytics Intern, Labmentix
