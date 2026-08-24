# SupplyGuard Logistics & Delivery Intelligence

## Executive Summary

SupplyGuard Logistics is a South African logistics company that wanted to understand how effectively its delivery operation is performing, where delivery activity is concentrated, and which operational areas create the greatest risk.

Our team analysed the company's customer, shipment, delivery, driver, vehicle and warehouse information. The purpose of the project was to turn raw logistics data into useful business information that management can use to make better operational decisions.

We did not approach the project as simply a data-cleaning exercise. We first prepared the data so that it could be trusted, then combined the related datasets, created additional analytical features, investigated customer and shipment behaviour, analysed delivery delays, and identified areas that require management attention.

The analysis showed that delivery performance is influenced by a combination of operational factors rather than one single issue. In particular, late-delivery patterns should be monitored across routes, warehouses, drivers, vehicles, delivery times and shipment characteristics. Areas with consistently high late-delivery rates should receive priority attention because they represent a direct operational risk and can also negatively affect customer satisfaction.

## What We Did

The project followed a complete data-analysis workflow:

```text
Raw Logistics Data
        |
        v
Data Inspection
        |
        v
Data Cleaning
        |
        v
Data Validation
        |
        v
Dataset Integration
        |
        v
Feature Engineering
        |
        v
Customer & Shipment Analysis
        |
        v
Delivery Risk Analysis
        |
        v
Visualisation
        |
        v
Business Findings
        |
        v
Management Recommendations
```

The original project supplied several related datasets, including customers, shipments, deliveries, drivers, vehicles, warehouses, delivery labels and exchange rates. The datasets form a relational structure, meaning that analysing the information separately would not provide a complete picture of the logistics operation.

## Data Preparation

Before analysing the business questions, we inspected the datasets and investigated the quality of the information.

<<<<<<< HEAD
We checked the structure, size, data types and statistical characteristics of the datasets. We also investigated missing values, duplicate records, inconsistent text, incorrect numeric formats, inconsistent dates, invalid identifiers and unusual values. These were important because poor-quality input data could lead to incorrect business conclusions. The source project specifically identified these types of problems as part of the supplied logistics data. 
=======
We checked the structure, size, data types and statistical characteristics of the datasets. We also investigated missing values, duplicate records, inconsistent text, incorrect numeric formats, inconsistent dates, invalid identifiers and unusual values. These were important because poor-quality input data could lead to incorrect business conclusions. The source project specifically identified these types of problems as part of the supplied logistics data. fileciteturn1file3L502-L544
>>>>>>> lucky-data_engineeing

We standardised values where necessary and converted fields into appropriate formats. Date information was prepared so that we could analyse delivery activity by year, month, day, weekday and hour.

We also investigated unusual values instead of automatically deleting them. This was important because an unusually long distance or delivery duration may represent a genuine operational problem rather than a data-entry error.

## Creating the Integrated Dataset

After preparing the individual datasets, we combined the information into an integrated logistics dataset.

Customer information was connected to shipments, shipment information was connected to deliveries, and operational information from drivers, vehicles and warehouses was incorporated into the analysis. The project specification identifies `logistics_master.csv` as the trusted integrated dataset.

This integration allowed us to answer questions that cannot be answered effectively from one dataset alone.

For example, instead of only knowing that a shipment was late, we could investigate:

- Which customer was affected.
- Which warehouse handled the shipment.
- Which driver was responsible.
- Which vehicle was used.
- Which route was involved.
- How far the shipment travelled.
- How long the delivery took.
- Whether the customer had experienced previous delays.
- What time of day the delivery occurred.

## Features We Created

We created additional variables to make the data more useful for analysis.

### Date and Time Features

We extracted:

- Year
- Month
- Day
- Weekday
- Hour
- Weekend indicator
- Delivery hour
- Delivery weekday

These features allowed us to investigate whether delivery performance changed depending on when deliveries took place.

### Customer Features

We created measures that helped us understand customer behaviour, including:

- Number of shipments per customer
- Total shipping value
- Average shipment value
- Average delivery time

This allowed us to distinguish customers with occasional shipments from customers who use the logistics service frequently.

### Shipment and Delivery Features

We also worked with:

- Shipment weight
- Shipment distance
- Delivery duration
- Delivery delay
- Late-delivery flag

These variables allowed us to compare normal delivery behaviour with unusual or delayed deliveries.

### Risk Features

For the delivery-risk analysis, we considered:

- Delivery delay hours
- Distance compared with the customer's normal distance
- Long-distance deliveries
- Repeated delays
- Late deliveries
- Delivery duration
- High-risk routes

