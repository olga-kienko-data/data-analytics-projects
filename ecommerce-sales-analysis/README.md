#  E-commerce Sales Analysis

##  Project Overview
This project analyzes e-commerce sales data using three datasets: `events`, `countries`, and `products`.

The goal is to clean, transform, and analyze the data to generate business insights related to revenue, cost, and profitability across different dimensions such as product categories, regions, and sales channels.

---

##  Data Preparation
- Merged datasets using:
  - Country Code ↔ alpha-3
  - Product ID ↔ id
- Applied LEFT JOIN to preserve all sales records
- Created final dataset: `sales_data`
- Removed technical columns and kept business-relevant fields

---

##  Data Cleaning
- Handled missing values:
  - Antarctica → "No region"
  - Namibia → fixed ISO code
  - 82 missing country codes → kept as "Unknown"
- Removed rows with missing Units Sold
- Standardized text fields
- Converted dates to datetime format
- Validated delivery time (no negative values)

---

##  Key Metrics
- Revenue
- Cost
- Profit
- Margin
- Delivery Days

---

##  Analysis

### Product Performance
- Top profit drivers: **Cosmetics, Office Supplies, Household**
- High volume but low profit: **Beverages, Fruits**

 Insight: High sales volume ≠ high profitability

---

### Regional Analysis
- Europe generates the majority of profit
- Other regions contribute less

 Insight: Market popularity ≠ efficiency

---

### Sales Channels
- Offline:
  - Higher profit per order
- Online:
  - Higher volume

 Strategy:
- Online → scale
- Offline → profitability

---

### Logistics Analysis
- Delivery time varies by category and country
- No strong correlation with profit

---

### Time Analysis
- High volatility in profit over time
- Weekly pattern observed:
  - Friday → highest average profit
  - Weekend → highest number of orders

---

##  Conclusion
Sales performance depends on a combination of factors:
- product category
- geography
- sales channel
- logistics

No single factor determines profitability.

---

##  Recommendations
- Focus on high-margin categories
- Optimize low-profit high-volume products
- Improve logistics consistency
- Reduce "Unknown" geographic data

---

## Tech Stack
- Python (pandas, matplotlib, seaborn)
- SQL
- Excel
