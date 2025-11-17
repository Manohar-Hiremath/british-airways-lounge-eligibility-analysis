# British Airways Lounge Eligibility Analysis

## Overview
This project focuses on predicting lounge eligibility for British Airways passengers at Heathrow Terminal 3. Using flight schedule data, the goal is to estimate how many travelers qualify for Tier 1, Tier 2, and Tier 3 lounges based on factors such as time of day, haul type, and arrival region. This helps support BA’s future lounge capacity planning and operational decisions.

## Project Structure
- lounge_analysis.ipynb – Main notebook with full analysis
- BA_Lounge_Eligibility_Lookup.xlsx – Final lookup table output
- BA_Visualization/ – Folder containing bar chart visualization
- Dataset.xlsx – Input dataset
- README.md – Project documentation

## Project Steps

### 1. Data Loading
The flight schedule dataset is loaded using Pandas. Initial checks are performed to understand the dataset size, column information, and missing values.

### 2. Data Exploration
Key fields such as time of day, haul type, region, seat counts, and lounge-eligible passenger counts are reviewed to understand the overall structure and patterns in the data.

### 3. Grouping and Aggregation
Flights are grouped by:
- TIME_OF_DAY  
- HAUL  
- ARRIVAL_REGION  

For each group, the average number of eligible passengers is calculated for:
- Tier 1 Lounge
- Tier 2 Lounge
- Tier 3 Lounge

### 4. Lookup Table Creation
Eligibility percentages are calculated by dividing average eligible passengers by the total number of passengers in each flight group. These percentages are rounded and exported to an Excel file for easy reuse.

### 5. Visualization
A bar chart is created to compare eligible passenger counts across lounge tiers. This visualization helps show which lounges face the highest expected demand. The chart is saved in the BA_Visualization folder.

## Tools Used
- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Jupyter Lab

## Key Insights
- Long-haul flights tend to have higher premium lounge eligibility.
- Tier 3 (Club Lounge) consistently has the highest number of eligible passengers.
- Eligibility trends vary depending on time of day and destination region.
- The lookup table makes it possible to forecast lounge demand even without exact future flight schedules.

## Final Deliverables
- Reusable lounge eligibility lookup table (Excel)
- Cleaned and grouped data
- Visualization for lounge tier comparison
- Complete documentation in this README

## Author
Manohar Hiremath  
MSc Data Science  
Coventry University, UK
