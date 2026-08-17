# SupplyGuard Logistics Dataset

Large synthetic South African logistics dataset created for
the SupplyGuard two-week Python and Data Analytics sprint.

## Files

- customers.csv
- shipments.csv
- deliveries.csv
- drivers.csv
- vehicles.csv
- warehouses.csv
- delivery_labels.csv
- exchange_rates.csv
- data_dictionary.csv

## Dataset sizes

Approximately:

- 100,000 customers
- 500,000 shipments
- 500,000 deliveries
- 5,000 drivers
- 3,000 vehicles
- 100 warehouses

The data is deliberately large so learners must work with
multiple related CSV files and cannot simply analyse one small
dataset.

## Relationships

customers
    |
    v
shipments
    |
    v
deliveries
    |
    +--> drivers
    |
    +--> vehicles
    |
    +--> delivery_labels

shipments
    |
    +--> warehouses

## Intentional data-quality problems

The raw datasets contain:

- duplicate customers
- duplicate shipments
- duplicate deliveries
- missing values
- inconsistent text
- inconsistent status values
- mixed date formats
- numeric values stored as strings
- extreme distance outliers
- invalid customer IDs
- invalid driver IDs
- invalid vehicle IDs
- invalid warehouse IDs

## Learner requirement

DO NOT overwrite the raw datasets.

Recommended structure:

data/
    raw/
    processed/
    final/

The raw files should remain unchanged.

## Main analytical challenge

Learners should investigate:

1. Customer activity
2. Shipment volume
3. Delivery performance
4. Delayed deliveries
5. Driver performance
6. Vehicle performance
7. Warehouse performance
8. Route and distance patterns
9. Delivery-time patterns
10. Operational risk

## Risk analysis

Machine learning is NOT required.

Learners should create an explainable rule-based risk score.

Example:

Late delivery                 +25
Very long distance            +15
Long delivery duration        +20
Repeated delivery attempts    +15
Low vehicle maintenance       +15
Poor driver rating            +10

Suggested interpretation:

0-30       Low Risk
31-60      Medium Risk
61-100     High Risk

Learners must justify their final scoring system.

## Recommended technologies

Python
NumPy
Pandas
Matplotlib
Jupyter Notebook
SQLite
Requests
Git
GitHub

## SQL requirement

Load selected cleaned datasets into SQLite and demonstrate
queries involving:

- GROUP BY
- JOIN
- WHERE
- ORDER BY
- aggregate functions

## API requirement

Use requests to acquire a small external or simulated JSON
dataset and integrate it into the analysis.

## No Machine Learning

This version intentionally removes the Machine Learning
component from the original brief.

The focus is:

Python
data acquisition
data cleaning
data quality
Pandas
NumPy
SQL
API
feature engineering
grouping
reshaping
visualisation
business intelligence
Git/GitHub
Jupyter