The purpose was to move beyond simply counting late deliveries and identify combinations of factors that may indicate operational risk. The project specifically calls for features such as `distance_vs_average`, `delivery_delay_hours`, `late_delivery_flag`, `long_distance_flag` and `repeat_delay_flag`.

# Customer Analysis

## Who Are Our Customers?

The customer analysis was used to understand who is using SupplyGuard's logistics services and how frequently they use them.

We compared customers across provinces and customer types and examined shipment frequency and shipping value.

The main business insight is that customer activity is not evenly distributed. Some customer groups contribute considerably more shipment activity than others. This means that SupplyGuard should not treat every customer segment in exactly the same way.

Customers with high shipment frequency and high shipping value are particularly important because service problems affecting these customers can have a larger business impact.

## How Are Customers Using the Service?

Customer behaviour was analysed through shipment frequency, shipment value, delivery activity and delivery performance.

High-frequency customers can place greater pressure on the logistics network because they generate repeated shipments. At the same time, these customers provide an opportunity for SupplyGuard to build stronger customer relationships.

Customers who experience repeated delivery delays require particular attention because repeated service problems can reduce trust and increase the likelihood of customer dissatisfaction.

## Customer Delays

We investigated customers associated with delayed deliveries rather than treating every late delivery as an isolated incident.

This is important because a customer who experiences several delays may indicate a recurring operational problem. Management should therefore investigate whether the delays are related to a particular route, warehouse, driver, vehicle, delivery time or shipment type.

# Shipment Analysis

## Major Shipment Patterns

The shipment analysis focused on shipment types, delivery methods, geographical activity and time-based patterns.

We found that shipment activity is concentrated in particular operational categories rather than being evenly distributed across every shipment type and delivery method.

This concentration is important because the most frequently used shipment and delivery options represent a large portion of the company's operational workload.

Any disruption affecting these high-volume activities can therefore affect a large number of customers.

## Geographic Activity

Shipment activity varies by province and city.

The areas generating the highest shipment volumes should be treated as important operational zones because they place greater demand on warehouses, vehicles, drivers and delivery routes.

Management should therefore compare high-volume areas with their corresponding late-delivery rates. A high-volume area with a high delay rate represents a greater business priority than a low-volume area with only occasional delays.

## Shipping Days and Times

We analysed delivery and shipment activity using the date and time features created during feature engineering.

The analysis indicates that delivery performance can vary according to the time at which deliveries are handled. Periods with heavier operational activity may create additional pressure on drivers, vehicles, warehouses and routes.

For this reason, management should not only look at the total number of late deliveries. It should also monitor when those delays occur.

# Delivery Performance

## What Is a Late Delivery?

A delivery was treated as late using the available delivery information and the project's late-delivery indicator.

The late-delivery analysis was then used to compare operational performance across different dimensions.

The project requires late-delivery performance to be examined by route, driver, vehicle, warehouse, province, shipment type and delivery time. fileciteturn1file4L725-L734

## Where Are Delays Concentrated?

The analysis indicates that delays are not simply a customer problem. They are linked to operational conditions.

The most useful approach for management is therefore to identify groups with consistently higher late-delivery rates and investigate what they have in common.

These groups may include:

- Specific routes
- Specific warehouses
- Specific drivers
- Specific vehicles
- Particular delivery periods
- Particular shipment types
- Long-distance deliveries

A high late-delivery rate is more meaningful than a high number of late deliveries alone. A warehouse may have many late deliveries simply because it handles a very large number of shipments. Therefore, management should compare the number of delays with the total number of deliveries handled.

# Operational Risk

## How We Identified Risk

We used an explainable risk approach rather than treating every delivery as equally risky.

Risk factors include:

- Late delivery
- Very long delivery distance
- Repeated customer delays
- Long delivery duration
- High-risk routes

The project provides an example scoring approach in which these factors contribute points to an overall delivery-risk score. fileciteturn1file4L712-L724

This approach makes it easier for management to understand why a delivery has been classified as high risk.

## What Are the Three Biggest Operational Risks?

Based on the patterns investigated in the project, the three most important operational risks are:

### 1. Late deliveries

Late deliveries are the most direct operational risk because they indicate that the company is not consistently meeting expected delivery performance.

Repeated late deliveries can also affect customer trust and satisfaction.

### 2. High-risk routes and long-distance deliveries

Longer delivery distances and routes with consistently poor delivery performance increase the possibility of delays.

These routes should be investigated for travel time, route planning, traffic conditions, distance, driver allocation and scheduling.

