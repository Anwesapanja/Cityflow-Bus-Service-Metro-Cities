# 🚌 CityFlo Bus Service – Metro Cities Data Analysis

An end-to-end **Data Analytics and Business Intelligence project** that analyses CityFlo bus-service data across major metro cities to understand operational performance, revenue, customer behaviour, route efficiency, delays, occupancy, and service quality.

---

## 📌 Table of Contents

- [Project Overview](#-project-overview)
- [Business Objective](#-business-objective)
- [Business Questions](#-business-questions)
- [Dataset](#-dataset)
- [Project Workflow](#-project-workflow)
- [Data Inspection](#-data-inspection)
- [Data Cleaning and Preparation](#-data-cleaning-and-preparation)
- [Feature Engineering](#-feature-engineering)
- [Exploratory Data Analysis](#-exploratory-data-analysis)
- [Statistical Analysis](#-statistical-analysis)
- [Power BI Dashboard](#-power-bi-dashboard)
- [Dashboard 1 – City and Revenue Overview](#dashboard-1--city-and-revenue-overview)
- [Dashboard 2 – Operations and Capacity](#dashboard-2--operations-and-capacity)
- [Dashboard 3 – Delay, Rating and Route Performance](#dashboard-3--delay-rating-and-route-performance)
- [Dashboard 4 – Customer and Booking Behaviour](#dashboard-4--customer-and-booking-behaviour)
- [Key Business Insights](#-key-business-insights)
- [Business Recommendations](#-business-recommendations)
- [Technologies Used](#-technologies-used)
- [Repository Structure](#-repository-structure)
- [How to Run the Project](#-how-to-run-the-project)
- [Project Resources](#-project-resources)
- [Future Scope](#-future-scope)
- [Limitations](#-limitations)
- [Conclusion](#-conclusion)
- [Author](#-author)

---

# 📌 Project Overview

The **CityFlo Bus Service – Metro Cities Data Analysis** project is an end-to-end Data Analytics and Business Intelligence project developed to understand the performance of a bus transportation service across major Indian metro cities.

The project analyses transportation data from multiple perspectives, including:

- 🚌 Trip performance
- 🏙️ City-wise performance
- 💰 Revenue generation
- 🛣️ Route performance
- ⏱️ Trip delays
- 🪑 Bus occupancy
- 🌦️ Weather impact
- 👥 Customer demographics
- ⭐ Customer satisfaction
- 💳 Payment behaviour
- 🎫 Subscription behaviour
- 📱 Booking channels
- 📢 Customer complaints

The project follows a complete analytics lifecycle:

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
Power BI Dashboard
   ↓
Business Insights
   ↓
Business Recommendations

Note: The dataset used in this project is synthetic and is intended for educational, analytical, and portfolio purposes. It does not represent actual CityFlo operational data.

🎯 Business Objective

The primary objective of this project is to use data-driven analysis to understand the performance of a bus transportation service and identify opportunities for improving:

Operational efficiency
Revenue generation
Fleet utilisation
Customer satisfaction
Route performance
Booking experience
Capacity planning

The project combines Python-based data analysis with Power BI visualisation to convert raw data into meaningful business insights.

❓ Business Questions

The project attempts to answer the following questions:

Which cities have the highest number of trips?
Which cities generate the highest revenue?
Which cities experience the highest average delay?
Does weather affect trip delays?
Are peak-hour trips associated with higher delays?
Which bus types have the highest occupancy?
Does route distance have a relationship with revenue?
Is customer satisfaction related to trip delays?
Which payment modes are most popular?
Which subscription types are most commonly used?
Which booking channels generate the most revenue?
What percentage of trips are completed, delayed, cancelled, or no-show?
Which routes have the highest occupancy?
Which customer age groups form the largest customer segment?
What operational improvements can be made using the available data?
📊 Dataset

The dataset contains information related to bus trips, customers, routes, buses, revenue, bookings, payments, weather, occupancy, delays, and customer experience.

Main Data Categories
Category	Example Fields
Trip Information	trip_id, trip_date, trip_status
Route Information	route_id, route_name, distance_km
Customer Information	customer_id, age, gender, rating
Bus Information	bus_type
Operations	delay_minutes, occupancy_pct, is_peak_hour
Financial	fare_inr, discount_inr, net_revenue_inr
Booking	booking_mode, payment_mode
Subscription	subscription_type
Weather	weather
Customer Service	complaint_raised
Cities Analysed

The project analyses the following metro-city markets:

Mumbai
Pune
Bangalore
Chennai
Hyderabad
Delhi NCR
🔄 Project Workflow

The complete project follows a structured data analytics workflow.

1. Data Inspection

The raw dataset was inspected to understand its structure, quality, and characteristics.

2. Data Cleaning

Data-quality issues such as missing values, duplicates, inconsistent categories, and incorrect data types were addressed.

3. Data Preparation

The cleaned data was transformed into a suitable format for analysis.

4. Feature Engineering

New business-related features and metrics were created.

5. Exploratory Data Analysis

Statistical analysis and visualisations were used to identify patterns and trends.

6. Statistical Analysis

Statistical tests were applied to validate selected relationships.

7. Power BI Dashboard

The analytical results were converted into an interactive Power BI dashboard.

8. Business Insights

The results were interpreted from a business perspective.

9. Recommendations

Actionable recommendations were developed based on the findings.

🔍 Data Inspection

The first stage of the project involved inspecting the raw dataset.

The following checks were performed:

Dataset shape
Number of rows and columns
Data types
Missing values
Duplicate records
Unique values
Numerical variables
Categorical variables
Date columns
Invalid values
Outliers
Data inconsistencies

The purpose of this step was to understand the quality and structure of the data before performing further analysis.

🧹 Data Cleaning and Preparation

The dataset was cleaned and prepared before analysis.

The following activities were performed:

Removed duplicate records
Identified and handled missing values
Standardised categorical values
Removed unnecessary spaces
Converted columns to appropriate data types
Converted date columns into proper date format
Standardised Boolean values
Checked customer age values
Checked occupancy percentages
Validated fare values
Validated trip IDs
Validated customer IDs
Checked inconsistent categories
Reviewed potential outliers

The objective was to create a clean, consistent, and analysis-ready dataset.

🧮 Feature Engineering

Additional features were created to make the analysis more meaningful.

Net Revenue

Net revenue was calculated using:

Net Revenue = Fare - Discount

This metric represents the revenue remaining after applying customer discounts.

Delayed Trip

Trips were classified as delayed when the delay exceeded 5 minutes.

Delayed Trip = Delay Minutes > 5

This classification was used to analyse operational reliability.

Age Groups

Customers were grouped into meaningful age categories:

18–25
26–35
36–45
46–60
60+

This makes demographic analysis easier.

Date Features

The trip date was used to derive:

Year
Month
Weekday
Monthly trends

These features were used for time-based analysis.

📈 Exploratory Data Analysis

Exploratory Data Analysis was performed to understand patterns, distributions, relationships, and trends within the dataset.

Univariate Analysis

The following visualisations were used:

Histograms
Bar charts
Pie charts
Donut charts
Box plots
Summary statistics

Variables analysed include:

Age
Fare
Revenue
Delay
Occupancy
Rating
Distance
Bivariate Analysis

The following relationships were analysed:

Distance vs Fare
Distance vs Net Revenue
Delay vs Weather
Delay vs City
Occupancy vs Bus Type
Rating vs Delay
Revenue vs City
Occupancy vs Route
Multivariate Analysis

The analysis also included:

Correlation analysis
Correlation heatmaps
Grouped comparisons
Time-series analysis
City-level comparisons
Route-level comparisons
Customer segmentation
🧪 Statistical Analysis

Statistical tests were performed to validate selected relationships identified during exploratory analysis.

Pearson Correlation

Pearson correlation was used to analyse the relationship between:

Distance ↔ Fare

The objective was to determine whether route distance has a linear relationship with fare.

Independent Samples t-test

An independent samples t-test was used to compare:

Peak-hour Delay ↔ Non-peak-hour Delay

The objective was to determine whether average delays differ between peak and non-peak periods.

One-way ANOVA

One-way ANOVA was used to compare average fares across different bus types.

The objective was to determine whether there are statistically significant differences in average fare between bus categories.

Chi-square Test

A Chi-square test was used to analyse the relationship between:

City ↔ Trip Status

The objective was to determine whether trip status is associated with the city.

📊 Power BI Dashboard

The final analytical results were transformed into an interactive Power BI Dashboard.

The dashboard consists of four pages, with each page focusing on a different business area.

Dashboard Structure
Dashboard	Main Focus
Dashboard 1	City and Revenue Overview
Dashboard 2	Operations and Capacity
Dashboard 3	Delay, Rating and Route Performance
Dashboard 4	Customer and Booking Behaviour

The dashboard allows users to interact with the data using multiple filters.

Dashboard Filters

The available filters include:

Gender
Bus Type
Payment Mode
Days
City
Weather
Age Group
Booking Mode

These filters allow users to dynamically analyse different customer segments, cities, bus types, weather conditions, and booking behaviours.

📈 Dashboard 1 – City and Revenue Overview
Purpose

The first dashboard provides an executive-level overview of overall business performance.

It focuses on:

Trips
Customers
Routes
Revenue
City performance
Trip status
Monthly revenue
Customer demographics
KPI Cards

The dashboard provides important business KPIs such as:

Trip ID
Customer ID
Age
Route ID
Trip Date
Total Net Revenue

These KPIs provide a quick overview of the business.

Trips by City

The city-wise trip chart compares trip volume across different metro cities.

This helps identify:

High-demand cities
Low-demand markets
Cities with high operational activity
Markets that may require additional fleet capacity

The dashboard shows strong trip activity in cities such as Mumbai and Pune.

Revenue by City

The revenue table compares the net revenue generated by different cities.

The displayed ranking is:

Rank	City
1	Mumbai
2	Pune
3	Bangalore
4	Chennai
5	Hyderabad
6	Delhi NCR

This helps identify the strongest revenue-generating markets.

Trip Status Distribution

The trip-status chart shows the distribution of:

Completed
Delayed-Completed
Cancelled
No-show

The dashboard displays approximately:

Trip Status	Percentage
Completed	66%
Delayed-Completed	12%
Cancelled	11.7%
No-show	10.4%

This provides an overview of service reliability.

Monthly Revenue Trend

The monthly revenue chart shows how revenue changes over time.

It helps identify:

Revenue peaks
Revenue declines
Seasonal patterns
Changes in demand

This can support revenue planning and forecasting.

Customer Gender Distribution

The gender distribution chart provides an overview of the customer base.

The displayed dashboard shows approximately:

Female – 50.8%
Male – 44.7%
Other – Remaining percentage

This can support customer segmentation and targeted marketing.

⏱️ Dashboard 2 – Operations and Capacity
Purpose

The second dashboard focuses on operational efficiency and capacity utilisation.

It analyses:

Average delay
Occupancy
Peak-hour trips
Weather
City-level delays
Bus-type utilisation
KPI Cards

The dashboard displays:

Average Delay
Occupancy Rate
Number of Cities
Number of Age Groups
Number of Weather Categories
Number of Bus Types

The displayed dashboard shows approximately:

Average Delay: 61 minutes

Occupancy Rate: 58%

Customer Age Distribution

The treemap displays the distribution of customers across different ages.

This provides a visual understanding of the demographic structure of the customer base.

Peak Hour Trip Distribution

The dashboard compares peak and non-peak trips.

The displayed distribution is approximately:

Non-Peak – 60.1%
Peak – 39.9%

This provides an understanding of customer travel behaviour throughout the day.

Average Delay by City

The dashboard compares average delay across cities.

The displayed analysis shows Delhi NCR with the highest average delay.

This indicates that Delhi NCR may require additional operational attention.

Potential improvement areas include:

Better scheduling
Traffic-aware planning
Route optimisation
Peak-hour management
Operational buffers
Average Delay by Weather

The dashboard compares average delays under different weather conditions:

Heavy Rain
Fog
Haze
Rain
Clear
Cloudy

The analysis indicates that adverse weather conditions can be associated with higher delays, particularly heavy rain.

This suggests that weather conditions should be considered in operational planning.

Average Occupancy by Bus Type

The dashboard compares occupancy across:

AC Sleeper
Non-AC Seater
AC Seater
Premium AC

This helps identify how efficiently different bus types are being utilised.

The information can support better fleet allocation.

📉 Dashboard 3 – Delay, Rating and Route Performance
Purpose

The third dashboard connects operational performance with customer satisfaction and route economics.

It focuses on:

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
Customer Rating
Occupancy Rate
Total Revenue
Route Count

These KPIs provide a summary of overall service and route performance.

Delay and Customer Rating Over Time

The time-series chart compares delay and customer rating over time.

This helps investigate whether periods of increased delays are associated with changes in customer satisfaction.

A possible relationship can be represented as:

Higher Delay
     ↓
Poorer Service Experience
     ↓
Potentially Lower Customer Rating

This relationship can be further investigated using statistical analysis.

Distance vs Net Revenue

The scatter plot compares:

Distance (KM)
      ↕
Net Revenue (INR)

The displayed analysis indicates a positive relationship between distance and net revenue.

This suggests that longer routes generally generate higher revenue.

This information can support:

Fare planning
Route economics
Revenue forecasting
Route expansion decisions
Occupancy by Route

The route-level chart compares occupancy across different routes.

It helps identify:

High-demand routes
Low-demand routes
Capacity imbalance
Routes requiring additional frequency

This can support fleet allocation and route planning.

👥 Dashboard 4 – Customer and Booking Behaviour
Purpose

The fourth dashboard focuses on customer behaviour, booking patterns, payments, subscriptions, complaints, and customer satisfaction.

It answers:

Who are the customers, how do they use the service, and which channels contribute most to revenue?

Customer Rating Distribution

The rating chart shows the distribution of customer ratings from 1 to 5.

The displayed dashboard shows a higher concentration of ratings at 4 and 5.

This indicates generally positive customer feedback.

Lower-rated trips can be investigated to understand the reasons for customer dissatisfaction.

Customer Age Group Distribution

Customers are grouped into:

18–25
26–35
36–45
46–60

The displayed dashboard shows the 26–35 age group as the largest customer segment.

This information can support:

Customer segmentation
Marketing campaigns
Subscription planning
Loyalty programmes
Customers by Subscription Type

The dashboard compares:

Corporate Plan
Monthly Pass
Single Ride
Weekly Pass

This helps identify recurring customers and occasional users.

The analysis can support:

Customer retention
Subscription conversion
Loyalty programmes
Targeted offers
Payment Mode Distribution

The dashboard compares:

UPI
Wallet
Debit Card
Cash
Net Banking
Credit Card

The displayed dashboard shows strong usage of UPI and Wallet.

This highlights the importance of providing a smooth and reliable digital payment experience.

Complaint Status Distribution

The dashboard compares trips:

With complaints
Without complaints

Complaint data can be analysed together with:

Delay
City
Route
Bus type
Weather
Customer rating

This can help identify potential causes of customer dissatisfaction.

Revenue by Booking Channel

The dashboard compares revenue generated through:

Website
Corporate Portal
Mobile App
Kiosk

The displayed dashboard shows the Website as the dominant booking channel.

This indicates that website performance is an important part of the customer booking journey.

💡 Key Business Insights
1. City Performance

Mumbai and Pune are among the strongest revenue-generating cities in the displayed dashboard.

These markets represent important contributors to overall business performance.

2. Distance and Revenue

The Distance vs Net Revenue analysis indicates a positive relationship between route distance and revenue.

Longer routes generally tend to generate higher revenue.

3. Weather and Delays

Adverse weather conditions, particularly heavy rain, are associated with higher average delays.

Weather-aware operational planning could therefore improve service reliability.

4. Delhi NCR Delay Performance

Delhi NCR shows the highest displayed average delay.

This indicates a potential opportunity for targeted operational improvements.

5. Occupancy

The displayed overall occupancy rate is approximately 58%.

This suggests that there may be opportunities to improve fleet utilisation through better demand forecasting and scheduling.

6. Customer Satisfaction

Ratings of 4 and 5 represent a substantial portion of customer feedback.

Maintaining reliable service and reducing delays can help maintain customer satisfaction.

7. Digital Payment Behaviour

UPI and Wallet are among the commonly used payment methods.

This highlights the importance of maintaining reliable digital payment infrastructure.

8. Booking Channel Performance

The Website is the dominant booking channel in the displayed revenue analysis.

Improving website usability and booking conversion could therefore support revenue growth.

🚀 Business Recommendations
Operational Efficiency
Focus on high-delay cities and routes.
Introduce weather-aware scheduling.
Add operational buffers during adverse weather.
Analyse peak-hour congestion.
Monitor route-level delays.
Improve route planning.
Use historical delay patterns for scheduling.
Fleet Optimisation
Monitor occupancy by route.
Increase frequency on high-demand routes.
Optimise under-utilised routes.
Match bus types with customer demand.
Use historical demand for fleet allocation.
Customer Experience
Investigate low-rated trips.
Analyse complaints against delays.
Provide proactive delay notifications.
Monitor customer ratings continuously.
Identify recurring service-quality issues.
Revenue Improvement
Analyse revenue per kilometre.
Compare city-level revenue.
Analyse fare by bus type.
Optimise pricing by route.
Promote recurring subscription plans.
Identify high-value customer segments.
Digital Strategy
Improve website booking experience.
Maintain reliable UPI and wallet payments.
Analyse booking-channel performance.
Encourage repeat bookings.
Promote subscription plans.
🛠️ Technologies Used
Technology	Purpose
Python	Data analysis and processing
Pandas	Data cleaning and manipulation
NumPy	Numerical computation
Matplotlib	Data visualisation
Seaborn	Statistical visualisation
SciPy	Statistical analysis
Jupyter Notebook	Data analysis and documentation
Power BI	Interactive dashboard development
Google Sheets	Dataset management
Kaggle	Notebook hosting
GitHub	Version control and project hosting
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
📓 Notebook Description
Cityflo_Data_Inspect.ipynb

This notebook focuses on understanding the raw dataset.

It includes:

Dataset shape
Data types
Missing-value analysis
Duplicate detection
Unique-value analysis
Initial data understanding
Cityflo_Data_Clean_&_Prepare_.ipynb

This notebook focuses on cleaning and preparing the dataset.

It includes:

Missing-value handling
Duplicate removal
Data-type conversion
Category standardisation
Data transformation
Feature preparation
Cityflo_Data_Analyze.ipynb

This notebook contains the main analytical work.

It includes:

Exploratory Data Analysis
Data visualisation
Statistical summaries
Correlation analysis
Statistical testing
Business analysis
Cityflo_Data_Report.ipynb

This notebook presents the final analytical findings.

It includes:

Important KPIs
Major findings
Business insights
Recommendations
Final analysis
▶️ How to Run the Project
Step 1 – Clone the Repository
git clone https://github.com/Anwesapanja/Cityflow-Bus-Service-Metro-Cities.git
Step 2 – Navigate to the Project
cd Cityflow-Bus-Service-Metro-Cities
Step 3 – Install Required Libraries
pip install pandas numpy matplotlib seaborn scipy jupyter
Step 4 – Start Jupyter Notebook
jupyter notebook
Step 5 – Run the Notebooks

Run the notebooks in the following order:

1. Cityflo_Data_Inspect.ipynb
2. Cityflo_Data_Clean_&_Prepare_.ipynb
3. Cityflo_Data_Analyze.ipynb
4. Cityflo_Data_Report.ipynb
🔗 Project Resources
GitHub Repository

https://github.com/Anwesapanja/Cityflow-Bus-Service-Metro-Cities

Kaggle Notebook

https://www.kaggle.com/code/anwesapanja/cityflo-data-analysis

Google Sheets Dataset

https://docs.google.com/spreadsheets/d/1lvvWRxPfKCT4T3xvIqXpyCBdnCnL86It0-TIU80xqVE/edit?gid=1723667175#gid=1723667175

🔮 Future Scope

The project can be further enhanced using advanced analytics and machine learning.

Possible future improvements include:

Demand forecasting
Revenue forecasting
Machine-learning-based delay prediction
Customer segmentation
Customer churn prediction
Customer lifetime value analysis
Route optimisation
Dynamic fleet allocation
Geographic route analysis
Dynamic pricing
Weather-based demand forecasting
Real-time operational monitoring
Customer satisfaction prediction
Demand-based scheduling
⚠️ Limitations

The project has the following limitations:

The dataset is synthetic.
The results should not be interpreted as actual CityFlo business performance.
Correlation does not imply causation.
Dashboard values change depending on the selected filters.
Statistical conclusions are specific to the available dataset.
Geographic analysis is limited by the available location information.
Business recommendations are based on patterns observed within the dataset.
Real-world operational decisions would require additional information such as traffic conditions, fuel costs, fleet availability, real-time weather, and operational costs.
🏁 Conclusion

The CityFlo Bus Service – Metro Cities Data Analysis project demonstrates a complete end-to-end Data Analytics and Business Intelligence workflow.

The project transforms raw transportation data into meaningful business insights through:

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
Power BI Dashboard
      ↓
Business Insights
      ↓
Business Recommendations

The Power BI dashboard provides a comprehensive view of:

🚌 Trip performance
💰 Revenue
🏙️ City performance
⏱️ Delays
🌦️ Weather impact
🪑 Occupancy
🛣️ Route performance
⭐ Customer ratings
👥 Customer demographics
🎫 Subscription behaviour
💳 Payment methods
📢 Customer complaints
📱 Booking channels

The project demonstrates how raw transportation data can be transformed into actionable business intelligence to support better operational planning, fleet utilisation, revenue management, customer experience, and strategic decision-making.

👤 Author
Anwesa Panja

Data Analytics | Python | SQL | Power BI | Data Visualisation

⭐ Project

If you find this project useful, please consider giving the repository a ⭐ on GitHub.
