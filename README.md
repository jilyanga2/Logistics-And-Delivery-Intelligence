# Logistics-And-Delivery-Intelligence

# Data Preparation and Final Merge

The datasets were merged to create a final master dataset containing the relevant customer, shipment, delivery and operational required for the operational risk analysis.

The merge dataset, "master", serves as a foundation for developing the risk operational risk score. 

The operational risk score is based on five key risk factors. 

1. "Late Delivery"  - identifies deliveries with unusally long delivery durations. 
2. "Very Long Delivery Durations" - identifies deliveries with unsually long delivery durations. 
3. "Repeated Customer Delays" - identifies customers experiecing long delivery durations. 
4. "Long Delivery Durations" - identifies deliveries with exceptionally long delivery durations. 
5. "High Risk Route" - identifies routes with relatively high historical lae delivery rates.

# 6.3 Operational Risk Scoring 
The objective of this analysis is to create a simple and explainable operational risk score for each delivery. Five operational risk facts are evualated and assigned weighted points, resulting in a score between 0 and 100. Deliveries are then classified as Low, Medium or High Risk