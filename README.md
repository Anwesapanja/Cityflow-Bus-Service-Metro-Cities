🚌 CityFlo Bus Service – Metro Cities Data Analysis

An end-to-end Data Analytics & Business Intelligence project using Python, Statistical Analysis, and Power BI to analyse bus operations, revenue, customer behaviour, delays, occupancy, and service performance across metro cities.

📌 Table of Contents
Project Overview
Business Objective
Dataset
Project Workflow
Dashboard
Dashboard 1 – City & Revenue Overview
Dashboard 2 – Operations & Capacity
Dashboard 3 – Delay, Rating & Route Performance
Dashboard 4 – Customer & Booking Behaviour
Key Insights
Business Recommendations
Technologies Used
Repository Structure
How to Run
Project Links
Future Scope
Limitations
Author
📌 Project Overview

This project analyses a CityFlo-style bus-service dataset to understand operational performance, revenue generation, customer behaviour, service quality, and capacity utilisation.

The project follows a complete data analytics lifecycle:

Raw Dataset
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

The analysis focuses on major metro-city bus operations and provides an interactive dashboard for business decision-making.

Note: The dataset is synthetic and is used for learning, analytics practice, and portfolio purposes. It does not represent actual CityFlo operational data.

🎯 Business Objective

The main objective is to identify patterns and relationships that can help improve:

🚌 Operational efficiency
💰 Revenue performance
⏱️ On-time performance
🪑 Bus occupancy
⭐ Customer satisfaction
👥 Customer retention
🎫 Subscription adoption
💳 Payment and booking experience
Key Business Questions
Which cities generate the highest revenue?
Which cities have the highest trip volume?
Which cities experience the highest delays?
Does weather affect delays?
Are peak-hour trips more likely to experience delays?
Which bus types have the highest occupancy?
Does route distance influence revenue?
How do delays affect customer ratings?
Which payment modes are most popular?
Which subscription types have the highest customer volume?
Which booking channels generate the most revenue?
What percentage of trips are cancelled or marked as no-show?
📊 Dataset

The dataset contains trip-level information related to bus operations and customer behaviour.

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

The dashboard focuses on major metro-city markets including:

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
Unique categories
Invalid values
Outliers
Date formats
Boolean inconsistencies
2. Data Cleaning

The dataset was cleaned before analysis by:

Removing duplicate records
Standardising categorical values
Removing unnecessary whitespace
Converting columns to appropriate data types
Parsing date columns
Handling missing values
Standardising Boolean values
Validating customer ages
Checking occupancy values
Reviewing extreme fare values
Validating trip IDs
3. Feature Engineering

Additional variables were created to support business analysis.

Net Revenue
Net Revenue = Fare - Discount
Delayed Trip

A trip is classified as delayed when:

Delay Minutes > 5
Age Groups

Customers are grouped into meaningful age categories for demographic analysis.

Date Features

The trip date is used to derive:

Year
Month
Weekday
Monthly trends
📊 Dashboard

The project contains a four-page Power BI dashboard.

The dashboard is designed to move from a high-level business overview to detailed operational and customer analysis.

Dashboard Pages
Page	Focus
Page 1	City & Revenue Overview
Page 2	Operations & Capacity
Page 3	Delay, Rating & Route Performance
Page 4	Customer & Booking Behaviour
Dashboard Filters

Users can interactively filter the dashboard using:

Gender
Bus Type
Payment Mode
Days
City
Weather
Age Group
Booking Mode
📈 Dashboard 1 – City & Revenue Overview

Purpose

This page provides an executive-level overview of the entire bus-service business.

It focuses on:

Total trips
Customers
Routes
Revenue
City performance
Trip status
Monthly revenue
Customer demographics
KPI Cards

The dashboard displays:

Trip ID
Customer ID
Age
Route ID
Trip Date
Total Net Revenue

These KPIs provide a quick snapshot of the business.

Trips by City

The bar chart compares trip volume across cities.

It helps identify:

High-demand markets
Low-demand markets
Areas requiring additional capacity
Cities with high operational activity
Revenue by City

The table ranks cities based on net revenue.

The displayed dashboard shows:

Mumbai
Pune
Bangalore
Chennai
Hyderabad
Delhi NCR

This helps identify the strongest revenue-generating markets.

Trip Status Distribution

The pie chart shows:

