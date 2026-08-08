CityFlo Bus Service -- Metro Cities Data Analysis & Business Intelligence

📌 Project Overview

This project presents an end-to-end data analytics and businessintelligence solution for a CityFlo-style intercity/metro-city busservice.

The objective is to analyse trip operations, customer behaviour,revenue, delays, occupancy, booking patterns, payment preferences, andservice quality across major Indian cities.

The project covers the complete analytics lifecycle:

Data Inspection → Data Cleaning → Data Preparation → Exploratory DataAnalysis → Statistical Analysis → KPI Development → Dashboard Design →Business Insights

Note: The dataset used in this project is synthetic and isintended for analytics, learning, and portfolio purposes. It does notrepresent actual CityFlo operational data.

🎯 Business Objective

The primary objective is to use historical trip and customer data toanswer important business questions related to revenue, operationalefficiency, customer satisfaction, and capacity utilisation.

Key Business Questions

Which cities generate the highest revenue?

Which cities have the highest average delays?

How does weather affect trip delays?

Does peak-hour operation influence delays?

Which bus types have the highest occupancy?

How does route distance affect revenue?

What is the relationship between delays and customer ratings?

Which payment modes are most commonly used?

Which subscription types have the largest customer base?

How frequently are complaints raised?

How do customers differ across age groups and genders?

Which booking channels contribute to revenue?

How are trip statuses distributed across the service?

📊 Dataset

The project analyses a CityFlo-style bus-service dataset containingtrip-level, customer-level, operational, and financial information.

Major Data Categories

Category                            Important Variables

Trip Information                    trip_id, route_id, trip_date,trip_status

Customer Information                customer_id, age, gender,rating

Operations                          bus_type, distance_km,delay_minutes, occupancy_pct

Financial                           fare_inr, discount_inr,net_revenue_inr

Booking                             booking_mode, payment_mode,subscription_type

Conditions                          weather, is_peak_hour

Customer Service                    complaint_raised

Cities Analysed

Mumbai

Pune

Bangalore

Chennai

Hyderabad

Delhi NCR

Other metro-city records where applicable in the source data

🗂️ Project Structure

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

🔄 Data Analytics Workflow

1. Data Inspection

The raw dataset was first inspected to understand:

Number of rows and columns

Data types

Missing values

Duplicate records

Unique categories

Invalid values

Outliers

Date formats

Boolean inconsistencies

Numerical distributions

This step helped identify potential data-quality problems beforeanalysis.

2. Data Cleaning & Preparation

The cleaning process included:

Removing duplicate records

Standardising categorical values

Removing unnecessary whitespace

Converting columns to appropriate data types

Parsing dates

Handling missing values

Standardising Boolean fields

Validating customer ages

Checking occupancy percentages

Handling extreme fare values

Validating trip IDs

Performing cross-column consistency checks

3. Feature Engineering

Additional analytical variables were created, including:

Age groups

Month

Weekday

Peak-hour indicators

Delay indicators

Net revenue

Aggregated city-level KPIs

Route-level KPIs

Net Revenue

Net Revenue = Fare - Discount

Delayed Trip

A trip is treated as delayed when:

Delay Minutes > 5

Age Groups

Customers are grouped into meaningful age categories to make demographicanalysis easier.

📈 Exploratory Data Analysis

The analysis uses:

Bar charts

Histograms

Box plots

Pie charts

Donut charts

Line charts

Scatter plots

Correlation heatmaps

Grouped comparisons

Statistical tests

The analysis focuses on four major areas:

1. Operational Performance

Delay analysis

Trip status

Peak-hour behaviour

Weather impact

Route performance

Occupancy

2. Financial Performance

Revenue by city

Revenue over time

Distance vs. revenue

Fare analysis

Revenue by booking channel

3. Customer Behaviour

Age

Gender

Ratings

Subscription type

Payment mode

Complaints

4. Service Quality

Delays

Ratings

Complaints

No-shows

Cancellations

📊 Interactive Dashboard

