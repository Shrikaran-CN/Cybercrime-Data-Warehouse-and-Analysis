# Cybercrime-Data-Warehouse-and-Analysis

## Overview
This project was developed to design and implement a data warehouse for analyzing cybercrime data. The primary objectives were:
1. Crime Hotspot Identification – Determining areas with a high incidence of crime.
2. Policing Strategy Recommendations – Providing actionable insights for NCCU to develop effective policing strategies.

To achieve these objectives, a data warehouse was built using SQL Server Management Studio (SSMS), ETL pipelines were implemented using SQL Server Integration Services (SSIS), and data analysis & visualization were performed using Power BI.

## Technologies Used
* SQL Server Management Studio (SSMS) – For database design and querying.
* SQL Server Integration Services (SSIS) – For ETL (Extract, Transform, Load) operations.
* Visual Studio – For managing SSIS packages.
* Power BI – For data visualization and analysis.

## Database Design
The database follows a star schema with the following tables:
1. FACT_CRIME – Contains crime statistics, law enforcement expenditures, tax rates, and unemployment data.
2. FACT_CLEARANCE_RATE – Stores crime clearance rate metrics and policing efficiency statistics.
3. DIM_COUNTY – Dimension table categorizing counties based on location (e.g., urban, south, northeast, etc.).
4. DIM_DATE – Dimension table for time-based analysis (years).
![image](https://github.com/user-attachments/assets/e2683945-2217-4ed1-bb22-78dfc9efbed1)

## Data Analysis & Visualization
The analysis was conducted using Power BI, leveraging the data warehouse to generate key insights through interactive dashboards. The visualizations focus on two main aspects:
1. Crime Hotspot Identification
 * Crime Rate by County – A bar chart ranking counties by their average crime rate (crmrte), helping to identify high-crime areas.
 * Crime Rate Trend Over Time – A line chart illustrating the changes in crime rate over the years, highlighting trends in criminal activity.
 * Crime Density & Crime Rate Averages – Key metrics summarizing the overall crime rate and crime density.

![Screenshot 2024-12-03 161426](https://github.com/user-attachments/assets/cb04e97e-e166-47a5-bc52-e8a720713bbb)

2. Policing Strategies Analysis
 * Crime Rate vs. Police Presence – A bar and line combination chart showing the relationship between crime rate (crmrte) and police officers per capita (pol_p1000p) across different counties.
 * Crime Density vs. Police Presence – Another visualization comparing crime density with policing resources to assess their effectiveness.
 * Probabilities of Arrest & Conviction – Key performance indicators (prbarr, prbconv) to evaluate law enforcement efficiency.

![image](https://github.com/user-attachments/assets/f35e598a-b08f-4489-a0b7-368a05a09d0f)
These dashboards help in identifying high-crime areas and assessing the effectiveness of policing efforts, aiding NCCU in optimizing resource allocation and strategy formulation.

## Key Findings
#### 1. Crime Hotspot Identification
 * Certain counties, such as county_id 119, 129, and 63, have the highest crime rates (crmrte), making them potential crime hotspots.
 * Crime rates fluctuated over the years, with a noticeable decline in 1984, followed by a rise towards 1987, indicating possible external factors influencing crime trends.
 * The overall average crime rate is approximately 0.03, suggesting a relatively low but non-negligible rate across all counties.
   
#### 2. Policing Strategies Effectiveness
 * Higher police presence (polpc) does not always correlate with lower crime rates, indicating that other factors might be influencing crime trends.
 * Counties with high crime rates (e.g., 119, 129, and 63) also show higher population density, emphasizing the need for targeted policing efforts in these areas.
 * Probabilities of arrest (prbarr) and conviction (prbconv) vary across counties, affecting overall crime deterrence effectiveness.
 * Some counties with low crime rates still have significant police presence, suggesting potential inefficiencies in resource allocation.
  
### Recommendations for NCCU
* Focus policing efforts on high-crime counties such as 119, 129, and 63, where high population density may contribute to crime trends.
* Investigate the causes of crime fluctuations over the years to identify patterns and external influences.
* Reassess police resource allocation to ensure that high-crime areas receive adequate law enforcement support.
* Enhance arrest and conviction rates in crime-prone areas to strengthen deterrence measures.

## Conclusion
This project successfully demonstrates how a data warehouse can support crime analysis and strategic decision-making. The combination of structured data storage, ETL processes, and visualization provides valuable insights to NCCU for crime prevention and law enforcement improvements.
The integration of the data warehouse and Power BI enabled NCCU to:
1. Centralize data management – The data warehouse consolidated crime statistics, population density, economic indicators, and policing activity into a structured repository, eliminating data silos.
2. Analyze historical trends – By providing access to historical data, the system helped identify patterns in crime rates and assess the effectiveness of past policing strategies.
3. Identify high-risk areas – Hotspot mapping and trend analysis highlighted priority areas for immediate intervention.
4. Develop data-driven strategies – Insights into the factors influencing crime informed actionable policing and community programs.
5. Monitor and adapt policies – Real-time visualization allowed NCCU to assess the impact of policies and adjust them as needed for maximum effectiveness.

## Future Enhancements
* Integration of real-time data sources for more up-to-date crime reporting.
* Advanced machine learning models to predict crime trends based on historical data.
* Geospatial analysis for more precise hotspot mapping.
