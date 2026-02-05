# 📊 Superstore Sales Analysis Dashboard
Page 1: Sales Performance Overview
<img width="1310" height="743" alt="dashboard_overview" src="https://github.com/user-attachments/assets/fc84d3b1-e455-440c-bf8b-29c2029ee05b" />
---
Page 2: Customer Behavior Analysis
<img width="1310" height="742" alt="dashboard_product" src="https://github.com/user-attachments/assets/03309f3d-f747-41c9-adbc-651f0961f5c9" />
---
Page 3: Product & Regional Insights
<img width="1311" height="737" alt="dashboard_customer" src="https://github.com/user-attachments/assets/36e0b62d-e911-48ac-ab72-145ab61eab02" />

---

## 📌 Project Overview

This project analyzes historical retail sales data to uncover revenue trends, customer behavior, and product performance. The goal is to provide actionable business insights through an interactive Power BI dashboard for decision-making.

---

## 📂 Dataset

- **Source**: Superstore Sales Dataset
- **Period**: 2015 – 2018
- **Records**: 9,900+ sales transactions
- **Geography**: 49 U.S. states

---

## 🛠️ Data Preparation

### Data Cleaning & Transformation
- Cleaned and transformed raw data using **Power Query**
- Handled missing values, standardized fields, and created derived columns

### Data Modeling
Designed a **Star Schema** data model:
- **1 Fact table**: Sales
- **4 Dimension tables**: 
  - Date
  - Product
  - Customer
  - Geography

---

## 📐 Data Modeling & DAX

### DAX Measures Implemented
Built **15+ DAX measures**, including:

```dax
// Core Metrics
Total Sales = SUM(Sales[Sales Amount])

Average Order Value (AOV) = 
DIVIDE([Total Sales], DISTINCTCOUNT(Sales[Order ID]), 0)

// Time Intelligence
MoM Growth = 
VAR CurrentMonth = [Total Sales]
VAR PreviousMonth = CALCULATE([Total Sales], DATEADD(Date[Date], -1, MONTH))
RETURN DIVIDE(CurrentMonth - PreviousMonth, PreviousMonth, 0)

YoY Growth = 
VAR CurrentYear = [Total Sales]
VAR PreviousYear = CALCULATE([Total Sales], SAMEPERIODLASTYEAR(Date[Date]))
RETURN DIVIDE(CurrentYear - PreviousYear, PreviousYear, 0)

QTD Sales = TOTALQTD([Total Sales], Date[Date])
```

### Performance Optimization
- Optimized model for performance and scalability
- Implemented efficient relationships and cardinality
- Used calculated columns strategically

---

## 📊 Dashboard Features

### Interactive Filters
Filter data dynamically by:
- 📦 **Product Category**
- 👥 **Customer Segment**
- 🗺️ **Region & State**

### Advanced Analytics
- ✅ **Drill-through analysis** for detailed insights
- ✅ **Time-series trends** with month/quarter/year views
- ✅ **Dynamic tooltips** for contextual information
- ✅ **3 analytical report pages** focusing on:
  - Sales Performance Overview
  - Customer Behavior Analysis
  - Product & Regional Insights

---

## 🔍 Key Insights

### Revenue Analysis
- **Technology category** generated **38%** of total revenue
- Identified high-margin product opportunities

### Customer Segmentation
- **Consumer segment** contributed **52%** of overall sales
- Sales growth driven primarily by repeat high-value customers

### Seasonal Trends
- Strong seasonal sales peaks observed in **November–December**
- Strategic planning opportunities for inventory management

### Growth Patterns
- Month-over-Month (MoM) and Year-over-Year (YoY) growth tracked
- Quarter-to-Date (QTD) performance monitored for real-time insights

---

## 💼 Business Value

This dashboard delivers measurable business impact:

1. **Strategic Decision-Making**
   - Helps stakeholders identify high-performing products and customer segments
   
2. **Trend Analysis**
   - Supports strategic planning through trend and seasonal analysis
   