The project contains a four-page interactive Power BI dashboard.

The dashboard is designed to convert the analytical results into aneasy-to-understand business intelligence interface.

A consistent dashboard design is used across all pages:

Dark CityFlo-style navigation panel

KPI cards

Interactive filters

Charts and tables

City and route comparisons

Time-series analysis

Customer segmentation

Operational performance analysis

The main dashboard filters are:

Gender

Bus Type

Payment Mode

Days

City

Weather

Age Group

Booking Mode

These filters allow users to analyse the KPIs dynamically for a selectedcustomer segment, city, bus type, weather condition, or bookingbehaviour.

🖥️ Dashboard 1 -- City & Revenue Overview



Purpose

The first dashboard page provides a high-level executive overview ofthe bus service.

It answers:

How is the overall business performing across cities, revenue, tripstatus, time, and customer demographics?

KPI Cards

The top section provides the major business metrics:

Trip ID / Total Trips

Shows the total number of trip records available in the dashboard.

Customer ID

Shows the number of customers represented in the analysis.

Age

Provides the customer-age KPI used for demographic context.

Route ID

Shows the number of routes represented in the dataset.

Trip Date

Provides the number of trip-date records/coverage represented in thedashboard.

Total Net Revenue

Shows the total revenue generated after discounts.

This is one of the most important financial KPIs in the dashboard.

Trips by City

The Trips by City bar chart compares the number of trips acrossmajor cities.

It helps identify:

Which cities have the highest trip volume

Which markets have relatively lower demand

Where operational capacity is concentrated

In the displayed dashboard, Mumbai and Pune have among the highest tripvolumes.

Business Use

Management can use this chart to determine where:

More buses may be required

Demand is strongest

Route expansion could be considered

Operational resources should be concentrated

Revenue by City

The revenue table ranks cities according to net revenue.

The displayed dashboard shows:

Mumbai

Pune

Bangalore

Chennai

Hyderabad

Delhi NCR

Mumbai and Pune are the strongest revenue-generating cities in thedisplayed view.

Business Use

This allows management to compare market contribution and identifyhigh-value cities.

Revenue can then be compared with trip volume and occupancy to determinewhether a city is profitable because of:

High demand

Higher fares

Longer routes

Better occupancy

Or a combination of these factors

Trip Status Distribution

The pie chart shows the proportion of:

Completed

Delayed-Completed

Cancelled

No-show

In the displayed dashboard:

Completed: approximately 66%

Delayed-Completed: approximately 12%

Cancelled: approximately 11.7%

No-show: approximately 10.4%

Business Interpretation

Although completed trips represent the majority, a meaningful proportionof trips are affected by delays, cancellations, or no-shows.

This is important because these outcomes can affect:

Customer satisfaction

Revenue

Fleet utilisation

Operational efficiency

Monthly Revenue Trend

The line chart shows how revenue changes throughout the year.

It helps identify:

High-revenue months

Low-revenue months

Seasonal patterns

Revenue volatility

The displayed trend shows revenue fluctuating across the year, withseveral peaks and declines.

Business Use

This can support:

Demand forecasting

Promotional planning

Fleet allocation

Seasonal pricing strategies

Customer Gender Distribution

The donut chart displays the gender composition of customers.

The dashboard shows approximately:

Female: 50.8%

Male: 44.7%

Other: remaining share

Business Use

This provides a demographic overview that can support customersegmentation and targeted service strategies.

🖥️ Dashboard 2 -- Operations, Delay & Capacity



Purpose

The second dashboard focuses on operational performance and capacityutilisation.

It answers:

Where are delays occurring, what conditions influence them, and howefficiently are buses being utilised?

KPI Cards

The page highlights:

Average Delay

Occupancy Rate

Number of Cities

Number of Age Groups

Number of Weather Categories

Number of Bus Types

The displayed dashboard shows:

Average delay: approximately 61 minutes

Average occupancy: approximately 58%

These KPIs provide an immediate view of operational efficiency.

