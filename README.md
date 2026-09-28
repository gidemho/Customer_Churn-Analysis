# Customer Churn Analysis

## 📊 Interactive Power BI Dashboard

An interactive customer churn analysis project developed using **Microsoft Power BI** to identify customer retention patterns and examine the factors associated with customer churn.

The dashboard provides an overview of customer churn across contract types, payment methods, internet services, tenure, and monthly charges.


## 🎯 Project Objective

The objective of this project is to analyze customer churn patterns and provide business insights that can support customer retention strategies.

The analysis focuses on:

- Customer churn rate
- Churned customer volume
- Contract type
- Payment method
- Internet service
- Customer tenure
- Monthly charge groups

## ⭐ Project Highlights

- Built an interactive customer churn dashboard using Power BI.
- Analyzed churn across contract types, payment methods, internet services, tenure, and monthly charges.
- Created DAX measures for customer count, churned customers, average monthly charges, and churn rate.
- Developed customer segmentation groups for tenure and monthly charges.
- Used interactive slicers to support customer-level and segment-level analysis.
- Translated analytical findings into actionable customer retention recommendations.

## 🛠️ Tools Used

Microsoft Power BI – Data visualization and dashboard development

Power Query – Data transformation and preparation

DAX – Measures and KPI calculations

GitHub – Project documentation and portfolio hosting

## 🔄 Data Preparation & Methodology

The customer churn dataset was prepared and analyzed using Microsoft Power BI.

## Data Preparation
- Imported the Telco Customer Churn dataset into Power BI.
- Reviewed the dataset for missing and inconsistent values.
- Converted relevant fields to appropriate data types.
- Prepared customer and service-related variables for analysis.
- Created customer segments based on tenure and monthly charges.
- Created a monthly charge grouping in Power BI using DAX to classify customers into five charge ranges: Below $30, $30–$49, $50–$69, $70–$89, and $90+.


## Analysis Process
1. Data Cleaning – Reviewed and prepared the raw customer data.
2. Data Transformation – Organized variables and created analysis-ready fields using Power Query.
3. DAX Measures – Created measures for key performance indicators including total customers, churned customers, average monthly charges, and churn rate.
4. Data Visualization – Developed KPI cards, charts, and interactive visuals in Power BI.
5. Interactive Analysis – Added slicers to explore churn across customer segments.
6. Business Insights – Examined customer characteristics and service factors associated with churn.

## Key Metrics
- Total Customers: 7,043
- Churned Customers: 1,869
- Churn Rate: 26.54%
- Average Monthly Charges: 64.76

## 📌 Key Performance Indicators

The dashboard provides four major KPIs:

| KPI | Value |
|---|---:|
| Total Customers | 7,043 |
| Average Monthly Charges | 64.76 |
| Churned Customers | 1,869 |
| Churn Rate | 26.54% |

> **Note:** KPI values represent the overall dataset view. Selecting dashboard slicers dynamically changes the results.

## 🧮 DAX Measures

The dashboard uses DAX measures to calculate key customer churn metrics dynamically.

### Total Customers

```DAX
Total Customers =
DISTINCTCOUNT(Customer_Churn[customerID])
```

### Average Monthly Charges

```DAX
Average Monthly Charges =
AVERAGE(Customer_Churn[MonthlyCharges])
```

### Churned Customers

```DAX
Churned Customers =
CALCULATE(
    DISTINCTCOUNT(Customer_Churn[customerID]),
    Customer_Churn[Churn] = "YES"
)
```

### Churn Rate

```DAX
Churn Rate =
DIVIDE(
    [Churned Customers],
    [Total Customers],
    0
)
```

## 📈 Dashboard Analysis

The dashboard examines customer churn across:

1. Contract Type
Compares churn patterns across month-to-month, one-year, and two-year contracts.

2. Payment Method
Analyzes customer churn across electronic check, mailed check, bank transfer, and credit card payment methods.

3. Internet Service
Examines churn patterns among customers using DSL, fiber optic, and customers without internet service.

4. Customer Tenure
Shows how customer churn patterns vary across different tenure groups.

5. Monthly Charges
Groups customers according to their monthly charges and compares churn patterns across the groups.

6. Churn Rate by Payment Method
Shows the percentage of customers who churn within each payment method category.

## 💡 Key Insights

The analysis identified several patterns associated with customer churn:

- Contract type: Customers on month-to-month contracts represent a significant portion of churn, indicating that customers without long-term commitments are more likely to leave.

- Payment method: Churn varies across payment methods, with electronic check customers showing a relatively high level of churn.

- Internet service: Customers using fiber optic internet account for a substantial share of churn, making this an important customer segment to monitor.

- Customer tenure: Churn is more concentrated among customers with shorter tenure, suggesting that the early customer lifecycle is an important period for retention efforts.

- Monthly charges: Customers with higher monthly charges show greater exposure to churn, indicating that pricing and perceived value may be relevant to retention.

- Overall churn: The dataset contains 1,869 churned customers out of 7,043 customers, representing a churn rate of approximately 26.5%.
Why we're doing this


## 🎛️ Interactive Features

The dashboard includes slicers for:

- Internet Service
- Gender
- Contract Type

These filters dynamically update the dashboard KPIs and visualizations, allowing users to explore specific customer segments.


## 📷 Dashboard Preview

![Customer Churn Dashboard](dashboard/customer-churn-dashboard.png)

## 🎯 Business Recommendations

Based on the churn patterns identified in the analysis, the following actions could support customer retention:

- Strengthen early-stage retention: Develop onboarding and engagement initiatives for newer customers, where churn is more concentrated.

- Encourage longer-term contracts: Offer incentives or additional value to customers who move from month-to-month contracts to longer-term plans.

- Review high-churn payment segments: Investigate customer experience and payment friction among customers using payment methods associated with higher churn.

- Monitor high-charge customers: Review pricing, service bundles, and perceived value for customers with higher monthly charges.

- Improve retention for high-risk service segments: Use targeted offers and service-quality initiatives for customer groups with elevated churn.

- Use customer segmentation: Apply the dashboard's interactive filters to identify high-risk customer groups and support targeted retention campaigns.

## 💼 Business Value

Customer churn can affect recurring revenue and customer lifetime value.

This analysis can help businesses:

- Identify customer segments with higher churn exposure
- Understand relationships between customer characteristics and churn
- Develop targeted customer retention strategies
- Investigate payment and service-related churn patterns
- Support data-driven customer relationship decisions

## 🚀 Future Improvements

Potential extensions of this project include:

- Building a customer churn prediction model using Python
- Applying machine learning classification techniques
- Developing customer lifetime value analysis
- Creating automated reporting
- Adding more customer segmentation analysis

## 👤 Author

gidemho

Economics Graduate | Data Analyst | Finance & Business Analytics

## 📂 Project Status

Completed Power BI dashboard and exploratory customer churn analysis.
