# Cityflow-Bus-Service-Metro-Cities
# CityFlo Metro-City Bus Service — Data Analysis & Business Insights

## 📌 Project Overview

This project analyses a synthetic CityFlo-style metro-city bus service dataset to understand the operational, customer, and financial factors affecting bus service performance.

The analysis focuses on identifying the factors that drive:

* Trip delays
* Trip cancellations and no-shows
* Low customer satisfaction
* Demand variation
* Revenue performance
* Bus occupancy

The analysis compares these factors across **cities, routes, bus types, and time periods**, including **peak vs. non-peak hours, day of week, and month**.

> **Note:** The dataset is synthetically generated for exploratory data analysis (EDA) and workflow practice. It does not represent real CityFlo operational data.

---

## 🎯 Problem Statement

> **What factors drive trip delays, cancellations, and low customer satisfaction in CityFlo's metro-city bus operations, and how do demand, revenue, and occupancy vary across cities, routes, bus types, and time (peak vs. non-peak, day of week, month)?**

This problem statement drives the project scope, including:

* Required columns
* Data-cleaning decisions
* Derived metrics
* Exploratory analysis
* Statistical hypothesis testing
* Dashboard KPIs
* Business recommendations

---

## 📊 Dataset Overview

The dataset contains **3,258 passenger-trip records** across **36 columns**, representing bus trips operated during **2024** across six Indian metro-city markets.

### Cities Covered

* Mumbai
* Pune
* Bangalore
* Hyderabad
* Chennai
* Delhi NCR

### Dataset Characteristics

The raw dataset was intentionally designed to simulate real-world data-quality challenges, including:

* Mixed date formats
* Inconsistent categorical values
* Messy Boolean representations
* Currency symbols and commas in fare values
* Missing values
* Duplicate records
* Negative or invalid ages
* Occupancy values above 100%
* Extreme fare values
* Context-dependent missing ratings

The raw dataset contained **58 intentional exact duplicate rows**.

---

## 🗂️ Project Workflow

The project follows a structured four-phase data analytics workflow.

```text
Raw Dataset
     │
     ▼
Phase 1: Inspect
Steps 1–8
     │
     ├── Dataset shape
     ├── Column understanding
     ├── Whitespace checks
     ├── Duplicate checks
     ├── Memory usage
     ├── Data-type checks
     └── Missing-value checks
     │
     ▼
Phase 2: Clean & Prepare
Steps 9–17
     │
     ├── Column classification
     ├── Data cleaning
     ├── Missing-value treatment
     ├── Outlier handling
     ├── Date/time standardisation
     ├── Boolean standardisation
     ├── Derived metrics
     ├── Logical consistency checks
     └── Clean dataset export
     │
     ▼
Phase 3: Analyse
Steps 18–21
     │
     ├── Univariate analysis
     ├── Bivariate analysis
     ├── Multivariate analysis
     └── Hypothesis testing
     │
     ▼
Phase 4: Report
Steps 22–23
     │
     ├── KPI definition
     ├── Dashboard chart selection
     └── Business insights
```

---

## 🧹 Phase 1 — Data Inspection

The raw dataset was inspected to understand its structure and quality.

The inspection included:

1. Total number of rows
2. Total number of columns
3. Understanding each column
4. Checking and trimming extra spaces
5. Identifying duplicate records
6. Checking memory usage
7. Checking column data types
8. Checking missing values

The inspection identified several columns that required type conversion, including:

* Numeric columns
* Date columns
* Boolean columns

Examples of columns requiring attention:

```text
Numeric:
age
distance_km
fare_inr
discount_inr
rating
occupancy_pct

Datetime:
trip_date

Boolean:
is_peak_hour
gps_enabled
complaint_raised
```

---

## 🧹 Phase 2 — Data Cleaning & Preparation

### Column Classification

The columns were grouped into:

* Numerical columns
* Categorical columns
* Date/time columns
* Identifier columns

This allowed different cleaning strategies to be applied based on each column's intended purpose.

### Columns Removed

The following columns were removed because they were outside the project's analytical scope or did not provide useful aggregate-level insight:

* `booking_id`
* `customer_name`
* `driver_id`
* `driver_name`
* `bus_number`
* `seat_number`
* `device_type`

`customer_id` was retained for potential customer-level grouping, while personally identifiable information such as `customer_name` was removed.

### Data Cleaning Operations

The cleaning process included:

* Standardising categorical labels
* Removing unwanted whitespace
* Converting numeric columns to numeric data types
* Standardising Boolean values
* Parsing dates
* Standardising time fields
* Handling missing values
* Validating IDs
* Handling invalid ages
* Handling occupancy outliers
* Handling extreme fare values
* Removing duplicate trips
* Performing cross-column consistency checks

### Missing Value Treatment

