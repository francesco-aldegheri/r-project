# Technical changes and Formula 1 car performance (R)

Course project, Introduction to Computer Programming for Economics and Management, Università di Trento — May 2024.

## Question
How did the technical regulation changes between 2020 and 2023 affect the performance of F1 cars?

## What the code does
- **Data collection:** downloads lap-level and telemetry data for qualifying and race sessions through the `f1dataR` package (an R interface to the Python FastF1 library).
- **Qualifying analysis:** for the fastest qualifying laps, compares average RPM, maximum speed, full-throttle share and final lap time across seasons (2020→2021, 2021→2022, 2022→2023).
- **Race analysis:** measures performance consistency with the standard deviation of lap times (excluding laps slower than 110% of the fastest lap) and compares mean speed at given throttle positions.
- **Interpretation:** links the measured differences to the specific rule changes of each season (floor design, minimum weight, tyres, the 2022 ground-effect regulations).

## Files
- `f1_technical_changes.Rmd` — R Markdown source
- `f1_technical_changes.html` — knitted report with all charts

## Reproducing
Install `f1dataR` and run `setup_fastf1()` once; the data are downloaded automatically when the document is knitted.
