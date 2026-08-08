# 🚌 CityFlo Bus Service – Metro Cities Data Analysis

> An end-to-end Data Analytics and Business Intelligence project using Python, Statistical Analysis, and Power BI to analyse bus operations, revenue, customer behaviour, delays, occupancy, and service performance across metro cities.

---

## 📌 Table of Contents

- [Project Overview](#-project-overview)
- [Business Objective](#-business-objective)
- [Dataset](#-dataset)
- [Project Workflow](#-project-workflow)
- [Dashboard](#-dashboard)
  - [Dashboard 1 – City & Revenue Overview](#dashboard-1--city--revenue-overview)
  - [Dashboard 2 – Operations & Capacity](#dashboard-2--operations--capacity)
  - [Dashboard 3 – Delay, Rating & Route Performance](#dashboard-3--delay-rating--route-performance)
  - [Dashboard 4 – Customer & Booking Behaviour](#dashboard-4--customer--booking-behaviour)
- [Data Cleaning](#-data-cleaning)
- [Feature Engineering](#-feature-engineering)
- [Exploratory Data Analysis](#-exploratory-data-analysis)
- [Statistical Analysis](#-statistical-analysis)
- [Key Insights](#-key-insights)
- [Business Recommendations](#-business-recommendations)
- [Technologies Used](#-technologies-used)
- [Repository Structure](#-repository-structure)
- [How to Run](#-how-to-run)
- [Project Links](#-project-links)
- [Future Scope](#-future-scope)
- [Limitations](#-limitations)
- [Conclusion](#-conclusion)
- [Author](#-author)

---

# 📌 Project Overview

CityFlo Bus Service – Metro Cities is an end-to-end Data Analytics and Business Intelligence project developed to analyse bus-service operations across major Indian metro cities.

The project transforms raw trip-level data into meaningful business insights by analysing:

- 🚌 Trip and route performance
- 💰 Revenue generation
- ⏱️ Trip delays and operational efficiency
- 👥 Customer demographics and behaviour
- ⭐ Customer ratings and complaints
- 🪑 Bus occupancy and capacity utilisation
- 💳 Payment behaviour
- 🎫 Subscription patterns
- 🌦️ Weather impact on operations
- 📱 Booking-channel performance

The project follows a complete analytics workflow:

```text
Raw Data
   ↓
Data Inspection
   ↓
Data Cleaning
   ↓
Data Preparation
   ↓
Feature Engineering
   ↓
Exploratory Data Analysis
   ↓
Statistical Analysis
   ↓
KPI Development
   ↓
Power BI Dashboard
   ↓
Business Insights
   ↓
Business Recommendations

Note: The dataset is synthetic and is used for learning, analytics practice, and portfolio purposes. It does not represent actual CityFlo operational data.

🎯 Business Objective

The primary objective of this project is to understand the factors affecting:

Revenue
Customer satisfaction
Operational efficiency
Bus occupancy
Trip delays
Route performance
Customer behaviour
Key Business Questions
Which cities generate the highest revenue?
Which cities have the highest trip volume?
Which cities experience the highest average delays?
Does weather have an impact on trip delays?
Are peak-hour trips more likely to experience delays?
Which bus types have the highest occupancy?
Does route distance influence net revenue?
Is there a relationship between delay and customer rating?
Which payment modes are most frequently used?
Which subscription types have the highest number of customers?
Which booking channels generate the most revenue?
What percentage of trips are completed, delayed, cancelled, or marked as no-show?
📊 Dataset

The dataset contains trip-level information related to bus operations, customers, routes, revenue, payments, bookings, and service performance.

Main Data Categories
Category	Example Columns
Trip Information	trip_id, trip_date, trip_status
Route Information	route_id, route_name, distance_km
Customer Information	customer_id, age, gender, rating
Bus Information	bus_type
Operational Information	delay_minutes, occupancy_pct, is_peak_hour
Financial Information	fare_inr, discount_inr, net_revenue_inr
Booking Information	booking_mode, payment_mode
Subscription	subscription_type
Weather	weather
Customer Service	complaint_raised
Cities Analysed

The dashboard analyses the following metro cities:

Mumbai
Pune
Bangalore
Chennai
Hyderabad
Delhi NCR
🔄 Project Workflow
1. Data Inspection

The raw dataset was inspected to understand:

Dataset dimensions
Data types
Missing values
Duplicate records
Unique values
Categorical variables
Numerical variables
Outliers
Date formats
Data inconsistencies
2. Data Cleaning

The dataset was cleaned before performing analysis.

The cleaning process included:

Removing duplicate records
Handling missing values
Standardising categorical values
Removing unnecessary spaces
Converting columns to appropriate data types
Parsing date columns
Standardising Boolean values
Validating age values
Checking occupancy percentages
Reviewing extreme fare values
Validating trip and customer IDs
3. Feature Engineering

Several derived variables were created to support business analysis.

Net Revenue
Net Revenue = Fare - Discount
Delayed Trip

A trip is classified as delayed when:

delay_minutes > 5
Age Groups

Customer ages were grouped into meaningful age categories for demographic analysis.

Date Features

The trip date was used to derive:

Year
Month
Weekday
Monthly trends
📊 Dashboard

The project contains a four-page interactive Power BI dashboard.

The dashboard is designed to provide both high-level business insights and detailed operational analysis.

Dashboard Pages
Page	Dashboard	Main Focus
1	City & Revenue Overview	Overall business and city performance
2	Operations & Capacity	Delays, weather, peak hours and occupancy
3	Delay, Rating & Route Performance	Service quality, routes and revenue
4	Customer & Booking Behaviour	Customers, payments, subscriptions and bookings
Interactive Filters

The dashboard provides interactive filters for:

Gender
Bus Type
Payment Mode
Days
City
Weather
Age Group
Booking Mode

These filters allow users to dynamically analyse the business based on different customer segments, cities, weather conditions, bus types, and booking behaviours.

📈 Dashboard 1 – City & Revenue Overview

Purpose

The first dashboard provides an executive-level overview of the bus-service business.

It focuses on:

Trip performance
Customer count
Route coverage
Revenue
City performance
Trip status
Monthly revenue
Customer demographics
KPI Cards

The dashboard displays the following KPIs:

Trip ID
Customer ID
Age
Route ID
Trip Date
Total Net Revenue

These KPI cards provide a quick summary of the overall business performance.

Trips by City

The bar chart compares the total number of trips across cities.

This helps identify:

High-demand cities
Low-demand cities
Cities requiring additional fleet capacity
Markets with high operational activity
Revenue by City

The table ranks cities based on net revenue.

The displayed ranking is:

Rank	City
1	Mumbai
2	Pune
3	Bangalore
4	Chennai
5	Hyderabad
6	Delhi NCR

This visual helps identify the strongest revenue-generating markets.

Trip Status Distribution

The pie chart shows the distribution of:

Completed
Delayed-Completed
Cancelled
No-show

The displayed dashboard shows approximately:

Completed: 66%
Delayed-Completed: 12%
Cancelled: 11.7%
No-show: 10.4%

This helps measure service reliability and identify the proportion of trips affected by operational issues.

Monthly Revenue Trend

The line chart displays revenue across the months.

It helps identify:

High-revenue months
Low-revenue months
Seasonal patterns
Revenue fluctuations

This information can support demand planning and revenue optimisation.

Customer Gender Distribution

The donut chart shows the gender distribution of customers.

The displayed dashboard shows approximately:

Female: 50.8%
Male: 44.7%
Other: Remaining share

This can support customer segmentation and targeted marketing.

⏱️ Dashboard 2 – Operations & Capacity

Purpose

The second dashboard focuses on operational efficiency and capacity utilisation.

It analyses:

Delay
Occupancy
Peak-hour demand
Weather conditions
City-level delays
Bus-type utilisation
KPI Cards

The dashboard includes:

Average Delay
Occupancy Rate
Number of Cities
Number of Age Groups
Number of Weather Categories
Number of Bus Types

The displayed dashboard reports approximately:

Average Delay: 61 minutes
Occupancy Rate: 58%
Customer Age Distribution

The treemap displays the distribution of customers across different age values.

This provides a visual understanding of the customer age structure.

Peak Hour Trip Distribution

The donut chart compares peak-hour and non-peak-hour trips.

The displayed dashboard shows approximately:

Non-Peak: 60.1%
Peak: 39.9%

This helps understand demand concentration during peak periods.

Average Delay by City

The bar chart compares the average delay across cities.

The displayed dashboard shows:

Delhi NCR
Hyderabad
Chennai
Pune
Bangalore
Mumbai

Delhi NCR has the highest displayed average delay.

This indicates an opportunity for city-specific operational improvements.

Average Delay by Weather

The chart compares average delays under:

Heavy Rain
Fog
Haze
Rain
Clear
Cloudy

The displayed analysis shows higher average delays during adverse weather conditions, particularly heavy rain.

Potential improvements include:

Weather-aware scheduling
Additional buffer time
Proactive customer notifications
Better fleet planning
Average Occupancy by Bus Type

The horizontal bar chart compares occupancy across:

AC Sleeper
Non-AC Seater
AC Seater
Premium AC

The displayed dashboard shows relatively similar occupancy levels across bus types, with AC Sleeper showing the highest displayed occupancy.

This analysis can support fleet allocation and capacity planning.

📉 Dashboard 3 – Delay, Rating & Route Performance

Purpose

The third dashboard connects operational performance with customer experience and route economics.

It analyses:

Delay
Customer rating
Revenue
Distance
Occupancy
Route performance
KPI Cards

The dashboard displays:

Total Trips
Average Delay
Rating
Occupancy Rate
Total Revenue
Route Count
Delay & Customer Rating Over Time

The time-series chart compares:

Delay minutes
Customer rating
Trip date

This helps identify periods where increased delays may coincide with changes in customer satisfaction.

Distance vs Net Revenue

The scatter plot compares:

Distance (km)
        vs
Net Revenue (INR)

The displayed data shows a strong positive relationship between route distance and net revenue.

This suggests that longer routes generally generate higher revenue.

This analysis can support:

Fare planning
Revenue forecasting
Route economics
Route expansion decisions
Occupancy by Route

The route-level chart compares occupancy across routes.

It helps identify:

High-utilisation routes
Low-utilisation routes
Demand fluctuations
Capacity imbalance

This can support:

Fleet allocation
Route frequency planning
Schedule optimisation
Capacity planning
👥 Dashboard 4 – Customer & Booking Behaviour

Purpose

The fourth dashboard focuses on customer behaviour and booking patterns.

It analyses:

Customer ratings
Age groups
Subscription types
Payment modes
Complaints
Booking channels
Revenue
Customer Rating Distribution

The bar chart shows customer ratings from 1 to 5.

The displayed dashboard shows a larger concentration of higher ratings, particularly ratings 4 and 5.

This provides an overview of customer satisfaction.

Customer Age Group Distribution

Customers are divided into:

18–25
26–35
36–45
46–60

The displayed dashboard shows 26–35 as the largest customer segment.

This information can support:

Marketing campaigns
Customer segmentation
Subscription design
Loyalty programmes
Customers by Subscription Type

The chart compares:

Corporate Plan
Monthly Pass
Single Ride
Weekly Pass

This helps distinguish recurring customers from occasional users.

Payment Mode Distribution

The chart compares:

UPI
Wallet
Debit Card
Cash
Net Banking
Credit Card

The displayed dashboard shows strong usage of UPI and Wallet.

This highlights the importance of maintaining a smooth digital payment experience.

Complaint Status Distribution

The chart compares trips with and without complaints.

Complaints can be analysed alongside:

Delay
City
Route
Bus type
Weather
Rating

This can help identify the root causes of customer dissatisfaction.

Revenue by Booking Channel

The funnel chart compares revenue across:

Website
Corporate Portal
Mobile App
Kiosk

The displayed dashboard shows the Website as the dominant booking channel.

This helps identify where customers prefer to book and where digital investment should be prioritised.

📊 Exploratory Data Analysis

Exploratory Data Analysis was performed to identify patterns, trends, relationships, and anomalies within the dataset.

Univariate Analysis

The following visualisations were used:

Histograms
Bar charts
Box plots
Pie charts
Donut charts
Summary statistics
Bivariate Analysis

Relationships analysed include:

Distance vs Fare
Distance vs Net Revenue
Delay vs Weather
Delay vs City
Occupancy vs Bus Type
Rating vs Delay
Revenue vs City
Multivariate Analysis

The analysis also includes:

Correlation analysis
Heatmaps
Grouped comparisons
Time-series analysis
Route-level comparisons
🧪 Statistical Analysis

Statistical tests were performed to validate relationships identified during exploratory analysis.

Pearson Correlation

Used to analyse the relationship between:

distance_km ↔ fare_inr
Independent Samples t-test

Used to compare average delays between:

Peak-hour trips ↔ Non-peak-hour trips
One-way ANOVA

Used to determine whether average fares differ significantly across different bus types.

Chi-square Test

Used to investigate whether:

City ↔ Trip Status

are statistically associated.

💡 Key Insights
1. Revenue Performance

Mumbai and Pune are among the strongest revenue-generating cities in the displayed dashboard.

2. Distance and Revenue

The scatter plot indicates a strong positive relationship between route distance and net revenue.

3. Weather and Delays

Adverse weather conditions, particularly heavy rain, are associated with higher average delays.

4. City-Level Delays

Delhi NCR has the highest displayed average delay and may require targeted operational improvements.

5. Occupancy

The overall displayed occupancy rate is approximately 58%, indicating opportunities to improve capacity utilisation.

6. Customer Satisfaction

Higher ratings, particularly 4 and 5, account for a substantial proportion of customer feedback.

7. Digital Payments

UPI and Wallet are among the most frequently used payment modes.

8. Booking Channels

The Website is the dominant booking channel in the displayed revenue analysis.

🚀 Business Recommendations
Improve Operational Efficiency
Focus on high-delay cities and routes.
Introduce weather-aware scheduling.
Add operational buffers during adverse weather.
Analyse peak-hour congestion.
Monitor route-level delays.
Improve Fleet Utilisation
Monitor occupancy by route.
Increase frequency on high-demand routes.
Optimise under-utilised routes.
Match bus types with demand patterns.
Improve Customer Experience
Investigate low-rated trips.
Connect complaints with delays and routes.
Provide proactive delay notifications.
Monitor customer ratings over time.
Improve Revenue
Analyse revenue per kilometre.
Compare city-level revenue.
Optimise pricing by route and bus type.
Promote recurring subscription plans.
Strengthen Digital Channels
Improve the website booking experience.
Maintain reliable UPI and wallet payments.
Analyse booking-channel conversion.
Encourage repeat bookings and subscriptions.
🛠️ Technologies Used
Technology	Purpose
Python	Data analysis and processing
Pandas	Data cleaning and manipulation
NumPy	Numerical operations
Matplotlib	Data visualisation
Seaborn	Statistical visualisation
SciPy	Statistical analysis
Jupyter Notebook	Data analysis and documentation
Power BI	Interactive dashboard
Google Sheets	Dataset management
Kaggle	Notebook hosting
GitHub	Version control
📁 Repository Structure
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
▶️ How to Run
1. Clone the Repository
git clone https://github.com/Anwesapanja/Cityflow-Bus-Service-Metro-Cities.git
2. Navigate to the Project Directory
cd Cityflow-Bus-Service-Metro-Cities
3. Install Required Libraries
pip install pandas numpy matplotlib seaborn scipy jupyter
4. Start Jupyter Notebook
jupyter notebook
5. Run the Notebooks in Order
1. Cityflo_Data_Inspect.ipynb
2. Cityflo_Data_Clean_&_Prepare_.ipynb
3. Cityflo_Data_Analyze.ipynb
4. Cityflo_Data_Report.ipynb
🔗 Project Links
GitHub Repository

https://github.com/Anwesapanja/Cityflow-Bus-Service-Metro-Cities

Kaggle Notebook

https://www.kaggle.com/code/anwesapanja/cityflo-data-analysis

Google Sheets Dataset

https://docs.google.com/spreadsheets/d/1lvvWRxPfKCT4T3xvIqXpyCBdnCnL86It0-TIU80xqVE/edit?gid=1723667175#gid=1723667175

🔮 Future Scope

The project can be extended with:

📈 Demand forecasting
🤖 Machine-learning-based delay prediction
💰 Revenue forecasting
👥 Customer segmentation
🔄 Customer churn prediction
🗺️ Geographic route analysis
🚌 Dynamic fleet allocation
📊 Real-time operational monitoring
⭐ Customer satisfaction prediction
🎯 Dynamic pricing
🌦️ Weather-based demand forecasting
⚠️ Limitations
The dataset is synthetic.
The results should not be interpreted as actual CityFlo business performance.
Correlation does not imply causation.
Dashboard results depend on the selected filters.
Statistical conclusions are specific to the available dataset.
Geographic analysis is limited by the available location information.
🏁 Conclusion

This project demonstrates a complete Data Analytics and Business Intelligence workflow for a transportation business.

The project transforms raw trip-level data into actionable insights across:

Operations
     ↓
Revenue
     ↓
Customer Behaviour
     ↓
Service Quality
     ↓
Capacity Utilisation
     ↓
Business Decisions

The four-page Power BI dashboard provides a consolidated view of:

Trip performance
Revenue
City performance
Delays
Weather impact
Occupancy
Route performance
Customer ratings
Customer demographics
Subscription behaviour
Payment methods
Complaints
Booking channels

Overall, the project demonstrates how raw operational data can be transformed into meaningful business intelligence, visual insights, and practical recommendations.

👤 Author
Anwesa Panja

Data Analytics | Python | SQL | Power BI | Data Visualisation

⭐ If you find this project useful, feel free to explore the notebooks, dashboard, and analysis.
