# Austria market analysis (R)

Group project (Group 7), Lab I: Market Analysis, Università di Trento — December 2024.

## Question
How attractive is the Austrian sweet-snacks market (biscuits, snack bars, fruit snacks) for a new entrant, compared with other European countries?

## What the code does
- **Data collection:** pulls macro and demographic series directly from the Eurostat API (`eurostat` package) and combines them with industry datasets (market volumes, values, prices, firm-level financials).
- **Data preparation:** cleaning, reshaping (`pivot_longer` / `pivot_wider`), joins across sources, and merging municipal shapefiles with population data (`sf`).
- **Analysis:**
  - Demand side: population structure, unemployment by region and age, GDP per capita, food consumption, income and consumption, price comparison and demand curves across countries.
  - Supply side: number of enterprises, employees, hours worked, investment and capital intensity, cost structure.
  - Market structure: market shares, private labels, concentration ratios (C4) and the Herfindahl–Hirschman Index (custom `calculate_hhi()` function).
  - Financial position of the main players: net income, return on sales, return on equity.
- **Output:** maps, time-series and cross-country charts (`ggplot2`) and formatted tables (`kableExtra`).

## Files
- `austria_market_analysis.Rmd` — R Markdown source
- `austria_market_analysis.html` — knitted report with all charts and tables

## Reproducing
The Eurostat series download automatically. The industry datasets and shapefiles used in the course (`Dataset_Market_Analysis_Austria_G7/`) were provided by the course and are not included; set the working directory to a folder containing them before knitting.
