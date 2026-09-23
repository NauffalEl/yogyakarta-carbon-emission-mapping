# 🏫 Banyumas School Geospatial & TSP Analysis

A geospatial analysis project for mapping school locations across **Banyumas Regency, Central Java, Indonesia**, combined with **shortest-route analysis using a Brute Force Traveling Salesman Problem (TSP) approach**.

The project visualizes the spatial distribution of schools and explores route optimization between selected educational facilities based on geographic distance.

---

## 📌 Project Overview

The distribution of educational facilities is an important aspect of regional planning and accessibility analysis. This project utilizes geospatial data to map school locations throughout Banyumas Regency.

In addition to visualization, the project applies a **Brute Force approach to the Traveling Salesman Problem (TSP)** to evaluate possible school visitation sequences and identify the shortest route among the selected locations.

The Brute Force method evaluates all possible permutations of school visitation sequences. Although computationally expensive for a large number of locations, this approach provides an exact solution for smaller datasets and serves as a useful baseline for route optimization studies.

---

## 🎯 Objectives

The main objectives of this project are:

* Map school locations across Banyumas Regency.
* Visualize the spatial distribution of educational facilities.
* Calculate distances between selected schools.
* Analyze possible school visitation routes.
* Identify the shortest route using the Brute Force TSP approach.
* Provide an initial insight into educational facility accessibility and route optimization.

---

## 🗺️ Study Area

**Banyumas Regency, Central Java, Indonesia**

The analysis focuses on the geographic distribution of schools within Banyumas Regency.

---

## 🔍 Methodology

The project consists of several main stages:

### 1. Data Collection

School location data is collected in the form of geographic coordinates containing:

* School name
* Latitude
* Longitude
* School location

### 2. Geospatial Mapping

School coordinates are plotted on an interactive map to visualize the distribution of educational facilities throughout Banyumas Regency.

### 3. Distance Calculation

The geographic distance between schools is calculated based on their coordinates.

A distance matrix is generated to represent the distance between every pair of selected schools.

### 4. Brute Force TSP

The Traveling Salesman Problem is formulated as:

> Find the shortest possible route that visits every selected school exactly once and returns to the starting school.

The Brute Force approach generates and evaluates all possible permutations of school visitation sequences.

For `n` locations, the number of possible routes grows approximately as:

```text
(n - 1)!
```

Therefore, the computational complexity becomes very high as the number of locations increases.

### 5. Route Optimization

Each possible route is evaluated based on its total distance.

The route with the minimum total distance is selected as the optimal route for the tested dataset.

---

## 📊 Analysis Workflow

```text
School Location Data
        │
        ▼
Data Cleaning & Preparation
        │
        ▼
Latitude & Longitude
        │
        ▼
Geospatial Visualization
        │
        ▼
Distance Matrix
        │
        ▼
Generate TSP Permutations
        │
        ▼
Calculate Route Distances
        │
        ▼
Find Minimum Distance
        │
        ▼
Optimal School Route
```

---

## 🧠 Algorithm

### Brute Force TSP

The Brute Force algorithm systematically checks every possible route.

Simplified process:

```python
best_route = None
best_distance = float("inf")

for route in all_possible_routes:
    distance = calculate_total_distance(route)

    if distance < best_distance:
        best_distance = distance
        best_route = route
```

This guarantees the shortest route for the tested locations because every possible permutation is evaluated.

However, the factorial growth of possible routes makes the method unsuitable for large-scale TSP problems.

---

## 🛠️ Technologies

Depending on the implementation, this project can utilize:

* **Python**
* **Pandas** — Data processing
* **NumPy** — Numerical computation
* **GeoPandas** — Geospatial data processing
* **Folium** — Interactive map visualization
* **Matplotlib** — Data visualization
* **Scikit-learn** — Supporting analytical tasks

---

## 📁 Project Structure

```text
banyumas-school-geospatial-tsp/
│
├── data/
│   ├── schools.csv
│   └── processed/
│
├── notebooks/
│   └── analysis.ipynb
│
├── src/
│   ├── data_processing.py
│   ├── distance.py
│   ├── tsp_bruteforce.py
│   └── visualization.py
│
├── outputs/
│   ├── school_map.html
│   ├── distance_matrix.csv
│   └── optimal_route.png
│
├── requirements.txt
├── README.md
└── .gitignore
```

---

## 📍 Example Dataset

Example school data:

| School   | Latitude | Longitude |
| -------- | -------: | --------: |
| School A |  -7.4241 |  109.2396 |
| School B |  -7.4258 |  109.2412 |
| School C |  -7.4281 |  109.2358 |
| School D |  -7.4310 |  109.2385 |

*The actual dataset may contain additional schools and attributes.*

---

## 📈 Expected Output

The project produces several outputs:

### School Distribution Map

An interactive map displaying school locations across Banyumas Regency.

### Distance Matrix

A matrix containing the calculated distance between each pair of selected schools.

### Optimal Route

The shortest route obtained after evaluating all possible school visitation sequences.

Example:

```text
Start
  ↓
School A
  ↓
School C
  ↓
School D
  ↓
School B
  ↓
School A
```

The total route distance is calculated based on the selected distance metric.

---

## ⚠️ Limitations

The Brute Force approach has significant computational limitations.

For `n` schools, the number of possible routes increases factorially:

```text
3 schools  → 2!     = 2 routes
5 schools  → 4!     = 24 routes
10 schools → 9!     = 362,880 routes
15 schools → 14!    = 87,178,291,200 routes
```

Therefore, this approach is primarily suitable for:

* Small datasets
* Algorithm demonstrations
* Baseline optimization
* Exact TSP solutions for limited locations

For larger datasets, more scalable approaches such as **Nearest Neighbor, Dynamic Programming, Genetic Algorithms, Simulated Annealing, or other heuristic/metaheuristic methods** can be explored.

---

## 🚀 Future Development

Potential improvements include:

* Integrating OpenStreetMap road networks.
* Using actual road distance instead of straight-line distance.
* Adding school categories and education levels.
* Developing an interactive GIS dashboard.
* Comparing Brute Force with heuristic algorithms.
* Implementing Genetic Algorithm for larger datasets.
* Adding travel time estimation.
* Developing route optimization based on real road networks.
* Expanding the analysis to all educational facilities in Banyumas Regency.

---

## 📚 Research Context

This project demonstrates how **Geographic Information Systems (GIS)** and **combinatorial optimization** can be combined to analyze the spatial distribution and accessibility of educational facilities.

The combination of school mapping and TSP-based route optimization provides a computational baseline for studying potential routes between educational facilities.

---

## 👨‍💻 Author

**Naufal El Kamil**

Data Science & Machine Learning Enthusiast
Indonesia

---

## 📄 License

This project is intended for **educational, research, and portfolio purposes**.
