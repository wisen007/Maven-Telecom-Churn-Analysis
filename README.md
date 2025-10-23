# 📊 Maven Telecom Customer Churn Analysis

This Power BI project explores customer churn patterns at **Maven Telecom**, identifying key drivers behind customer attrition and recommending data-driven strategies to improve retention and customer satisfaction.

---

## 🔍 Project Overview
- **Objective:** Analyze customer behavior to uncover why customers leave Maven Telecom and provide actionable insights for reducing churn.  
- **Dataset Size:** 7,043 customer records from three tables — `customers`, `offers`, and `events`.  
- **Tools Used:** Microsoft Power BI, DAX, Excel.  
- **Skills Demonstrated:** Data Cleaning • Data Modeling • DAX Measures • Visualization • Insight Communication  

---

## 💡 Key Insights
- 🔴 **27% (1,869 customers)** churned out of the 7,043 analyzed.  
- 🔴 **12%** of churn was directly linked to poor support service.  
- 🔴 **56%** of churn occurred within the first year, with **49% leaving within the first two months.**  
- 🔴 **85%** of churned users were on month-to-month contracts, and **71%** of them used bank transfers.  
- 🔴 **56%** of all customers were never offered promotional deals.  
- 🔴 **45%** left due to better offers and services from competitors.  
- 🔴 **19%** of long-term customers (3+ years) also churned.  

---

## 🧠 Recommendations
- 🟢 **Improve Customer Support:** Train or replace staff where needed to reduce churn from poor service.  
- 🟢 **Incentivize New Users:** Offer welcome discounts to reduce early-stage churn (~56%).  
- 🟢 **Revamp Month-to-Month Plans:** Add value or perks to make short-term contracts more appealing.  
- 🟢 **Reward Loyalty:** Recognize long-term customers through special promotions or discounts.  
- 🟢 **Stay Competitive:** Continuously monitor competitor pricing, devices, and service quality.  
- 🟢 **Enhance Reliability:** Strengthen network performance and review long-distance charge policies.  

---

## 📈 Dashboard Preview
Add your dashboard screenshots in this section:  

| Overall Churn Dashboard | Customer Segmentation |
|--------------------------|-----------------------|
| ![Churn Overview](images/dashboard_overview.png) | ![Customer Segments](images/churn_insights.png) |

*(Replace with your exported Power BI visuals in `.png` format)*  

---

## 🔗 Live Power BI Report
If published to Power BI Service, include the link below:

👉 [**View Interactive Dashboard**](http://bit.ly/4nnQYL0)

---

## 🧮 Data Model Overview
The data model combines three main tables:  

- **Customers Table:** Demographics, tenure, contract type, and payment method.  
- **Offers Table:** Promotional deals, devices, and service plans offered.  
- **Events Table:** Churn records, customer activity, and retention events.  

Key DAX measures included:
```DAX
Total Customers = DISTINCTCOUNT(Customers[Customer_ID])
Churn Rate (%) = DIVIDE([Churned Customers], [Total Customers])
New Customers = CALCULATE([Total Customers], FILTER(Customers, Customers[Status] = "New"))
