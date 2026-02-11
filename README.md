# Airline Delays

![](hero.jpg) 

## 1. Introduction
From an industry-wide perspective, delays contribute to congestion at airports, inefficient air traffic management, and increased environmental impact due to excessive fuel burn and carbon emissions. The economic consequences extend beyond airlines to include airports, ground service providers, and businesses dependent on timely air travel, such as logistics and tourism industries.

## 2. Problem Statement
Understanding the key factors contributing to delays - ranging from weather conditions, air traffic congestion, and mechanical issues to staffing shortages, security procedures, and airline scheduling inefficiencies - is crucial for developing strategies to mitigate their occurrence. By leveraging data analytics, predictive modeling, and real-time monitoring, stakeholders can identify patterns, anticipate potential disruptions, and implement proactive solutions.
This analysis focuses on:
- Identifying the busiest months and airports for flights.
- Determining months with the highest delay rates.
- Analyzing delay patterns across different airlines.
- Examining primary causes of delays.
- Evaluating geographical patterns in delay occurrences.

## 3. Skills Demonstrated
- **Data Cleaning & Transformation** using Power Query
- **DAX Measures** for advanced calculations
- **Data Modeling** with relationships between fact and dimension tables
- **Interactive Dashboards** using Power BI visualizations
- **Power Query**: Using Power Query to clean, transform, and shape raw data into an analysis-ready format, ensuring accuracy and consistency.
- **Power BI Parameters**: Implemented a dynamic parameter allowing users to select different delay and flight categories . This enhances interactivity and enables focused analysis based on user selection. 

## 4. Data Sourcing
The dataset used in this project consists of airline delay data, including:
- Flight details (Year, Month, Airline, Airport Code, Total Flights, Delays)
- Delay breakdown (Carrier, Weather, Late Aircraft, etc.)
- Additional airport and carrier information

The Dataset Provide by **FP20 Analytics** 

