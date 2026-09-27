# Scottish Health System Model 🏥🏴

An open-source R, Power BI and Tableau project exploring how the **Scottish health system can be represented, analysed and modelled using publicly available data**.

The project brings together data from the **Public Health Scotland (PHS) Scottish Health and Social Care Open Data platform**, statistical modelling, machine learning, forecasting and simulation to investigate patterns, demand, capacity and relationships across different parts of the health system.

---

## 🎯 Project Aim

The aim of this project is to develop a data-driven model of the Scottish health system using publicly available health and population data.

Rather than analysing individual datasets in isolation, the project aims to connect different components of the health system and investigate how changes in one part of the system may relate to outcomes elsewhere.

Potential areas of modelling include:

* 👥 Population and demographic change
* 🏥 Emergency department demand
* ⏳ Waiting times and waiting lists
* 🔬 Diagnostics
* 🎗️ Cancer services
* 💊 Prescribing and medicines
* 🩺 Primary care
* 👨‍⚕️ Workforce and capacity
* 🚑 Patient flows
* 📈 Demand forecasting
* 🔮 Scenario modelling
* 🤖 Machine learning and predictive modelling

---

## 📊 Data

The primary data source is the **Scottish Health and Social Care Open Data platform**, managed by Public Health Scotland.

[PHS Scottish Health and Social Care Open Data](https://www.opendata.nhs.scot/)

The platform provides access to Scottish health and social-care statistics and reference data for reuse. Data is released under the **Open Government Licence**.

Example datasets that may be incorporated into the model include:

* Accident & Emergency
* Cancer incidence and mortality
* Cancer waiting times
* Diagnostics waiting times
* Prescribed and Dispensed
* Population estimates
* General Practice
* Primary care workforce
* Hospital activity
* Waiting times
* Health board-level statistics

The exact datasets used will evolve as the model develops.

---

## 🔌 Data Access

Data can be retrieved programmatically using the [`phsopendata`](https://github.com/Public-Health-Scotland/phsopendata) R package.

`phsopendata` provides functions for discovering datasets and resources and downloading data from the PHS Open Data platform through its CKAN API. It also supports filtering and selecting data before downloading.

### Example

```r
library(phsopendata)

# Find available resources
resources <- list_resources(
  dataset_contains = "emergency department"
)

# Download a resource
data <- get_resource(
  res_id = "RESOURCE_ID"
)
```

The package also provides functionality for retrieving the latest resources and running SQL queries against Open Data resources.

---

## 🧰 Technologies

The project is primarily developed in **R**.

### Core

* R
* RStudio / Posit
* tidyverse
* data.table
* arrow
* phsopendata

### Visualisation

* ggplot2
* plotly
* leaflet

### Statistical Modelling

* Regression models
* Time-series forecasting
* Statistical distributions
* Monte Carlo simulation
* Scenario modelling

### Machine Learning

Potential machine-learning approaches include:

* Random Forest
* XGBoost
* Classification models
* Regression models
* Clustering
* Anomaly detection
* Dimensionality reduction

⭐ Project Vision

Build a reproducible, data-driven representation of the Scottish health system using publicly available data, statistical modelling, simulation and machine learning.

The project will evolve over time as new datasets, modelling approaches and system-level relationships are incorporated.
