# Marketing Campaign Analysis Dashboard

---

### Project Overview

This project presents an analytical dashboard focused on **marketing campaign performance and customer behavior**. The solution was developed using **Microsoft Power BI** and aims to transform raw customer and campaign data into actionable insights to support business decision-making.

The project was developed as part of **Mini-Project I – Chapter 4** of the *Microsoft Power BI for Business Intelligence and Data Science* program at **Data Science Academy (DSA)**.

Unlike traditional business scenarios, the client did not provide predefined business questions. Therefore, the analysis followed an **exploratory and diagnostic approach**, seeking to identify relevant patterns related to customer profile, purchasing behavior, channels, and campaign effectiveness.

---

### Dataset Description

A single dataset in CSV format was provided, containing approximately **2,000 records**, with no null or blank values.

**Main features include:**

* Customer demographics (birth year, education, marital status, country)
* Household composition (children and teenagers at home)
* Annual income
* Spending by product category
* Purchase channels (store, web, catalog)
* Campaign participation and outcomes

---

### Data Preparation

During the data exploration phase, **outliers were identified** in numerical variables. After validation with the business context, these values were classified as **data entry errors** and were removed from the dataset.

To enable a consolidated analysis of customer spending, a new DAX measure was created:

```DAX
Total Spend =
SUMX(
    MarketingData,
    MarketingData[Food Spend]
    + MarketingData[Toy Spend]
    + MarketingData[Electronics Spend]
    + MarketingData[Furniture Spend]
    + MarketingData[Utilities Spend]
    + MarketingData[Clothing Spend]
)
```

Additionally, the categorical field **"Purchased"** was standardized by replacing binary values (0 and 1) with **"No"** and **"Yes"**, improving interpretability.

---

### Dashboard Structure

The dashboard is organized into four analytical views:

1. **Customer Overview** – Demographic profile and purchase channels.

<img width="1231" height="698" alt="Print - Visão Cliente" src="https://github.com/user-attachments/assets/10a2adf5-3e91-4974-86b6-e4e4c451871f" />

2. **Customer Purchase Behavior** – Relationship between income, household composition, and total spending.

<img width="1233" height="687" alt="Print - Visão Comportamento de Compra do Cliente" src="https://github.com/user-attachments/assets/bbdcd93e-2c11-467c-b82f-5f7951eb463e" />

3. **Marketing Campaign Performance** – Campaign effectiveness and customer response analysis.

<img width="1230" height="687" alt="Print - Visão Performance das Campanhas de Marketing" src="https://github.com/user-attachments/assets/16d2c427-b43a-4ee3-ad01-312787debfaa" />

4. **Purchase Patterns by Point of Sale** – Spending distribution by country, category, and time.

<img width="1227" height="687" alt="Print - Visão de Padrões de Compra por Ponto de Venda" src="https://github.com/user-attachments/assets/92ef8fc5-66cb-48d9-ab60-0eb654015c7e" />

---

### Tools and Technologies

* Microsoft Power BI
* DAX
* CSV Dataset

---
### Key Findings and Business Insights

Based on the exploratory analysis and the dashboards developed, the following key insights were identified:

* Customer Profile Concentration
The customer base is predominantly composed of individuals with higher education levels, especially those with undergraduate and postgraduate degrees. This indicates a customer profile with higher purchasing power and greater responsiveness to value-based marketing strategies.

* Marital Status and Purchasing Behavior
Single customers represent the largest share of the customer base and also account for the highest total spending. This suggests that personalized campaigns targeting this segment may generate higher returns.

* Income vs. Spending Relationship
There is a clear positive correlation between annual salary and total spending, although with diminishing marginal returns at higher income levels. This indicates that factors beyond income — such as lifestyle and household composition — play a relevant role in purchasing behavior.

* Household Composition Impact
Customers without children or adolescents at home exhibit significantly higher total spending. As the number of children or adolescents increases, overall spending tends to decrease, suggesting budget constraints or shifts in consumption priorities.

* Geographical and Channel Performance
The United States consistently leads in total spending across product categories and years, followed by Spain and Chile. Physical stores remain the dominant sales channel, while web and catalog channels show potential for growth through targeted digital strategies.

* Marketing Campaign Effectiveness
The majority of customers did not convert during the marketing campaigns. However, customers who did convert present a higher average annual salary, indicating that income level is a strong predictor of campaign success.

* Business Implication:
The analysis suggests that marketing efforts should focus on higher-income, single customers with no children, while also investing in more personalized and segmented campaigns to improve conversion rates across other profiles.

---

## Disclaimer

The datasets used in this project were provided exclusively for educational purposes by Data Science Academy and do not represent real company data.

---

### Author

**Leandro Álax**
Data Analytics | Business Intelligence | Power BI

For professional inquiries or collaboration opportunities,
leandroalax@hotmail.com