Customer Age Distribution

The treemap displays customers across different age values/groups.

It helps identify the concentration of customers by age.

Business Use

Understanding age composition can help with:

Customer segmentation

Pricing strategies

Subscription planning

Marketing campaigns

Peak Hour Trip Distribution

The donut chart compares:

Peak-hour trips

Non-peak-hour trips

The displayed view shows approximately:

False / non-peak: 60.1%

True / peak: 39.9%

Business Interpretation

A significant portion of trips occur during peak hours, making peak-hourcapacity and scheduling important operational considerations.

Average Delay by City

The bar chart compares average delay across cities.

In the displayed dashboard:

Delhi NCR has the highest average delay

Hyderabad follows

Chennai, Pune, Bangalore and Mumbai show progressively loweraverages

Business Use

This allows management to identify cities requiring operationalimprovement.

Potential actions include:

Schedule optimisation

Route redesign

Better fleet allocation

Traffic-aware planning

Driver and dispatch optimisation

Average Delay by Weather

The line chart compares average delay under:

Heavy Rain

Fog

Haze

Rain

Clear

Cloudy

The displayed chart shows higher delays during adverse weather,particularly heavy rain, with delays generally decreasing toward clearerconditions.

Business Interpretation

Weather can be an operational risk factor.

This suggests that the service could benefit from:

Weather-based scheduling

Buffer times

Proactive customer notifications

Dynamic fleet planning

Average Occupancy by Bus Type

The horizontal bar chart compares occupancy for:

AC Sleeper

Non-AC Seater

AC Seater

Premium AC

The displayed occupancy values are relatively close, with AC Sleepershowing the highest occupancy among the displayed categories.

Business Use

This helps determine:

Which bus types are most efficiently utilised

Where capacity can be increased

Which bus types may require schedule optimisation

🖥️ Dashboard 3 -- Delay, Rating & Route Performance



Purpose

The third dashboard connects operational performance with customersatisfaction and route economics.

It answers:

How do delays, ratings, route distance, revenue, and occupancyinteract?

KPI Cards

The page displays:

Total Trips

Average Delay

Customer Rating

Occupancy Rate

Total Revenue

Number of Routes

These provide a combined view of:

Operations + Customer Experience + Finance

Delay & Customer Rating Over Time

This is one of the most important charts in the dashboard.

It compares:

delay_minutes

Customer rating

trip_date

over the course of the year.

The chart allows management to identify:

Periods with unusually high delays

Rating fluctuations

Potential relationships between operational issues and customerexperience

Business Use

If periods of increasing delays coincide with declining ratings,management can investigate whether service reliability is affectingcustomer satisfaction.

Distance vs Net Revenue

The scatter plot compares:

distance_km

net_revenue_inr

The points show a clear positive relationship between distance andrevenue.

Business Interpretation

Longer routes generally generate higher revenue.

This can help the business understand:

Route economics

Fare structure

Revenue potential of longer routes

Potential route expansion opportunities

A regression/trend line is also shown to make the overall relationshipeasier to interpret.

Occupancy by Route

The route-level chart compares occupancy across different routes.

It helps identify:

High-utilisation routes

Low-utilisation routes

Routes with fluctuating demand

Business Use

This analysis can support:

Bus allocation

Route frequency decisions

Schedule changes

Capacity planning

Route optimisation

🖥️ Dashboard 4 -- Customer & Booking Behaviour



Purpose

The fourth dashboard focuses on customer behaviour, paymentpreferences, subscriptions, complaints, and booking channels.

It answers:

Who are the customers, how do they use the service, and throughwhich channels do they generate business?

Customer Rating Distribution

The bar chart shows the number of trips/customers associated with eachrating from 1 to 5.

The dashboard shows that:

Rating 5 has the highest frequency

Rating 4 is the next major category

Lower ratings occur less frequently

Business Interpretation

The overall distribution suggests that customer feedback is generallyconcentrated toward higher ratings.

However, low-rated trips should still be analysed to identify serviceproblems.

