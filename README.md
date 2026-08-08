# 🚌 CityFlo Bus Service – Metro Cities Data Analysis

![CityFlo](https://img.shields.io/badge/Project-CityFlo%20Bus%20Service-003B5C)
![Python](https://img.shields.io/badge/Python-3.x-blue)
![Pandas](https://img.shields.io/badge/Pandas-Data%20Analysis-150458)
![Power BI](https://img.shields.io/badge/Power%20BI-Dashboard-F2C811)
![Status](https://img.shields.io/badge/Status-Completed-success)

---

## 📌 Project Overview

**CityFlo Bus Service – Metro Cities Data Analysis** is an end-to-end **Data Analytics and Business Intelligence project** focused on analyzing bus service operations, customer behavior, revenue performance, trip performance, delays, occupancy, subscriptions, payment methods, and booking channels across major Indian metro cities.

The project transforms raw trip-level data into meaningful business insights using **Python, Pandas, NumPy, Matplotlib, Seaborn, SciPy, and Power BI**.

The main objective of this project is to understand:

- Bus service performance
- Revenue generation
- Customer behavior
- Trip status
- Delay patterns
- Occupancy levels
- Route performance
- Customer satisfaction
- Subscription behavior
- Payment preferences
- Booking channels
- Weather impact on operations

---

# 🎯 Business Objectives

The project is designed to answer important business questions such as:

- Which cities generate the highest revenue?
- Which cities have the highest number of trips?
- Which cities experience the highest average delays?
- What percentage of trips are completed, delayed, cancelled, or no-show?
- Does weather affect bus delays?
- Which bus types have the highest occupancy?
- How does route distance affect revenue?
- How does customer rating vary over time?
- Which customer age groups are the most active?
- Which subscription types are most popular?
- Which payment modes are most frequently used?
- How many trips have complaints?
- Which booking channels generate the most revenue?
- Which routes have higher occupancy?
- How does revenue change month by month?

---

# 🛠️ Technology Stack

| Technology / Tool | Purpose |
|---|---|
| Python | Data analysis and preprocessing |
| Pandas | Data manipulation and cleaning |
| NumPy | Numerical computation |
| Matplotlib | Data visualization |
| Seaborn | Statistical visualization |
| SciPy | Statistical analysis and hypothesis testing |
| Jupyter Notebook | Data analysis environment |
| Kaggle | Notebook and analysis |
| Power BI | Interactive dashboard development |
| GitHub | Version control and project documentation |

---

# 🔄 Project Workflow

**Raw Dataset**

↓

**Data Inspection**

↓

**Data Cleaning & Preparation**

↓

**Feature Engineering**

↓

**Exploratory Data Analysis**

↓

**Statistical Analysis**

↓

**Business Analysis**

↓

**Power BI Dashboard**

↓

**Business Insights & Recommendations**

---

# 📂 Dataset

The dataset contains trip-level information related to CityFlo bus services.

### Important Columns

- Trip ID
- Customer ID
- Route ID
- Trip Date
- City
- Age
- Gender
- Bus Type
- Payment Mode
- Booking Mode
- Subscription Type
- Weather
- Trip Status
- Delay Minutes
- Occupancy Percentage
- Distance
- Fare
- Discount
- Net Revenue
- Customer Rating
- Complaint Status

The dataset is used to analyze operational performance, customer behavior, and financial performance.

> **Note:** The dataset is intended for data-analysis and dashboarding practice and should not be considered actual confidential CityFlo operational data.

---

# 🧹 Data Cleaning & Preparation

Before performing analysis, the dataset was inspected and cleaned to improve data quality and consistency.

### Data Cleaning Activities

- Checked the structure of the dataset
- Identified duplicate records
- Handled missing values
- Checked invalid values
- Standardized categorical values
- Removed unwanted spaces
- Converted columns into appropriate data types
- Formatted date and time columns
- Validated numerical columns
- Checked inconsistent values
- Identified and handled outliers
- Prepared the cleaned dataset for analysis

### Missing Value Handling

Different approaches were used depending on the column and business meaning.

Examples include:

- Missing `age` values were handled using appropriate statistical imputation.
- Missing `discount_inr` values were treated as `0` where applicable.
- Missing ratings were retained where the rating was not applicable, such as cancelled or no-show trips.
- Missing occupancy values were handled using suitable imputation techniques.

---

# 🧮 Feature Engineering

Several new features were created to support deeper analysis.

## Net Revenue

The net revenue was calculated as:

`Net Revenue = Fare - Discount`

This represents the revenue generated after applying discounts.

---

## Delay Minutes

Delay was calculated using the difference between actual and scheduled departure time:

`Delay Minutes = Actual Departure Time - Scheduled Departure Time`

This metric is used to measure operational delays.

---

## Is Delayed

Trips with delays greater than the defined threshold were classified as delayed.

---

## Trip Month

The month was extracted from the trip date to analyze monthly revenue and trip trends.

---

## Trip Weekday

The weekday was extracted from the trip date to understand day-wise travel patterns.

---

## Age Group

Customers were categorized into different age groups:

- 18–25
- 26–35
- 36–45
- 46–60
- 60+

---

# 📊 Power BI Dashboard

The project contains **four major Power BI dashboards**, each focusing on a different aspect of CityFlo's business performance.

---

# 1️⃣ Dashboard 1 – CityFlo Executive Overview

## 🎯 Purpose

The **CityFlo Executive Overview Dashboard** provides a high-level summary of overall trip, customer, route, and revenue performance.

It is designed for management and business stakeholders who need a quick overview of the company's performance.

---

## 📌 KPI Cards

The dashboard contains the following KPI cards:

- **Trip ID** – Total number of trips
- **Customer ID** – Total customer count
- **Age** – Age-related customer metric
- **Route ID** – Number of routes
- **Trip Date** – Trip-date metric
- **Total Net Revenue** – Total revenue after discounts

---

## 📊 Dashboard Visualizations

### 🏙️ Trips by City

A column chart showing the number of trips across different cities:

- Mumbai
- Pune
- Delhi NCR
- Bangalore
- Chennai
- Hyderabad

### Business Purpose

This visualization helps identify cities with higher trip demand and compare operational activity across different markets.

---

### 💰 Revenue by City

A ranked table showing the net revenue generated by each city.

The dashboard displays:

1. Mumbai
2. Pune
3. Bangalore
4. Chennai
5. Hyderabad
6. Delhi NCR

### Business Insight

Mumbai is the highest revenue-generating city in the displayed dashboard.

This analysis can help management identify strong-performing markets and prioritize business investment.

---

### 🥧 Trip Status Distribution

A pie chart showing the distribution of different trip statuses:

- Completed
- Delayed-Completed
- Cancelled
- No-show

### Business Insight

Completed trips form the largest portion of total trips.

Cancelled and no-show trips represent potential opportunities for improving operational efficiency and reducing revenue loss.

---

### 📈 Monthly Revenue Trend

A line chart showing how net revenue changes throughout the year.

### Business Purpose

This visualization helps identify:

- High-revenue months
- Low-revenue months
- Revenue fluctuations
- Seasonal patterns

This information can support revenue forecasting and business planning.

---

### 👥 Customer Gender Distribution

A donut chart showing customer distribution by:

- Female
- Male
- Other

### Business Purpose

This visualization provides an overview of customer gender composition and can support customer segmentation and targeted marketing.

---

## 🎛️ Interactive Filters

The dashboard provides filters for:

- Gender
- Bus Type
- Payment Mode
- Days
- City
- Weather
- Age Group
- Booking Mode

These filters allow users to analyze specific customer and operational segments.

---

# 2️⃣ Dashboard 2 – Operations & Delay Analysis

## 🎯 Purpose

The **Operations & Delay Analysis Dashboard** focuses on operational performance, delays, weather conditions, peak-hour activity, customer age distribution, and bus occupancy.

It helps identify factors that may influence service reliability.

---

## 📌 KPI Cards

The dashboard contains:

- **Delay Mins**
- **Occupancy Rate**
- **City**
- **Age Group**
- **Weather**
- **Bus Type**

---

## 📊 Dashboard Visualizations

### 👤 Customer Age Distribution

A treemap showing customers distributed across different ages.

### Business Purpose

This visualization helps understand the age profile of CityFlo customers and provides detailed demographic information.

---

### 🕐 Peak Hour Trip Distribution

A donut chart comparing:

- Peak-hour trips
- Non-peak-hour trips

### Business Purpose

This visualization helps identify how much demand occurs during peak operating hours.

It can support:

- Fleet planning
- Driver allocation
- Schedule optimization
- Capacity management

---

### 🏙️ Average Delay by City

A bar chart comparing average delay minutes across cities:

- Delhi NCR
- Hyderabad
- Chennai
- Pune
- Bangalore
- Mumbai

### Business Insight

Delhi NCR records the highest average delay among the displayed cities, while Mumbai records the lowest.

### Business Purpose

This analysis can help operations teams identify cities where punctuality and route efficiency need improvement.

---

### 🌧️ Average Delay by Weather

A line chart showing average delay under different weather conditions:

- Heavy Rain
- Fog
- Haze
- Rain
- Clear
- Cloudy

### Business Insight

Heavy rain shows the highest average delay in the dashboard.

This indicates that adverse weather conditions can have a significant impact on service punctuality.

### Business Purpose

The analysis can support:

- Weather-based contingency planning
- Schedule adjustments
- Additional fleet planning
- Route-level risk management

---

### 🚌 Average Occupancy by Bus Type

A horizontal bar chart comparing occupancy across:

- AC Sleeper
- Non-AC Seater
- AC Seater
- Premium AC

### Business Insight

AC Sleeper shows the highest average occupancy among the displayed bus types.

### Business Purpose

This analysis can help with:

- Fleet allocation
- Capacity planning
- Bus-type optimization
- Route assignment

---

# 3️⃣ Dashboard 3 – Route, Revenue & Customer Experience Analysis

## 🎯 Purpose

The **Route, Revenue & Customer Experience Dashboard** combines operational data with customer experience and financial performance.

It focuses on:

- Delays
- Customer ratings
- Route distance
- Revenue
- Occupancy
- Route performance

---

## 📌 KPI Cards

The dashboard contains:

- **Trip ID**
- **Delay Mins**
- **Rating**
- **Occupancy Rate**
- **Total Revenue**
- **Route ID**

---

## 📊 Dashboard Visualizations

### 📉 Delay & Customer Rating Over Time

A combined time-series chart displaying:

- Delay minutes
- Customer rating

over the trip date.

### Business Purpose

This visualization helps investigate whether operational delays are associated with changes in customer satisfaction.

It can be used to monitor service quality over time.

---

### 📍 Distance vs Net Revenue

A scatter plot comparing:

- Distance in kilometres
- Net revenue in INR

### Business Insight

The dashboard shows a strong positive relationship between distance and net revenue.

In general, longer routes tend to generate higher net revenue.

### Business Purpose

This relationship can support:

- Pricing decisions
- Route planning
- Revenue forecasting
- Route profitability analysis

---

### 🛣️ Occupancy by Route

A line chart showing occupancy percentage across different routes.

### Business Purpose

This visualization helps identify routes with:

- High passenger utilization
- Low passenger utilization
- Demand fluctuations

Routes with consistently high occupancy may require additional capacity, while low-occupancy routes may require schedule or route optimization.

---

# 4️⃣ Dashboard 4 – Customer, Subscription & Booking Analysis

## 🎯 Purpose

The **Customer, Subscription & Booking Analysis Dashboard** focuses on customer behavior and preferences.

It provides insights into:

- Customer ratings
- Age groups
- Subscription plans
- Payment methods
- Complaints
- Booking channels

---

## 📌 KPI Cards

The dashboard displays:

- **Trip ID**
- **Rating**
- **Customer ID**
- **Subscription Type**

---

## 📊 Dashboard Visualizations

### ⭐ Customer Rating Distribution

A bar chart showing the distribution of customer ratings:

- 1 Star
- 2 Stars
- 3 Stars
- 4 Stars
- 5 Stars

### Business Insight

The dashboard shows a significant concentration of higher customer ratings, particularly 5-star ratings.

This indicates generally positive customer feedback within the analyzed dataset.

---

### 👥 Customer Age Group Distribution

A donut chart showing customer distribution across:

- 18–25
- 26–35
- 36–45
- 46–60

### Business Insight

The 26–35 age group represents the largest displayed customer segment.

### Business Purpose

This information can be used for:

- Targeted marketing
- Customer segmentation
- Subscription campaigns
- Personalized offers

---

### 💳 Customers by Subscription Type

A chart showing customer distribution across:

- Corporate Plan
- Monthly Pass
- Single Ride
- Weekly Pass

### Business Purpose

This visualization helps identify popular subscription models and understand recurring versus one-time customers.

---

### 💰 Payment Mode Distribution

A horizontal bar chart showing usage of:

- UPI
- Wallet
- Debit Card
- Cash
- Net Banking
- Credit Card

### Business Insight

UPI and other digital payment methods represent a major portion of payment activity.

### Business Purpose

This highlights the importance of maintaining a convenient and reliable digital payment experience.

---

### 📢 Complaint Status Distribution

A bar chart showing:

- Complaint = False
- Complaint = True

### Business Insight

The majority of recorded trips do not have a complaint.

However, complaint cases should still be monitored to identify recurring service issues.

---

### 🔻 Revenue by Booking Channel

A funnel chart comparing revenue across:

- Website
- Corporate Portal
- Mobile App
- Kiosk

### Business Purpose

This visualization helps compare the relative contribution of different booking channels and supports decisions around digital booking strategy.

---

# 🔍 Key Business Insights

Based on the dashboard analysis, the following insights were identified:

### 1. Mumbai is a Strong Revenue Market

Mumbai generates the highest net revenue among the displayed cities.

### 2. Trip Completion is Dominant

Completed trips account for the largest proportion of trip statuses.

### 3. Delhi NCR Has Higher Delays

Delhi NCR records the highest average delay among the cities shown in the dashboard.

### 4. Weather Influences Delays

Heavy rain shows the highest average delay compared with the other weather conditions.

### 5. AC Sleeper Has High Occupancy

AC Sleeper has the highest average occupancy among the displayed bus types.

### 6. Distance is Positively Related to Revenue

Longer routes generally generate higher net revenue.

### 7. 26–35 is a Major Customer Segment

The 26–35 age group represents the largest displayed age-group segment.

### 8. Higher Ratings are Common

The rating distribution shows a significant concentration of higher customer ratings.

### 9. Digital Payments are Important

UPI and other digital payment methods represent a large share of payment activity.

### 10. Most Trips Have No Complaint

The majority of recorded trips do not have a complaint associated with them.

---

# 📈 Exploratory Data Analysis

The project includes detailed exploratory data analysis using Python.

## Univariate Analysis

The following techniques were used:

- Histograms
- Bar charts
- Pie charts
- Box plots
- Mean
- Median
- Mode
- Standard deviation
- Skewness
- Kurtosis

## Bivariate Analysis

The following techniques were used:

- Scatter plots
- Correlation analysis
- Grouped analysis
- Cross-tabulation
- Box plots
- Comparative visualizations

## Multivariate Analysis

The project also includes:

- Correlation heatmaps
- Pair plots
- Multi-variable comparisons
- City-level analysis
- Delay analysis
- Revenue analysis

---

# 🧪 Statistical Analysis

Statistical techniques were used to validate relationships identified during exploratory analysis.

## Pearson Correlation

Used to study relationships between numerical variables such as:

- Distance
- Fare

---

## Independent Samples T-Test

Used to compare delay behavior between:

- Peak-hour trips
- Non-peak-hour trips

---

## One-Way ANOVA

Used to determine whether average fares differ significantly between different bus types.

---

## Chi-Square Test

Used to examine relationships between categorical variables such as:

- City
- Trip Status

---

# 💡 Business Recommendations

Based on the analysis, the following recommendations can be considered:

### 1. Improve High-Delay Cities

Operational teams should investigate traffic, route planning, scheduling, and fleet allocation in cities with higher average delays.

### 2. Develop Weather-Based Planning

Heavy rain and other adverse weather conditions should be considered when planning schedules and allocating buses.

### 3. Optimize Bus Allocation

Bus capacity should be adjusted based on route-level occupancy.

### 4. Reduce Cancelled and No-Show Trips

The company can investigate the causes of cancellations and no-shows to improve seat utilization and revenue.

### 5. Monitor Customer Satisfaction

Customer ratings should be monitored together with delays to identify potential service-quality issues.

### 6. Strengthen Digital Payment Options

Digital payment methods should remain reliable and user-friendly because of their high usage.

### 7. Improve Subscription Strategies

Customer age groups and subscription preferences can be used to create targeted subscription offers.

### 8. Optimize Booking Channels

Revenue contribution from different booking channels can be used to prioritize investments in high-performing digital platforms.

### 9. Analyze Route Profitability

Distance, occupancy, and revenue should be analyzed together when making route-planning decisions.

---

# 📁 Project Structure

    Cityflow-Bus-Service-Metro-Cities/
    │
    ├── Dashboard/
    │   ├── Dashboard_1.png
    │   ├── Dashboard_2.png
    │   ├── Dashboard_3.png
    │   └── Dashboard_4.png
    │
    ├── Cityflo_Data_Inspect.ipynb
    ├── Cityflo_Data_Clean_&_Prepare_.ipynb
    ├── Cityflo_Data_Analyze.ipynb
    ├── Cityflo_Data_Report.ipynb
    │
    ├── cityflo_bus_service_metro_cities.csv
    ├── cityflo_bus_service_metro_cities_cleaned.csv
    │
    └── README.md

---

# ▶️ How to Run the Project

## Step 1 – Clone the Repository

    git clone https://github.com/Anwesapanja/Cityflow-Bus-Service-Metro-Cities.git

## Step 2 – Navigate to the Project Directory

    cd Cityflow-Bus-Service-Metro-Cities

## Step 3 – Install Required Libraries

    pip install pandas numpy matplotlib seaborn scipy jupyter

## Step 4 – Start Jupyter Notebook

    jupyter notebook

## Step 5 – Run the Notebooks

Run the notebooks in the following order:

    1. Cityflo_Data_Inspect.ipynb
           ↓
    2. Cityflo_Data_Clean_&_Prepare_.ipynb
           ↓
    3. Cityflo_Data_Analyze.ipynb
           ↓
    4. Cityflo_Data_Report.ipynb

---

# 📚 Project Resources

## 📊 Dataset / Google Spreadsheet

https://docs.google.com/spreadsheets/d/1lvvWRxPfKCT4T3xvIqXpyCBdnCnL86It0-TIU80xqVE/edit?gid=1723667175#gid=1723667175

## 📓 Kaggle Notebook

https://www.kaggle.com/code/anwesapanja/cityflo-data-analysis

## 💻 GitHub Repository

https://github.com/Anwesapanja/Cityflow-Bus-Service-Metro-Cities

---

# 📌 Conclusion

The **CityFlo Bus Service – Metro Cities Data Analysis** project demonstrates a complete end-to-end data analytics workflow, starting from raw data and ending with an interactive Business Intelligence dashboard.

The project combines:

**Data Cleaning + Feature Engineering + Exploratory Data Analysis + Statistical Analysis + Business Analysis + Power BI Dashboard = Actionable Business Insights**

The dashboards provide a comprehensive view of:

- City performance
- Revenue
- Trip volume
- Trip status
- Delays
- Weather impact
- Occupancy
- Route performance
- Customer ratings
- Customer demographics
- Subscription types
- Payment modes
- Complaints
- Booking channels

Overall, this project demonstrates how data analytics and visualization can be used to convert raw transportation data into meaningful insights that support:

- Operational planning
- Revenue optimization
- Customer experience improvement
- Capacity planning
- Route optimization
- Business decision-making

---

# 👤 Author

**Anwesa Panja**

### Skills Demonstrated

- Python
- Pandas
- NumPy
- SQL
- Data Cleaning
- Exploratory Data Analysis
- Statistical Analysis
- Data Visualization
- Power BI
- Business Intelligence
- Dashboard Development

---

# ⭐ Project Links

### 📊 Dataset / Google Spreadsheet

https://docs.google.com/spreadsheets/d/1lvvWRxPfKCT4T3xvIqXpyCBdnCnL86It0-TIU80xqVE/edit?gid=1723667175#gid=1723667175

### 📓 Kaggle Notebook

https://www.kaggle.com/code/anwesapanja/cityflo-data-analysis

### 💻 GitHub Repository

https://github.com/Anwesapanja/Cityflow-Bus-Service-Metro-Cities