3. **Performance Optimization**
   - Enables data-driven decisions for sales and marketing optimization

4. **Revenue Growth**
   - Identifies opportunities for cross-selling and upselling
   
5. **Operational Efficiency**
   - Reduces reporting time and improves data accessibility

---

## 🚀 Tools & Skills

### Technical Stack
- **Power BI Desktop** - Dashboard development and visualization
- **Power Query (M)** - Data extraction, transformation, and loading (ETL)
- **DAX** - Advanced calculations and time intelligence
- **Data Modeling** - Star Schema design and relationship management

### Skills Demonstrated
- ✅ Business Intelligence & Analytics
- ✅ Data Visualization
- ✅ ETL Processes
- ✅ Performance Optimization
- ✅ Dashboard Design (UX/UI)
- ✅ Storytelling with Data

---

## 📁 Project Structure

```
Superstore-Sales-Dashboard/
│
├── Superstore_Sales_Dashboard.pbix    # Main Power BI dashboard file
├── superstore_final_dataset.csv       # Cleaned dataset
├── bg.png                              # Dashboard background
├── logo.jpg                            # Brand logo
└── README.md                           # Project documentation
```

---

## 🚀 Getting Started

### Prerequisites
- Microsoft Power BI Desktop (Latest version)
- Download from: https://powerbi.microsoft.com/desktop/

### Installation Steps

1. **Clone the repository**
   ```bash
   git clone https://github.com/trieuha573/Superstore-Sales-Dashboard.git
   ```

2. **Open the dashboard**
   - Navigate to the project folder
   - Double-click `Superstore_Sales_Dashboard.pbix`
   - Or open Power BI Desktop → File → Open

3. **Refresh data** (if needed)
   - Click "Refresh" on the Home ribbon
   - Data loads from `superstore_final_dataset.csv`

4. **Explore the dashboard**
   - Use slicers and filters to interact
   - Click visuals for cross-filtering
   - Hover for dynamic tooltips

---

## 📈 Dashboard Pages

### Page 1: Sales Performance Overview
- High-level KPIs (Total Sales, Profit, AOV)
- Revenue trends over time
- Top-performing categories and products

### Page 2: Customer Behavior Analysis
- Customer segmentation breakdown
- Purchase patterns and frequency
- Customer lifetime value (CLV)

### Page 3: Product & Regional Insights
- Category and sub-category performance
- Regional sales distribution
- Geographic heat maps

---

## 📊 Sample Visualizations

- **KPI Cards**: Total Sales, Profit Margin, Number of Orders
- **Line Charts**: Revenue trends, MoM/YoY growth
- **Bar/Column Charts**: Top products, category comparison
- **Pie/Donut Charts**: Customer segment distribution
- **Maps**: Geographic sales performance
- **Tables**: Detailed product listings with drill-through

---

## 🎯 Key Performance Indicators (KPIs)

| KPI | Description | DAX Measure |
|-----|-------------|-------------|
| **Total Sales** | Sum of all revenue | `SUM(Sales[Sales Amount])` |
| **Average Order Value** | Revenue per order | `DIVIDE([Total Sales], [Order Count])` |
| **MoM Growth** | Month-over-month change | Time intelligence calculation |
| **YoY Growth** | Year-over-year change | `SAMEPERIODLASTYEAR` function |
| **QTD Sales** | Quarter-to-date revenue | `TOTALQTD` function |
| **Profit Margin** | Profitability percentage | `DIVIDE([Profit], [Sales])` |

---

## 💡 Insights & Recommendations

### Strategic Recommendations

1. **Focus on Technology Category**
   - Highest revenue contributor (38%)
   - Recommend increased inventory and marketing

2. **Nurture Consumer Segment**
   - Largest customer base (52%)
   - Implement loyalty programs

3. **Capitalize on Seasonality**
   - Plan inventory for Q4 peaks
   - Launch targeted campaigns in November-December

4. **Regional Expansion**
   - Identify underperforming regions
   - Allocate resources strategically

---
