# Hospitality-Revenue-insights

+ The hospitality industry thrives on delivering exceptional guest experiences and optimizing operational efficiency. In this context, leveraging data analytics has become imperative to drive data-informed decision-making and gain a competitive edge.
  
+ This project focuses on revolutionizing hospitality management by harnessing the power of data analytics to unlock valuable insights into various facets of the industry.

+ By employing advanced analytics techniques and data visualization tools, we aim to provide a comprehensive overview of key performance indicators, guest preferences, and operational metrics. These insights will enable stakeholders to make informed decisions and drive business success.
  
+ Through the integration and analysis of diverse data sources, such as bookings, guest feedback, and market trends, we offer a holistic understanding of guest behavior, demand patterns, and market dynamics. This helps identify opportunities for revenue growth, personalize guest experiences, and make informed pricing and marketing strategies

+ By developing intuitive and user-friendly dashboards tailored to the hospitality industry, our solution provides real-time visibility into performance metrics, guest sentiment, and operational KPIs. This empowers hoteliers to monitor and track progress, identify areas for improvement, and take proactive measures to deliver exceptional guest experiences

+ By developing an intuitive and user-friendly sales dashboard, we aim to enhance sales visibility, facilitate performance tracking, and enable proactive decision-making for sales teams.

+ This project will empower hospitality organizations to stay ahead of the competition, optimize revenue, and elevate guest satisfaction by harnessing the power of data analytics and actionable insights.
+ Mockup dashboard provided by the client
  ![image](Images/Data_Modelling.PNG)
## Project Flow Steps 

* <p><a href="#link1">Business Requirement Document & Data Gathering</a></p>
* <p><a href="#link2">Problem Statement</a></p>
* <p><a href="#link3">Main Goal</a></p>
* <p><a href="#link4">Data Cleaning / Data Transformation</a></p>
* <p><a href="#link5">Data Modeling</a></p>
* <p><a href="#link6">DAX</a></p>
* <p><a href="#link7">UI</a></p>

# <h2 id="link1">Business Requirement Document and Data Gathering</h2>
<br>

we are utilizing Excel files provided by our client, the hotel revenue manager, as our primary data source. These Excel files contain valuable information related to hotel revenue, bookings, and other relevant metrics.

# <h2 id="link2">Problem Statment</h2>
<br>

Atliq Grands owns multiple five-star hotels across India. They have been in the hospitality industry for the past 20 years. Due to strategic moves from other competitors and ineffective decision-making in management, Atliq Grands are losing its market share and revenue in the luxury/business hotels category. As a strategic move, the managing director of Atliq Grands wanted to incorporate “Business and Data Intelligence” in order to regain their market share and revenue. However, they do not have an in-house data analytics team to provide them with these insights.

Their revenue management team had decided to hire a 3rd party service provider to provide them insights from their historical data.
<br>


# <h2 id="link3">Main Goal</h2>
<br>

Our main goal is to develop and implement a robust data analytics solution that empowers stakeholders in the hospitality industry. This solution will provide valuable insights into various aspects of the industry, including revenue management, guest experiences, and operational efficiency. By leveraging data-driven insights, our aim is to enable informed decision-making, optimize revenue, enhance guest satisfaction, and drive operational excellence.
<br>

# <h2 id="link4">Data Cleaning / Data Transformation</h2>

The process of data cleaning and transformation is a __crucial step in preparing data__ for analysis.During the data cleaning process, we identified and filtered out any null values that were present in the dataset. This ensures that the data used for analysis and modeling is complete and reliable.

In the data cleaning and transformation phase, we have implemented a column creation process to categorize the days of the week. This categorization designates Sunday to Thursday as weekdays and Friday and Saturday as the weekend.

By introducing this new column, we enable better analysis and insights based on the distinction between weekdays and weekends. This differentiation can be beneficial for various purposes, such as studying patterns in customer behavior, evaluating revenue trends, and optimizing operational strategies.
<br>
# <h2 id="link5">Data Modeling</h2>
<br>
In the data modeling phase for the hospitality industry, we have implemented the star schema as the foundation for structuring and organizing the data. The star schema is a widely adopted dimensional modeling technique that enables efficient data analysis and reporting.

Our data model revolves around a central fact table that represents the primary focus of our analysis, such as hotel bookings or revenue. This fact table contains key performance indicators (KPIs) and measures specific to the hospitality domain, such as room revenue, occupancy rates, average daily rate (ADR), and guest satisfaction scores.

Encircling the fact table, we have multiple dimension tables that capture different aspects of the hospitality data. These dimension tables include entities such as guests, rooms, dates, hotel locations, and amenities. Each dimension table comprises descriptive attributes that provide contextual information and further insights into the corresponding aspect of the hospitality operations..

![image](Images/Data_Modelling.PNG)


# <h2 id="link6">DAX</h2>

Data Analysis Expressions (DAX) is a programming language that is used throughout Microsoft Power BI for creating calculated columns, measures, and custom tables. It is a collection of functions, operators, and constants that can be used in a formula, or expression, to calculate and return one or more values.

__Some Important Measure__

* Revenue : 
```
Revenue = sum('fact_bookings'[revenue_realized])
```

* ADR-(Average Daily Rate) :

```
ADR = DIVIDE( [Revenue], [Total Bookings],0
```
* RevPAR - Revenue per available room :

```
RevPAR = DIVIDE([Revenue],'Base Measure'[Toatal capacity])
```

* DSRN -(Daily sellable room nights) :

```
DSRN = DIVIDE([Toatal capacity],[No of days])
```

* DBRN - Daily Booked Room Nights :
```
DBRN =DIVIDE([Total Bookings], [No of days]) 
```
* DURN - Daily Utilized Room Nights:
```
DURN = DIVIDE([Total Checked Out],[No of days])  
```
<br>

# <h2 id="link7">UI/UX Design</h2>
<br>
The sales dashboard can offer a visually appealing and user-friendly experience. It will enable stakeholders to easily navigate through sales data visualizations, interact with filters and controls, and access relevant insights effortlessly. The UI/UX design ensures that the dashboard becomes an intuitive and valuable tool for decision-making, enhancing the overall effectiveness of the sales analytics solution.



![image](Images/Hardware_sales_insights.PNG)
<br>

## Some Important insights from the Dashboard

- Mumbai generates the highest revenue (669 M) followed by Bangalore, Hyderabad and Delhi
- AtliQ Exotica performs better compared to all 7 type of properties with 320 Million revenue, rating 3.62, occupancy percentage 57 and cancellation rate as 24.4%.
- AtliQ Blu has the highest occupancy of 62%
- Week 24 recorded the highest revenue among all, which is 139.6 Million
- Delhi tops both in occupancy and rating followed by Hyderabad, Mumbai, Bangalore
- Elite type rooms has the most booking and as well higher cancellation rate