Completed
Delayed-Completed
Cancelled
No-show

This provides an overview of service reliability and trip outcomes.

Monthly Revenue Trend

The line chart tracks revenue over time and helps identify:

High-revenue periods
Low-revenue periods
Seasonal trends
Revenue fluctuations
Customer Gender Distribution

The donut chart provides an overview of customer gender composition.

⏱️ Dashboard 2 – Operations & Capacity

Purpose

This dashboard focuses on operational efficiency and capacity utilisation.

It analyses:

Delay
Occupancy
Peak-hour trips
Weather
City-level delays
Bus-type utilisation
KPI Cards

The page displays:

Average Delay
Occupancy Rate
Number of Cities
Number of Age Groups
Number of Weather Categories
Number of Bus Types
Customer Age Distribution

The treemap shows the distribution of customers across different ages.

This helps understand the customer demographic structure.

Peak Hour Trip Distribution

The donut chart compares:

Peak-hour trips
Non-peak-hour trips

This helps determine how much demand occurs during peak periods.

Average Delay by City

The bar chart compares average delay between cities.

The displayed dashboard shows Delhi NCR with the highest average delay.

This can help management identify locations requiring operational improvement.

Average Delay by Weather

The chart compares delays under:

Heavy Rain
Fog
Haze
Rain
Clear
Cloudy

The analysis indicates higher delays under adverse weather conditions.

Average Occupancy by Bus Type

The chart compares occupancy across:

AC Sleeper
Non-AC Seater
AC Seater
Premium AC

This helps determine which bus types are being utilised most efficiently.

📉 Dashboard 3 – Delay, Rating & Route Performance

Purpose

This page connects operations, customer experience, and route economics.

It analyses:

Delay
Customer rating
Revenue
Distance
Occupancy
Route performance
KPI Cards

The dashboard includes:

Total Trips
Average Delay
Rating
Occupancy Rate
Total Revenue
Route Count
Delay & Customer Rating Over Time

The time-series chart compares delay and customer rating across the year.

It helps identify whether periods of increased delays coincide with changes in customer satisfaction.

Distance vs Net Revenue

The scatter plot compares:

Distance (km)
        vs
Net Revenue (INR)

The displayed data shows a strong positive relationship.

This suggests that longer routes generally generate higher revenue.

Occupancy by Route

The route-level visual compares occupancy across routes.

It helps identify:

High-demand routes
Low-utilisation routes
Capacity imbalance
Opportunities for route optimisation
👥 Dashboard 4 – Customer & Booking Behaviour

Purpose

This page focuses on customer demographics, satisfaction, subscriptions, payments, complaints, and booking channels.

Customer Rating Distribution

The bar chart displays the distribution of ratings from 1 to 5.

Higher ratings, especially 4 and 5, represent a significant portion of customer feedback.

Customer Age Group Distribution

The donut chart shows customer groups such as:

18–25
26–35
36–45
46–60

The displayed dashboard shows 26–35 as the largest age group.

Customers by Subscription Type

The chart compares:

Corporate Plan
Monthly Pass
Single Ride
Weekly Pass

This helps understand recurring versus occasional customers.

Payment Mode Distribution

The dashboard compares:

UPI
Wallet
Debit Card
Cash
Net Banking
Credit Card

UPI and Wallet show strong usage in the displayed dashboard.

Complaint Status Distribution

The chart compares trips with and without complaints.

Complaint data can be combined with delay, city, route, weather and rating to identify service-quality problems.

Revenue by Booking Channel

The funnel chart compares revenue contribution across booking channels:

Website
Corporate Portal
Mobile App
Kiosk

The displayed dashboard shows the Website as the dominant booking channel.

🧪 Statistical Analysis

Statistical testing was used to validate relationships found during exploratory analysis.

Pearson Correlation

Used to examine:

Distance ↔ Fare
Independent Samples t-test

Used to compare:

Peak-hour Delay ↔ Non-peak-hour Delay
One-way ANOVA

Used to determine whether average fare differs across bus types.

Chi-square Test

Used to determine whether:

City ↔ Trip Status

are statistically associated.

💡 Key Insights
Revenue

Mumbai and Pune are among the strongest revenue-generating cities in the displayed dashboard.

Distance & Revenue

Longer routes generally generate higher net revenue.

Weather & Delay