Examples of the treatment strategy included:

* Missing `age` → Median imputation
* Missing `discount_inr` → Filled with `0`
* Missing `rating` → Retained as missing for cancelled/no-show trips because no customer rating would be expected
* Missing `occupancy_pct` → Median imputation by `trip_status`

### Outlier Handling

Outliers were handled using appropriate domain-aware methods rather than blindly removing records.

For example:

* Invalid ages were treated as data-quality issues
* Occupancy values above 100% were identified as errors
* Extreme fare values were handled using clipping/winsorisation

The objective was to preserve useful trip records while reducing the impact of obvious data-entry errors.

---

## 🧮 Derived Metrics

Several new variables were created to support the business questions.

### 1. Trip Year

Extracted from `trip_date`.

### 2. Trip Month

Extracted from `trip_date` to analyse monthly trends.

### 3. Trip Weekday

Extracted from `trip_date` to analyse day-of-week demand.

### 4. Delay Minutes

Calculated as the difference between actual and scheduled departure time.

```text
delay_minutes =
actual_departure - scheduled_departure
```

Overnight time differences were also handled.

### 5. Is Delayed

A trip was classified as delayed when:

```text
delay_minutes > 5
```

### 6. Net Revenue

Calculated as:

```text
net_revenue_inr =
fare_inr - discount_inr
```

Negative values were prevented using a lower bound of zero.

### 7. Age Group

Passengers were grouped into age categories:

* 18–25
* 26–35
* 36–45
* 46–60
* 60+

---

## 📈 Phase 3 — Exploratory Data Analysis

### Univariate Analysis

Numerical variables were analysed using:

* Histograms
* Box plots
* Mean
* Median
* Mode
* Standard deviation
* Skewness
* Kurtosis

Key numerical variables included:

* Age
* Distance
* Fare
* Delay minutes
* Occupancy percentage
* Net revenue

Categorical variables were analysed using:

* Value counts
* Bar charts
* Pie charts

---

### Bivariate Analysis

The project analysed relationships between pairs of variables using:

* Scatter plots
* Correlation coefficients
* Grouped means
* Box plots
* Cross-tabulations
* Stacked bar charts

Examples include:

* Distance vs. Fare
* Average rating by city
* Trip status composition by city

---

### Multivariate Analysis

The project used:

* Pair plots
* Correlation heatmaps
* Grouped box plots
* City-level comparisons
* Faceted delay distributions

One analysis examined how **delay distributions differed across cities**.

---

## 🧪 Hypothesis Testing

Statistical tests were used to move beyond visual patterns and evaluate whether observed relationships were statistically significant.

### 1. Pearson Correlation

**Variables:**

```text
distance_km
fare_inr
```

**H₀:** There is no linear correlation between distance and fare.

**H₁:** There is a linear correlation between distance and fare.

---

### 2. Independent Samples t-test

**Variables:**

```text
delay_minutes
is_peak_hour
```

The test compared average delays between:

* Peak-hour trips
* Non-peak-hour trips

**H₀:** Mean delay is the same for peak and non-peak trips.

**H₁:** Mean delay differs between peak and non-peak trips.

Assumption checks included:

* Shapiro-Wilk test
* Levene's test

---

### 3. One-way ANOVA

**Variables:**

```text
fare_inr
bus_type
```

**H₀:** Mean fare is the same across all bus types.

**H₁:** At least one bus type has a different mean fare.

---

### 4. Chi-square Test of Independence

**Variables:**

```text
city
trip_status
```

The test evaluates whether trip outcomes such as cancellation and no-show behaviour are associated with the city.

**H₀:** City and trip status are independent.

**H₁:** City and trip status are associated.

---

## 📊 Phase 4 — Business KPIs

The following KPIs were identified for the final dashboard.

### Operational KPIs

* Total Trips
* Completed Trips
* Cancellation Rate %
* On-Time Performance %

### Financial KPIs

* Total Revenue
* Average Fare
* Revenue by City

### Customer KPIs

* Average Rating
* Complaint Rate %

### Capacity KPIs

* Average Occupancy %

---

## 📊 Recommended Dashboard Visualisations

The project identified the following charts for a business dashboard:

### KPI Cards

Display:

* Total Revenue
* Total Trips
* Completed Trips
* Cancellation Rate
* On-Time Performance
* Average Fare
* Average Occupancy
* Average Rating
* Complaint Rate

### Trend Analysis

**Monthly Revenue & Trip Volume Trend**

Shows how revenue and trip demand change over time.

### City Performance

**Revenue by City**

Compares total revenue generated across metro markets.

### Trip Outcome

**Trip Status Distribution**

Shows the proportion of:

* Completed trips
* Delayed-completed trips
* Cancelled trips
* No-shows

