
# SupplyGuard Ultimate Dataset

Synthetic logistics and supply-chain dataset.

## Datasets

customers.csv
shipments.csv
deliveries.csv
drivers.csv
vehicles.csv
warehouses.csv
delivery_labels.csv
exchange_rates.csv
data_dictionary.csv

## Purpose

Designed for a two-week Python/Data Analytics project.

Learners can practise:

- Python
- Pandas
- NumPy
- CSV processing
- Jupyter Notebooks
- Data cleaning
- Data validation
- Data integration
- Exploratory Data Analysis
- Matplotlib
- Business analysis
- Git
- GitHub
- Explainable risk scoring

## Intentionally messy data

The raw data contains:

- Missing values
- Duplicate records
- Inconsistent text
- Mixed date formats
- Numeric values stored as strings
- Outliers

## Business logic

The generator also maintains realistic relationships.

Examples:

1. Shipment customer IDs come from customers.

2. Shipment warehouse IDs come from warehouses.

3. Delivery shipment IDs come from shipments.

4. Delivery driver IDs come from drivers.

5. Delivery vehicle IDs come from vehicles.

6. Shipment weight is checked against vehicle capacity.

7. Delivery dates occur after shipment dates.

8. Actual delivery distance is related to expected distance.

9. Poor vehicle maintenance increases delivery risk.

10. Poor driver performance increases delivery risk.

11. Long-distance deliveries have higher risk.

12. Late deliveries have explainable risk reasons.

13. Late deliveries generally have lower customer ratings.

14. Multiple delivery attempts are more common for late deliveries.

15. Fuel cost is related to delivery distance.

## Important

DO NOT clean the original CSV files.

Create a separate processed/cleaned dataset.

Recommended workflow:

Raw Data
    |
    v
Data Inspection
    |
    v
Data Quality Assessment
    |
    v
Cleaning
    |
    v
Validation
    |
    v
Data Integration
    |
    v
Feature Engineering
    |
    v
Exploratory Analysis
    |
    v
Visualisation
    |
    v
Business Insights
    |
    v
Recommendations

Machine learning is NOT required.

Use explainable, rule-based analytics for delivery risk.
