# 🌃 BREATHE NEW YORK 🗽

<a href="https://prezi.com/view/Ac5QNch5vqhrez6dAeco/?referral_token=8frXDelnB3FN" style="color:#5CE1E6;" target="_blank">Breathe NYC Presentation</a>

---

## Goal: 
Our main objective was to identify the most polluted areas in Greater New York by analyzing four different datasets:

1. **OpenAQ dataset**: extracted real-time measurements of fluctuating levels of multiple air pollutants and toxins detected by a network of sensors distributed across the city.  
2. **Green areas and tree distribution**: incorporated total tree counts per borough to assess how green and breathable each borough is.  
3. **Noise complaints**: used total noise complaint counts to approximate which areas are most affected by noise disturbances.  
4. **Traffic volume**: computed the average traffic volume over the past five years using a MultiIndex Series.


## Business Idea:  
Business Idea: Assess whether homes are reasonably priced based on air quality and public health conditions, and identify overlooked investment opportunities across different boroughs based on current environmental conditions

---


## Process:

### 🌎 Extract real-time data from OpenAQ through their API
1. Identified relevant pollutants and toxins based on data availability and the time range covered by the dataset. Using a defined BBOX, selected all sensor stations located within the geographic boundary, resulting in 55 valid monitoring locations;
2. Verified data completeness for each sensor by checking the first and last recorded measurements (2016–2025), ensuring that each location provided sufficiently recent and continuous readings for analysis;

### 🌳 Merge all datasets by borough and analyze correlations
1. Extracted one pollutant (parameter) at a time, focusing on PM2.5, PM10, and PM1, which showed the most consistent data across boroughs. Respectively, they were detected by 48, 19, and 26 sensors across the Greater New York area. Then merged the datasets created from these extractions and mapped all sensor locations to their corresponding borough;
2. Calculated the average annual pollutant concentration for each borough, along with traffic volume, trees distribution and noise complaint counts;
3. Created a health score for each borough by first normalizing all environmental metrics (pollution, noise, traffic, tree count) using scikit-learn’s `MinMaxScaler`, and then combining the normalized values into a single composite index.


## 💡 Insights and Potential Initiatives  

- **Observation:** Investing in sustainability initiatives in the Bronx appears promising, as it could help reverse the borough’s current economic situation.  
- **Practical Applications:**  
  - Study historical price trends and environmental evolution, and build a predictive model that estimates future property prices considering environmental factors
  - Analyze the correlations between social dynamics and environmental conditions, creating a zoom-in map with a health score specific to neighbourhoods

---