### Correlation Analysis

**Correlation Heatmap**

Helps identify relationships among numerical variables.

### Booking-to-Completion Funnel

Tracks the journey from:

```text
Booked
   ↓
Not Cancelled / No-show
   ↓
Completed
   ↓
Completed On-Time
```

### Fare vs. Distance

A scatter plot used to examine the relationship between route distance and ticket fare.

> A geographic map was not included because the dataset does not contain latitude/longitude coordinates. City-level charts are used instead.

---

## 🔍 Key Findings

The statistical and exploratory analysis produced the following key findings:

### 1. Distance and Fare

Fare shows a strong positive relationship with distance.

This indicates that longer routes generally have higher ticket fares.

### 2. Bus Type and Fare

Bus type has a statistically significant effect on average fare based on the ANOVA analysis.

This suggests that pricing differs materially across bus categories.

### 3. Peak Hours and Delays

Delay behaviour differs between peak-hour and non-peak-hour trips based on the t-test analysis.

This suggests that commute-time demand and operating conditions may influence service punctuality.

### 4. City and Trip Outcomes

The Chi-square analysis indicates that trip status is associated with city.

This suggests that cancellation and no-show behaviour may vary across metro markets.

---

## 💡 Business Questions Answered

The project is designed to help answer questions such as:

* Which cities experience the highest delay rates?
* Which routes have the highest cancellation rates?
* Does peak-hour demand lead to higher occupancy?
* Are peak-hour trips more likely to be delayed?
* Does weather influence delays and cancellations?
* Which bus types generate the highest revenue?
* Which cities generate the most revenue?
* How does occupancy vary across cities and routes?
* Does higher delay correlate with lower customer ratings?
* Are complaints more common on delayed trips?
* How does demand change by weekday and month?
* Are trip outcomes significantly different across cities?

---

## 🛠️ Technologies Used

* **Python**
* **Pandas** — Data manipulation and analysis
* **NumPy** — Numerical computation
* **Matplotlib** — Data visualisation
* **Seaborn** — Statistical visualisation
* **SciPy** — Statistical hypothesis testing
* **Jupyter Notebook / Google Colab** — Development environment

---

## 📁 Project Files

```text
├── cityflo_bus_service_metro_cities(1).csv
├── cityflo_bus_service_metro_cities_cleaned.csv
│
├── Cityflo_Data_Inspect.ipynb
├── Cityflo_Data_Clean_&_Prepare_.ipynb
├── Cityflo_Data_Analyze.ipynb
└── Cityflo_Data_Report.ipynb
```

### Notebook Description

| File                                           | Purpose                                                          |
| ---------------------------------------------- | ---------------------------------------------------------------- |
| `Cityflo_Data_Inspect.ipynb`                   | Inspects the raw dataset and identifies data-quality issues      |
| `Cityflo_Data_Clean_&_Prepare_.ipynb`          | Cleans, standardises, transforms, and prepares the dataset       |
| `Cityflo_Data_Analyze.ipynb`                   | Performs EDA, multivariate analysis, and hypothesis testing      |
| `Cityflo_Data_Report.ipynb`                    | Defines KPIs, dashboard charts, and summarises business findings |
| `cityflo_bus_service_metro_cities_cleaned.csv` | Final cleaned dataset used for analysis                          |

---

## 🚀 How to Run the Project

### 1. Clone the repository

```bash
git clone <your-repository-url>
cd <your-repository-folder>
```

### 2. Install required libraries

```bash
pip install pandas numpy matplotlib seaborn scipy jupyter
```

### 3. Run the notebooks in order

```text
1. Cityflo_Data_Inspect.ipynb
          ↓
2. Cityflo_Data_Clean_&_Prepare_.ipynb
          ↓
3. Cityflo_Data_Analyze.ipynb
          ↓
4. Cityflo_Data_Report.ipynb
```

The recommended workflow is to first inspect the raw dataset, then generate the cleaned dataset, use the cleaned data for analysis, and finally prepare the KPI and dashboard outputs.

---

## 📌 Conclusion

This project demonstrates an end-to-end data analytics workflow for a metro-city bus service operation.

The project progresses from:

**Raw Data Inspection → Data Cleaning → Feature Engineering → EDA → Statistical Testing → KPI Definition → Business Insights**

The analysis identifies meaningful relationships between operational performance, pricing, demand, and trip outcomes. The results provide a foundation for an operations and business dashboard that can help stakeholders monitor **revenue, demand, occupancy, delays, cancellations, customer satisfaction, and city-level performance**.

The project also demonstrates how statistical analysis can be used alongside visual exploration to validate business hypotheses and support data-driven operational decisions.

---

## 👤 Author

**Anwesa Panja**

Data Analytics | Python | SQL | Power BI | Data Visualisation

---