More Information About This Challenge: [FP20 Analytics challenge 23](https://zoomcharts.com/en/microsoft-power-bi-custom-visuals/challenges/fp20-analytics-january-2025)


## 5. Data Transformation
Data preprocessing was performed using Power Query, including:
- Cleaning and structuring data
- Creating a Calendar table for time-based analysis
- Adding an Airport table with `Airport Code`, `Airport Name`, and `Airport Location`
- Adding a Carrier table with `Carrier Name` and `Carrier SVG Image`

## 6. Modeling
A `Star Schema` relational data model was designed in Power BI with the following structure:
- **Fact Table:** `Airline Delays`
- **Dimension Tables:** `Calendar`, `Airport`, `Carrier`
- Relationships established between the fact and dimension tables

**Data Model Screenshot:**
![Data Model](data_modeling.png)

### Create Parameters

#### Flight

| Parameter | Result |
|----------|----------|
| ![](parameter/parameter_flight.png) | ![](parameter/result_parameter_flight.png) |

#### Delays

| Parameter | Result |
|----------|----------|
| ![](parameter/parameter_delay.png) | ![](parameter/result_parameter_delay.png) |

### DAX Measures  
Here are some DAXs used for flight delay analysis:

#### Calculate Total and Average

![Data Model](dax_measure/total_average_dax.png)

#### Calculate Rate %

![Data Model](dax_measure/rate_dax.svg)

#### MoM Flight Arrival, Cenceled Flight, and Diverted FLight (The dax in the example is Flight Arrival) & Conditional Formating color to Clarify the Metric

![Data Model](dax_measure/mom_dax.svg)

#### Dynamic Slicer

![Data Model](dax_measure/slicer_dax.png)

##### Application Example

| Default | Filtered |
|----------|----------|
| ![](metric_and_slicer/slicer_default.png) | ![](metric_and_slicer/slicer_default_off.png) |

#### Selected Metric for better user understanding between `Delays` & `Flight`

![Data Model](dax_measure/selected_metric_dax.svg)

##### Application Example

| Delays | Flight |
|----------|----------|
| ![](metric_and_slicer/flight_matrix_value.png) | ![](metric_and_slicer/delay_matrix_value.png) |

## 7. Analysis & Visualization
Key insights were extracted using Power BI visualizations and DAX measures, including:
- **KPIs:** Delay Rate, Average Delay Per Flight, On-Time Performance, and Flight Category
- **Bar Charts & Line Charts** for trend analysis
- **Geographical Analysis** using airport locations

In this Dashboard there are 3 pages :

- Overview
- Flight
- Delay 

You can interact with report here [FP 20 Analytics Challenge](https://zoomcharts.com/en/microsoft-power-bi-custom-visuals/challenges/submission/a28f2a02988cf596c653c97057fe1162?challenge=fp20-analytics-january-2025)

![](dashboard2.png) 

### Insights

- **Flight Volume Trends:**
  - **2023 had higher flight volumes**, averaging **40K-60K flights per month**, with a peak in **January 2023 (68K+ flights)**.
  - **2024 showed a decline in flight volume (20K-40K flights/month)**, with a slight increase in December.

- **Busiest Months & Airports:**
  - Peak months: **January, April, May, October, November, and December**.
  - Busiest airports: **ATL (Hartsfield-Jackson), DFW (Dallas/Fort Worth), and ORD (Chicago O'Hare)**.

- **Months with the Highest Delay Rates:**
  - **May and July had the highest delay rates (21.5%)** especially in 2023.

- **Primary Causes of Delays:**
  - **Late aircraft (57.39K affected flights)**.
  - **Carrier-related delays (53.71K flights)**.
  - **Weather-related delays (4.82K flights)**.

- **Weather Impact & Geographic Disparities:**
  - **DFW (Dallas/Fort Worth), ORD (Chicago O'Hare), and MSP (Marcos Paz Airfield) airports experience the most weather-related delays**, adding **10-12 minutes per flight**.
  - **Coastal airports face significantly more delays (90%) compared to inland airports (10%)**.
  - **North America is the most affected region, with 4.1K flights delayed due to weather**.

- **Delay Patterns vs. Flight Volume:**
  - **Lower flight volumes in 2024 correlated with improved delay rates (stabilizing at 10-11%)**.

---

### Conclusion

Flight delays remain a **major operational challenge**, influenced by **seasonal traffic, airline efficiency, and external factors like weather**. Key takeaways:

- **Peak travel months lead to higher congestion and increased delays**.
- **Carrier-related and late aircraft delays are the most significant contributors** to flight disruptions.
- **Weather-related delays predominantly impact major hubs, particularly coastal airports**.
- **When flight volume decreases, on-time performance improves**, highlighting the importance of optimized scheduling.

Reducing delays requires **better scheduling, predictive analytics, and operational efficiency improvements**.

---

### Recommendations

- **📅 Peak Season Operations:**
  - Increase workforce, improve ground handling, and optimize aircraft turnaround times.
  - Use **slot management systems** to prevent excessive congestion.

- **⏳ Reducing Delay Rates in May & July:**
  - Implement **predictive analytics** for proactive scheduling.
  - Introduce **buffer time in flight schedules** to minimize cascading delays.

- **⚠ Minimizing Carrier & Late Aircraft Delays:**
  - Improve **fleet utilization and maintenance scheduling**.
  - Use **real-time tracking and AI-driven operational decision-making**.

- **🌦 Mitigating Weather-Related Delays:**
  - Invest in **advanced weather forecasting technology**.
  - Establish **backup aircraft and alternative routing strategies**.

- **🌍 Addressing Geographic Delay Disparities:**
  - Expand infrastructure and enhance **air traffic control systems** at coastal airports.
  - Adjust schedules to avoid peak congestion times.

- **✈ Learning from Airlines with Better On-Time Performance:**
  - Adopt best practices like **efficient fleet rotation, strategic scheduling, and improved passenger communication**.

By implementing these strategies, airlines and airports can **reduce delays, enhance passenger experience, and improve operational efficiency**. 🚀

---
### Repository Contents  
- **Power BI Dashboard File**: The main [PBIX File](https://zoomcharts.com/en/microsoft-power-bi-custom-visuals/challenges/submission/a28f2a02988cf596c653c97057fe1162?challenge=fp20-analytics-january-2025) containing the analysis and visualizations. 
- **Data Sources**: [Raw Dataset](Airline_Delays_English_C23.xlsx) used in the project.  
- **Screenshots/Reports**: Exported visualizations for sharing insights.  
- **README.md**: Project documentation (this file).