Customer Age Group Distribution

The donut chart segments customers into:

18--25

26--35

36--45

46--60

The displayed dashboard shows the largest segment as 26--35,followed by 18--25 and 36--45.

Business Use

This can support targeted:

Marketing

Subscription plans

Pricing

Promotions

Customer retention campaigns

Customers by Subscription Type

The chart compares customer counts across:

Corporate Plan

Monthly Pass

Single Ride

Weekly Pass

Business Interpretation

The displayed dashboard shows the Weekly Pass and other subscriptioncategories contributing substantial customer volume.

Subscription analysis helps identify recurring versus occasional users.

Business Use

The company can use this information to:

Promote long-term subscriptions

Improve customer retention

Identify high-value customer segments

Design targeted offers

Payment Mode Distribution

The horizontal bar chart compares:

UPI

Wallet

Debit Card

Cash

Net Banking

Credit Card

UPI and Wallet are among the most frequently used payment methods in thedisplayed dashboard.

Business Use

This information can help the business:

Prioritise digital payment infrastructure

Optimise checkout experience

Reduce payment friction

Identify preferred customer payment channels

Complaint Status Distribution

The chart compares:

Trips without complaints

Trips with complaints

The displayed dashboard shows that the majority of trips do not havecomplaints, while a smaller proportion have complaints.

Business Interpretation

Although complaints represent a smaller share, they are valuable foridentifying service-quality issues.

Complaint records can be analysed together with:

Delay

City

Route

Bus type

Weather

Rating

to identify root causes.

Revenue by Booking Channel

The funnel chart visualises revenue contribution across booking channelssuch as:

Website

Corporate Portal

Mobile App

Kiosk

The displayed chart shows the Website as the dominant bookingchannel, followed by other channels.

Business Use

This helps management understand:

Which channels generate the most business

Where customers prefer to book

Where digital investment should be prioritised

Which channels may need optimisation

🔍 Dashboard Design Philosophy

The four dashboard pages are intentionally designed to follow a logicalbusiness flow.

Page 1 --- What is happening?

CityFlo Business Overview



Provides the executive summary.

Page 2 --- Why is it happening operationally?

Operations & Performance

Focuses on delays, weather, peak hours, and occupancy.

Page 3 --- How does operations affect customers and routes?

Route & Revenue Analysis

Connects service quality with customer ratings and route economics.

Page 4 --- Who are the customers and how do they use the service?

Customer & Booking Insights

Explores demographics, subscriptions, payment methods, complaints, andbooking channels.

This creates a complete analytical story:

BUSINESS PERFORMANCE
        ↓
OPERATIONAL PERFORMANCE
        ↓
CUSTOMER EXPERIENCE
        ↓
CUSTOMER & BOOKING BEHAVIOUR
        ↓
BUSINESS DECISIONS

🧪 Statistical Analysis

The project also uses statistical testing to validate importantrelationships rather than relying only on visual observations.

Pearson Correlation

Used to examine the relationship between:

distance_km ↔ fare_inr

Independent Samples t-test

Used to compare:

delay_minutes

between:

peak-hour vs non-peak-hour trips

One-way ANOVA

Used to determine whether average fares differ significantly across:

bus_type

Chi-square Test

Used to determine whether:

city ↔ trip_status

are statistically associated.

💡 Key Business Insights

1. Revenue Concentration

Mumbai and Pune are among the strongest revenue-generating cities in thedisplayed dashboard.

This suggests that these markets should receive close attention whenplanning:

Capacity

Route expansion

Marketing

Fleet allocation

2. Distance Drives Revenue

The Distance vs Net Revenue scatter plot demonstrates a strong positiverelationship.

Longer routes generally generate higher net revenue.

3. Weather Can Affect Delays

Average delays are higher under adverse weather conditions, especiallyheavy rain.

Weather-aware operations could therefore improve punctuality.

4. City-Level Delay Differences

Delhi NCR shows the highest average delay among the cities displayed inthe dashboard.

