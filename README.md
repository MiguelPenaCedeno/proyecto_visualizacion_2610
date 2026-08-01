# Global Development Dashboard

Interactive data visualization dashboard exploring the relationship between happiness, peace, and Olympic performance across countries. Built for a Data Visualization course at Pontificia Universidad Javeriana.

**Live demo:** [proyectovisualizacion2610.vercel.app](https://proyectovisualizacion2610.vercel.app)

## Overview

This project combines three public datasets, the World Happiness Report, the Global Peace Index, and Olympic Games results, into a single analytical model, then presents the findings through an interactive dashboard with cross filtering. The goal was to investigate whether measurable factors like national peace and wellbeing correlate with a country's presence and performance on the Olympic stage.

## Data pipeline

- Raw data ingested from three independent public sources (`datos crudos/`)
- Cleaned and transformed with pandas in a Jupyter notebook (`ETL.ipynb`)
- Modeled into a star schema to support multi dimensional analysis (`datos transformados/`)
- Entity relationship diagram and star schema documented in `Anexos diagramas y modelos.docx`

## Dashboard and visual design

The dashboard combines five chart types, each chosen deliberately based on the analytical task it needs to support, following Munzner's visualization design framework:

- Line chart, for trends over time
- Box plot, for distribution and outlier comparison across countries
- Lollipop chart, for ranked comparisons
- Scatter plot, for correlation between variables
- Radar chart, for multi dimensional country profiles

All charts are cross filtered, selecting a country or region in one view updates the rest of the dashboard. Color palettes were chosen deliberately rather than by default, and are documented with hex and RGB codes alongside the reasoning behind each choice.

## Tech stack

- Python and pandas for the ETL pipeline
- D3.js for the interactive visualizations
- HTML and CSS for the dashboard shell
- Deployed on Vercel

## Repository structure

```
datos crudos/              raw source datasets
datos transformados/       cleaned, modeled data (star schema)
ETL.ipynb                  data cleaning and transformation pipeline
index.html                 dashboard entry point
Anexos diagramas y modelos.docx   entity relationship diagram and star schema model
Reporte Ejecutivo.docx.pdf        executive summary of findings
Reporte_sanchez_peña.pdf          full academic report
```

## Running locally

Clone the repository and serve the root folder with any static file server, for example

```
npx serve .
```

Then open the served URL in your browser. The ETL notebook can be run independently with Jupyter if you want to regenerate the transformed datasets.

## Reports

Two written deliverables accompany the dashboard, an executive summary aimed at a general audience, and a full academic report detailing the methodology, data sources, and design decisions behind each visualization.

## Notes

This was built as a university course project, so the scope and dataset selection were defined by the course brief. The focus was on applying sound data visualization principles end to end, from raw data to a deployed, interactive product.
