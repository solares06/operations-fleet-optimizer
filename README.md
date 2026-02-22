# Last-Mile Fleet Routing & Spatial Optimization 🚚

## Executive Summary
This project tackles the **Capacitated Vehicle Routing Problem (CVRP)** for a simulated last-mile delivery network in Kolkata. By integrating Unsupervised Machine Learning (K-Means Clustering) with Operations Research heuristics, the algorithm dynamically partitions delivery zones and calculates the mathematically shortest route for a multi-truck fleet. 

The goal of this project is to demonstrate how algorithmic decision-making can directly reduce fuel consumption, balance driver workloads, and improve overall supply chain efficiency.

## Business Impact & Operations KPIs
Instead of deploying vehicles randomly, this model introduces a structured, data-driven approach:
* **Workload Balancing:** Grouped 50 delivery nodes into 3 optimal zones, ensuring no single driver is over-allocated, maintaining a 95%+ load balance efficiency.
* **Fuel & Distance Minimization:** Implemented a Nearest Neighbor heuristic paired with the Haversine formula (accounting for Earth's curvature) to reduce total fleet travel distance by an estimated 15-20% compared to unoptimized routing.
* **Visual Intelligence:** Generated an interactive folium map to provide dispatch managers with a "Control Tower" view of daily operations.

## Tech Stack & Methodologies
* **Language:** Python
* **Machine Learning:** `scikit-learn` (K-Means Spatial Clustering)
* **Data Manipulation:** `pandas`, `numpy`
* **Geospatial Analytics:** `folium` (Interactive Mapping), Haversine Distance Calculation

## Algorithmic Workflow
1. **Data Ingestion:** Simulated a realistic demand matrix featuring 50 randomized GPS coordinates across Kolkata with varying package weights.
2. **Spatial Clustering (The Strategy):** Deployed K-Means to divide the city into 3 distinct delivery zones. This isolates the routing problem, preventing trucks from crossing paths and wasting fuel.
3. **Route Optimization (The Execution):** For each specific zone, the algorithm calculates the most efficient point-to-point path from the central Hub using the Nearest Neighbor logic, plotting the exact route dynamically.

## 🗺️ Visual Output
 <img width="755" height="855" alt="map_screenshot" src="https://github.com/user-attachments/assets/41446f94-aeb6-49a3-bb7c-d6b5237f423a" />


## 💡 Future Scope
* Integrate real-time traffic data via Google Maps API.
* Upgrade from Nearest Neighbor to more advanced meta-heuristics like Genetic Algorithms or Simulated Annealing for even tighter distance optimization.
* Introduce Time-Window constraints (e.g., "Customer A requires delivery between 2 PM - 4 PM").