This indicates a potential opportunity for targeted operationalimprovements.

5. Occupancy Is Around the Mid-50% Range

The displayed overall occupancy rate is approximately 58%.

This suggests that there may be opportunities to improve capacityutilisation through:

Better scheduling

Demand forecasting

Route optimisation

Dynamic capacity allocation

6. Customer Ratings Are Concentrated at Higher Levels

Ratings of 4 and 5 account for a substantial share of customer feedback.

Maintaining service reliability is important for protecting thispositive customer experience.

7. Digital Payments Are Highly Relevant

UPI and wallet payments show strong usage.

A seamless digital payment experience is therefore important forcustomer convenience.

8. Booking Channels Matter

The booking-channel analysis shows the website as the dominant channelin the displayed dashboard.

This makes website performance and conversion an important businessconsideration.

📌 Recommended Business Actions

Based on the dashboard analysis, the following actions could beconsidered:

Improve Delay Management

Focus on high-delay cities

Add weather-based operational buffers

Analyse high-delay routes individually

Improve dispatch and scheduling

Improve Capacity Utilisation

Monitor occupancy by route

Increase frequency on high-demand routes

Optimise under-utilised routes

Match bus type with demand

Improve Customer Experience

Investigate low-rated trips

Connect complaints with delay and route information

Provide proactive delay notifications

Track service-quality trends

Improve Revenue

Analyse revenue per kilometre

Compare city-level profitability

Optimise fares by route and bus type

Promote high-value subscription plans

Strengthen Digital Channels

Optimise the website booking experience

Maintain strong UPI/wallet support

Analyse conversion by booking channel

Encourage repeat bookings and subscriptions

🛠️ Technologies Used

Python

Pandas

NumPy

Matplotlib

Seaborn

SciPy

Jupyter Notebook

Power BI

Google Sheets

Kaggle

GitHub

🚀 How to Run the Project

Clone the repository

git clone https://github.com/Anwesapanja/Cityflow-Bus-Service-Metro-Cities.git
cd Cityflow-Bus-Service-Metro-Cities

Install Python dependencies

pip install pandas numpy matplotlib seaborn scipy jupyter

Run notebooks in sequence

1. Cityflo_Data_Inspect.ipynb
2. Cityflo_Data_Clean_&_Prepare_.ipynb
3. Cityflo_Data_Analyze.ipynb
4. Cityflo_Data_Report.ipynb

🔗 Project Resources

GitHub

https://github.com/Anwesapanja/Cityflow-Bus-Service-Metro-Cities

Kaggle

https://www.kaggle.com/code/anwesapanja/cityflo-data-analysis

Google Sheets

https://docs.google.com/spreadsheets/d/1lvvWRxPfKCT4T3xvIqXpyCBdnCnL86It0-TIU80xqVE/edit?gid=1723667175#gid=1723667175

⚠️ Project Limitations

The dataset is synthetic.

Results should not be interpreted as actual CityFlo businessperformance.

Correlation does not imply causation.

Dashboard results depend on the cleaned dataset and applied filters.

Geographic mapping is limited because latitude/longitude informationis not included.

Statistical conclusions apply only to the available dataset.

🏁 Conclusion

This project demonstrates how raw transportation data can be transformedinto meaningful business intelligence.

The analysis combines:

Data Cleaning → Feature Engineering → EDA → Statistical Testing → KPIAnalysis → Dashboard Development → Business Recommendations

The four dashboard pages provide a complete view of:

Revenue

Trips

Cities

Delays

Occupancy

Routes

Customer ratings

Customer demographics

Subscriptions

Payments

Complaints

Booking channels

The final dashboard enables decision-makers to move from "Whathappened?" to "Why did it happen?" and ultimately to "Whatshould we do next?"

👤 Author

Anwesa Panja

Data Analytics | Python | SQL | Power BI | Data Visualisation

⭐ If you find this project useful, consider exploring the notebooksand dashboard to understand the complete data analytics workflow.