Adverse weather conditions are associated with higher average delays.

City-Level Delay

Delhi NCR has the highest displayed average delay and may require targeted operational improvements.

Occupancy

The displayed overall occupancy rate is approximately 58%, indicating opportunities to improve capacity utilisation.

Customer Satisfaction

Ratings 4 and 5 account for a substantial proportion of customer feedback.

Payment Behaviour

UPI and Wallet are among the most commonly used payment methods.

Booking Behaviour

The Website is the dominant booking channel in the displayed revenue analysis.

🚀 Business Recommendations
1. Improve Delay Management
Focus on high-delay cities and routes.
Introduce weather-aware scheduling.
Add buffer time during adverse weather.
Analyse peak-hour congestion.
2. Improve Fleet Utilisation
Monitor occupancy by route.
Increase frequency on high-demand routes.
Optimise low-utilisation routes.
Match bus type with demand.
3. Improve Customer Experience
Investigate low-rated trips.
Analyse complaints against delay and route.
Provide proactive delay notifications.
Monitor customer ratings over time.
4. Improve Revenue
Analyse revenue per kilometre.
Compare city-level revenue.
Optimise pricing by route and bus type.
Promote recurring subscription plans.
5. Strengthen Digital Channels
Improve website booking experience.
Maintain reliable UPI and wallet payments.
Analyse booking-channel performance.
Encourage repeat bookings and subscriptions.
🛠️ Technologies Used
Technology	Purpose
Python	Data analysis
Pandas	Data cleaning and manipulation
NumPy	Numerical computation
Matplotlib	Visualisation
Seaborn	Statistical visualisation
SciPy	Statistical testing
Jupyter Notebook	Analysis
Power BI	Dashboard development
Google Sheets	Dataset management
Kaggle	Analysis notebook
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
Notebook Workflow
Cityflo_Data_Inspect.ipynb
          ↓
Cityflo_Data_Clean_&_Prepare_.ipynb
          ↓
Cityflo_Data_Analyze.ipynb
          ↓
Cityflo_Data_Report.ipynb
▶️ How to Run
Clone the repository
git clone https://github.com/Anwesapanja/Cityflow-Bus-Service-Metro-Cities.git
Navigate to the project
cd Cityflow-Bus-Service-Metro-Cities
Install dependencies
pip install pandas numpy matplotlib seaborn scipy jupyter
Start Jupyter Notebook
jupyter notebook

Run the notebooks in the following order:

1. Cityflo_Data_Inspect.ipynb
2. Cityflo_Data_Clean_&_Prepare_.ipynb
3. Cityflo_Data_Analyze.ipynb
4. Cityflo_Data_Report.ipynb
🔗 Project Links
GitHub

https://github.com/Anwesapanja/Cityflow-Bus-Service-Metro-Cities

Kaggle

https://www.kaggle.com/code/anwesapanja/cityflo-data-analysis

Google Sheets

https://docs.google.com/spreadsheets/d/1lvvWRxPfKCT4T3xvIqXpyCBdnCnL86It0-TIU80xqVE/edit?gid=1723667175#gid=1723667175

🔮 Future Scope

The project can be extended with:

Demand forecasting
Machine-learning-based delay prediction
Revenue forecasting
Customer segmentation
Customer churn prediction
Route optimisation
Dynamic fleet allocation
Geographic route analysis
Dynamic pricing
Weather-based demand forecasting
Real-time operational monitoring
⚠️ Limitations
The dataset is synthetic.
The analysis should not be interpreted as actual CityFlo business performance.
Correlation does not imply causation.
Dashboard values depend on the selected filters and cleaned dataset.
Geographic analysis is limited by the available location data.
Statistical conclusions are specific to this dataset.
🏁 Conclusion

This project demonstrates a complete Data Analytics and Business Intelligence workflow for a transportation business.

It transforms raw trip data into actionable insights across:

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

The four-page dashboard provides management with a consolidated view of revenue, trips, cities, delays, occupancy, routes, customer ratings, demographics, subscriptions, payments, complaints, and booking channels.

The project demonstrates how data can be transformed from raw records into meaningful business insights and practical recommendations.

👤 Author
Anwesa Panja

Data Analytics | Python | SQL | Power BI | Data Visualisation

⭐ If you find this project useful, feel free to explore the notebooks, dashboard, and analysis.