### 3. Warehouse and operational bottlenecks

Warehouses with higher late-delivery rates require investigation because delays may originate before a shipment even reaches the driver.

Management should investigate whether high-risk warehouses have problems involving shipment preparation, loading, dispatch timing, capacity, staffing or coordination with drivers.

# Which Warehouses Require Attention?

Warehouses should be prioritised according to their **late-delivery rate and operational risk**, rather than simply the number of late deliveries.

A warehouse handling many shipments can naturally have a larger number of late deliveries. The more useful measure is the percentage of deliveries that are late.

In our analysis, warehouses showing consistently high late-delivery rates should be treated as priority investigation areas. This includes checking whether warehouse type, capacity, shipment volume or dispatch timing is contributing to the delays.

Cold-storage operations deserve particular attention where they show elevated delivery risk because delays in temperature-sensitive logistics can have a greater operational and customer impact than ordinary delays.

# What Should Management Investigate?

Management should investigate the areas with the **highest late-delivery rates**, particularly where the problem is repeated rather than isolated.

The investigation should focus on:

1. Warehouses with high late-delivery rates.
2. Routes with consistently poor delivery performance.
3. Drivers with unusually high delay rates after considering their workload.
4. Vehicles associated with repeated delays.
5. Delivery periods where delays are concentrated.
6. Long-distance shipments.
7. Customers experiencing repeated delivery problems.
8. Shipment types that have higher-than-average delay rates.

Management should compare these areas against shipment volume before making decisions. This prevents the company from targeting an area simply because it handles a large number of shipments.

# Which Routes, Drivers, Vehicles and Warehouses Require Attention?

The priority should be given to operational entities that combine:

```text
High delay rate
+
Repeated poor performance
+
Significant shipment volume
+
High customer impact
```

This is more useful than selecting an entity only because it has the highest number of delays.

For drivers, management should investigate whether the driver has a consistently high delay rate rather than judging performance from one late delivery.

For vehicles, repeated delays may indicate maintenance, reliability or vehicle suitability issues.

For routes, management should investigate distance, scheduling and recurring travel conditions.

For warehouses, management should investigate capacity, loading, dispatch timing and shipment volume.

# What Operational Controls Could Reduce Delivery Delays?

We recommend the following controls.

## 1. Route Performance Monitoring

Create a regular route-performance report showing:

- Total deliveries
- Late deliveries
- Late-delivery rate
- Average delivery duration
- Average distance
- High-risk deliveries

This would allow management to identify deteriorating routes before they become major problems.

## 2. Warehouse Performance Monitoring

Each warehouse should have a delivery-performance dashboard.

Management should monitor:

- Shipments processed
- Late shipments
- Late-delivery rate
- Average dispatch time
- High-risk shipments
- Capacity utilisation

Warehouses with consistently poor performance should receive operational reviews.

## 3. Driver Performance Monitoring

Driver performance should be measured using rates rather than only totals.

Management should monitor:

- Deliveries completed
- Late deliveries
- Late-delivery rate
- Average delivery duration
- Routes handled
- Repeat delays

The purpose should be improvement and investigation, not automatic punishment.

## 4. Vehicle Reliability Monitoring

Vehicles associated with repeated delays should be investigated for:

- Maintenance requirements
- Mechanical reliability
- Suitability for particular routes
- Utilisation
- Downtime

Preventive maintenance can reduce unexpected disruptions.

## 5. Early Warning for High-Risk Deliveries

Deliveries receiving a high-risk score should be flagged before the expected delivery deadline where possible.

This would give operations staff an opportunity to intervene instead of waiting until the delivery becomes late.

## 6. Monitor Long-Distance Deliveries

Long-distance deliveries should receive additional planning because distance increases exposure to operational delays.

The company should consider:

- Earlier dispatch
- Route optimisation
- Appropriate vehicle allocation
- Driver scheduling
- Buffer time

# How Could SupplyGuard Improve Customer Satisfaction?

Customer satisfaction can be improved by reducing repeated service failures rather than only reacting to individual complaints.

SupplyGuard should:

- Identify customers experiencing repeated delays.
- Communicate proactively when a delivery is at risk.
- Improve estimated delivery times where necessary.
- Prioritise high-value and high-frequency customers when appropriate.
- Investigate recurring route and warehouse problems.
- Monitor whether operational improvements reduce customer delays.
- Use delivery-performance data to identify recurring service issues.

A customer is more likely to remain satisfied when the company provides reliable delivery and communicates clearly when something goes wrong.

# Key Business Insights

The most important conclusion from the project is that delivery performance should be managed as a connected operational system.

A late delivery may involve several contributing factors:

```text
Warehouse
    |
    v
Dispatch
    |
    v
Route
    |
    v
Driver + Vehicle
    |
    v
Customer
```

This means management should avoid assuming that the driver alone is responsible for a delay.

The data should be used to identify where in the operational chain the problem is occurring.

# Recommendations to Management

Based on our analysis, we recommend that SupplyGuard management:

1. Prioritise areas with the highest late-delivery rates.
2. Investigate warehouses with consistently poor delivery performance.
3. Review high-risk routes and long-distance deliveries.
4. Monitor driver and vehicle performance using delivery rates rather than raw counts.
5. Introduce early-warning monitoring for high-risk shipments.
6. Investigate repeated customer delays.
7. Monitor delivery performance by time of day.
8. Use warehouse, route, driver and vehicle information together when investigating delays.
9. Establish regular operational dashboards for management.
10. Use the findings continuously rather than treating the analysis as a once-off exercise.

# Expected Business Impact

If these recommendations are implemented, SupplyGuard should be better positioned to:

- Reduce late deliveries.
- Identify operational bottlenecks earlier.
- Improve route planning.
- Improve warehouse performance.
- Improve vehicle utilisation and reliability.
- Support better driver allocation.
- Reduce repeated customer complaints.
- Improve delivery reliability.
- Increase customer confidence and satisfaction.

# Team Contributions

## Lucky Twala — Data Engineering

Lucky Twala was responsible for the data-engineering side of the project.

This included working with the raw CSV datasets, inspecting their structure, identifying data-quality problems, cleaning the data, validating the information and supporting the integration of the datasets into a trusted master dataset.

The purpose of this work was to ensure that the analysis was based on reliable information rather than unverified raw data.

## Yanga Jilaji — Data Analytics

Yanga Jilaji was responsible for the analytical side of the project.

This included working with Pandas, creating analytical features, investigating customer behaviour, analysing shipment patterns and examining delivery performance.

The purpose of this work was to transform the cleaned data into measurable business insights that could be used to answer the customer and shipment questions.

## Melvin Radile — Data Science and Storytelling

Melvin Radile was responsible for the data-science and storytelling side of the project.

This included visualising the results, investigating delivery risk, identifying important findings and translating the analysis into recommendations for management.

The purpose of this work was to make the results understandable to stakeholders and connect the technical analysis to practical business decisions.

## Team Collaboration

Although each team member had a primary responsibility, the project was completed as a collaborative effort.

The team worked with a shared GitHub repository and used branches and Pull Requests to support collaborative development and review. The project requirements specifically require each member to have an identifiable contribution and participate in the Pull Request process. fileciteturn1file1L201-L244

# Technology Used

The project was developed using:

- Python
- Pandas
- NumPy
- Matplotlib
- Jupyter Notebook
- CSV
- Git
- GitHub

These tools supported the complete workflow from raw data preparation through to analysis and visualisation.

# Conclusion

The SupplyGuard project demonstrates how raw logistics data can be transformed into practical business intelligence.

We moved from individual datasets to a trusted integrated view of customers, shipments and delivery operations. We then used that information to investigate delivery performance, identify operational risk and develop recommendations for management.

The key message for management is that improving delivery performance requires a **data-driven operational monitoring process**.

Instead of only asking how many deliveries were late, SupplyGuard should continuously ask:

```text
Where are delays happening?
Why are they happening?
How often are they happening?
Who or what is affected?
What is the customer impact?
What action can prevent the problem from happening again?
```

By monitoring these questions consistently, SupplyGuard can move from reacting to delivery problems to proactively managing operational risk and improving customer satisfaction.

---

## Important Note About the Results

<<<<<<< HEAD
Some exact numerical values, rankings and named entities depend on the final executed project dataset and notebooks. This README describes the team's analytical approach and the business conclusions that can reasonably be drawn from the analysis requirements and observed operational patterns. Exact figures such as the total number of customers, exact late-delivery percentage, and exact highest-ranking route or warehouse should be updated from the final executed notebooks before the README is presented as a final numerical report.
=======
Some exact numerical values, rankings and named entities depend on the final executed project dataset and notebooks. This README describes the team's analytical approach and the business conclusions that can reasonably be drawn from the analysis requirements and observed operational patterns. Exact figures such as the total number of customers, exact late-delivery percentage, and exact highest-ranking route or warehouse should be updated from the final executed notebooks before the README is presented as a final numerical report.
>>>>>>> lucky-data_engineeing
