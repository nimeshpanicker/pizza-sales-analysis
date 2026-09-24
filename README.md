# 🍕 Pizza Sales Analysis Dashboard

![Power BI](https://img.shields.io/badge/Power%20BI-Dashboard-yellow)
![SQL](https://img.shields.io/badge/SQL-Analysis-blue)
![Microsoft Excel](https://img.shields.io/badge/Microsoft%20Excel-Data%20Analysis-green)
![Data Analytics](https://img.shields.io/badge/Data%20Analytics-Portfolio-orange)
![Status](https://img.shields.io/badge/Project-Completed-success)

> An interactive SQL, Excel, and Power BI analytics project analysing pizza
> sales performance, revenue, order volume, product performance, pizza
> categories, sizes, and monthly and day-of-week sales patterns.

---

# 📌 Project Overview

This project analyses one full year of pizza sales transactions from
**January 2025 to December 2025**.

The analysis combines **Microsoft Excel/CSV for data preparation, SQL for
KPI and aggregate calculations, and Power BI for interactive dashboard
visualization**.

The objective is to understand overall sales performance, customer ordering
behaviour, and the products, categories, and pizza sizes driving revenue.

The analysis covers:

- Revenue performance
- Order volume
- Pizza quantity sold
- Average order value
- Average pizzas per order
- Monthly revenue trends
- Day-of-week order patterns
- Pizza category performance
- Pizza size performance
- Top and bottom-performing pizzas
- Interactive Power BI filtering

The project processes **48,606 order-line records** across **21,334
distinct orders**, covering **32 pizza products, 4 categories, and 5 pizza
sizes**.

---

# 🎯 Project Objectives

The main objectives of this project are:

- Analyse one full year of pizza sales transactions.
- Calculate core sales KPIs.
- Track total revenue and order volume.
- Analyse monthly revenue trends.
- Identify day-of-week ordering patterns.
- Compare performance across pizza categories.
- Analyse revenue distribution by pizza size.
- Identify top-performing pizzas by revenue.
- Identify top-performing pizzas by order frequency.
- Identify top-performing pizzas by quantity sold.
- Identify consistently underperforming pizza products.
- Build an interactive Power BI dashboard.
- Provide data-driven business recommendations.

---

# 📊 Dataset

The analysis is based on a single transactional dataset:

**PIZZA.csv**

The same dataset is also modelled in SQL as:

**PIZZA_SALES**

| Dataset Attribute | Details |
|---|---|
| Total Records | **48,606 order lines** |
| Total Columns | **12** |
| Reporting Period | **01 January 2025 – 31 December 2025** |
| Data Grain | **One row per pizza sold within an order** |
| Distinct Orders | **21,334** |
| Distinct Pizza Products | **32** |
| Pizza Categories | **4** |
| Pizza Sizes | **5** |

### Pizza Categories

- Classic
- Supreme
- Chicken
- Veggie

### Pizza Sizes

- Small
- Medium
- Large
- XLarge
- XXLarge

---

# 🗂️ Dataset Columns

| Column | Description |
|---|---|
| `pizza_id` | Unique pizza transaction identifier |
| `order_id` | Identifier grouping pizzas into an order |
| `pizza_name_id` | Pizza product identifier |
| `quantity` | Number of pizzas sold |
| `order_date` | Date of the order |
| `order_time` | Time of the order |
| `unit_price` | Price per pizza |
| `total_price` | Total transaction value |
| `pizza_size` | Pizza size |
| `pizza_category` | Pizza category |
| `pizza_ingredients` | Pizza ingredient description |
| `pizza_name` | Pizza product name |

The SQL schema defines these 12 fields in the `PIZZA_SALES` table. 

---

# 🧹 Data Preparation & Validation

Before analysis, the dataset was reviewed and validated.

The following checks were performed:

- Reviewed the complete dataset structure.
- Confirmed **48,606 rows and 12 columns**.
- Checked all columns for missing values.
- Confirmed that **no null values were found**.
- Checked for duplicate order-line records.
- Confirmed that **no duplicate order-line records were found**.
- Verified numeric and date/time data types.
- Standardized and reviewed column names.
- Validated `total_price` against `quantity × unit_price`.
- Confirmed that the date field covers the complete January–December 2025 period.
- Loaded the validated data into SQL for KPI and aggregate analysis.
- Connected the resulting analysis to Power BI.

---

# 🛠️ Tools & Technologies

| Tool | Purpose |
|---|---|
| **Microsoft Excel** | Data handling and preparation |
| **CSV** | Transactional data source |
| **SQL** | KPI calculations, aggregation and ranking |
| **Power BI** | Interactive dashboard development |
| **DAX** | KPI and dashboard calculations |
| **Data Visualization** | Business performance analysis |
| **Data Storytelling** | Business insights and recommendations |

---

# 📈 Dashboard

The **Pizza Sales Performance Report** is a single-page interactive
Power BI dashboard built using the validated `PIZZA_SALES` dataset.

The dashboard contains:

- **5 KPI cards**
- **6 analytical charts**
- **3 interactive slicers**

### Dashboard Components

#### KPI Cards

- Total Revenue
- Total Orders
- Total Pizza Sold
- Average Pizza per Order
- Average Order Value

#### Analytical Visuals

- Monthly Revenue Trend
- Orders by Day of Week
- Sales Distribution by Category
- Sales Distribution by Pizza Size
- Total Pizza Sold by Size & Category
- Total Revenue by Pizza Name

#### Interactive Filters

- Year
- Pizza Category
- Pizza Size

These filters allow users to explore performance at different levels of
granularity.

---

# 🔢 Key Performance Indicators

| KPI | Result |
|---|---:|
| Total Revenue | **$817,621.80** |
| Total Orders | **21,334** |
| Total Pizzas Sold | **49,559** |
| Average Order Value | **$38.32** |
| Average Pizzas per Order | **2.32** |

### KPI Interpretation

**Total Revenue:**  
Total sales generated across all orders.

**Total Orders:**  
Number of distinct customer transactions.

**Total Pizzas Sold:**  
Total number of pizza units sold.

**Average Order Value:**  
Average revenue generated per order.

**Average Pizzas per Order:**  
Average number of pizzas included in each order.

> **Data Limitation:** The dataset does not contain cost information, so
> Profit and Profit Margin KPIs cannot be calculated. It also does not
> contain a unique customer identifier, so a Total Customers KPI is not
> included.

---

# 💰 Revenue Analysis

## Monthly Revenue

| Month | Revenue |
|---|---:|
| January | **$69,776.60** |
| February | **$65,159.60** |
| March | **$70,397.10** |
| April | **$68,736.80** |
| May | **$71,238.20** |
| June | **$68,210.00** |
| July | **$72,557.90** |
| August | **$68,262.20** |
| September | **$64,180.00** |
| October | **$64,027.60** |
| November | **$70,374.60** |
| December | **$64,701.20** |

### Monthly Findings

- **July** was the strongest month with **$72,557.90**.
- **October** was the weakest month with **$64,027.60**.
- Revenue remained relatively stable throughout the year.
- Monthly revenue ranged from approximately **$64K to $72.6K**.
- The strongest and weakest months differ by roughly 13%.

Because only one calendar year is available, the September–October decline
should be treated as an observation rather than a confirmed recurring
seasonal trend.

---

# 📅 Order Volume by Day of Week

| Day | Total Orders |
|---|---:|
| Monday | **2,972** |
| Tuesday | **3,024** |
| Wednesday | **3,238** |
| Thursday | **3,535** |
| Friday | **3,158** |
| Saturday | **2,624** |
| Sunday | **2,793** |

### Findings

- **Thursday** is the busiest day with **3,535 orders**.
- **Wednesday** follows with **3,238 orders**.
- **Friday** records **3,158 orders**.
- **Saturday** is the quietest day with **2,624 orders**.

The midweek-heavy and weekend-light pattern can be investigated further
for staffing, operating hours, and promotional planning.

---

# 🍕 Category Performance

| Category | Revenue | % of Total Revenue |
|---|---:|---:|
| Classic | **$219,997.10** | **26.91%** |
| Supreme | **$208,131.00** | **25.46%** |
| Chicken | **$195,848.50** | **23.95%** |
| Veggie | **$193,645.20** | **23.68%** |

### Findings

Revenue is relatively evenly distributed across the four categories.

The difference between the strongest category, **Classic**, and the
weakest, **Veggie**, is only **3.23 percentage points**.

This indicates a diversified category mix rather than dependence on a
single pizza category.

---

# 📏 Pizza Size Performance

| Size | Revenue | % of Total Revenue |
|---|---:|---:|
| Large | **$375,215.45** | **45.89%** |
| Medium | **$249,333.50** | **30.49%** |
| Small | **$177,990.25** | **21.77%** |
| XLarge | **$14,076.00** | **1.72%** |
| XXLarge | **$1,006.60** | **0.12%** |

### Findings

**Large pizzas** generate **45.89%** of total revenue.

Large and Medium pizzas together account for **76.38% of total revenue**.

XLarge and XXLarge pizzas together contribute less than **2% of total
revenue**.

The XLarge and XXLarge sizes are only offered within the Classic category.

---

# 🏆 Top 5 Pizzas by Revenue

| Rank | Pizza | Revenue |
|---|---|---:|
| 1 | The Thai Chicken Pizza | **$43,434.25** |
| 2 | The Barbecue Chicken Pizza | **$42,730.50** |
| 3 | The California Chicken Pizza | **$41,388.75** |
| 4 | The Classic Deluxe Pizza | **$38,164.50** |
| 5 | The Spicy Italian Pizza | **$34,818.75** |

**The Thai Chicken Pizza** is the highest revenue-generating pizza.

---

# 📉 Bottom 5 Pizzas by Revenue

| Rank | Pizza | Revenue |
|---|---|---:|
| 1 | The Brie Carre Pizza | **$11,588.50** |
| 2 | The Green Garden Pizza | **$13,943.75** |
| 3 | The Spinach Supreme Pizza | **$15,277.75** |
| 4 | The Mediterranean Pizza | **$15,360.50** |
| 5 | The Spinach Pesto Pizza | **$15,562.75** |

---

# 🥇 Top Pizzas by Orders & Quantity

| Pizza | Total Orders | Total Quantity Sold |
|---|---:|---:|
| The Classic Deluxe Pizza | **2,328** | **2,452** |
| The Hawaiian Pizza | **2,280** | **2,422** |
| The Pepperoni Pizza | **2,278** | **2,418** |
| The Barbecue Chicken Pizza | **2,271** | **2,430** |
| The Thai Chicken Pizza | **2,225** | **2,371** |

### Key Finding

**The Classic Deluxe Pizza** leads the menu in both order frequency and
total quantity sold.

It is the strongest volume-driving product even though it ranks fourth by
revenue.

---

# ⚠️ Underperforming Pizza

## The Brie Carre Pizza

| Metric | Result |
|---|---:|
| Revenue | **$11,588.50** |
| Orders | **480** |
| Quantity Sold | **490** |

The Brie Carre Pizza is the weakest performer across all three measured
product metrics:

- Revenue
- Order count
- Quantity sold

This makes it a clear candidate for further menu-performance review.

---

# 💡 Key Business Insights

## 1. Revenue Is Diversified Across Categories

Classic, Supreme, Chicken, and Veggie contribute relatively similar shares
of revenue.

The strongest category contributes **26.91%**, while the weakest contributes
**23.68%**.

Therefore, product- and size-level decisions provide a more specific
opportunity than simply shifting investment between categories.

---

## 2. Large and Medium Pizzas Drive Revenue

Large pizzas generate **45.89%** of total revenue.

Large and Medium together account for **76.38%**.

This makes pizza size an important driver of overall sales performance.

---

## 3. Basket Size Provides an Opportunity

The average order contains **2.32 pizzas** and generates **$38.32** in
revenue.

Increasing the number of pizzas per order through bundles or cross-selling
could increase revenue across the existing order base.

---

## 4. Thursday Is the Busiest Day

Thursday records **3,535 orders**, while Saturday records **2,624**.

The midweek-heavy pattern may have implications for staffing and promotional
planning.

---

## 5. July Is the Peak Revenue Month

July generates **$72,557.90**, while October records **$64,027.60**.

The difference is approximately 13%.

Additional years of data would be required to determine whether this pattern
is recurring.

---

## 6. Thai Chicken Pizza Is the Top Revenue Driver

The Thai Chicken Pizza generates **$43,434.25**, making it the highest
revenue-generating individual pizza.

Other chicken pizzas also appear strongly among the top revenue products.

---

## 7. Classic Deluxe Is the Volume Leader

The Classic Deluxe Pizza leads in:

- Total orders
- Total quantity sold

This makes it an important volume-driving menu item.

---

## 8. Brie Carre Is the Consistent Underperformer

The Brie Carre Pizza ranks lowest in revenue, orders, and quantity sold.

Its performance should be reviewed before making any menu decision.

---

## 9. Classic Small Pizzas Show Strong Volume

Classic pizzas account for **6,137 Small-size units**, considerably higher
than other category-size combinations.

This pattern could support a targeted small-pizza or lunch-oriented offer.

---

## 10. XLarge and XXLarge Are Niche Sizes

XLarge and XXLarge together contribute less than **2% of total revenue**.

Both sizes are available only within the Classic category.

Their continued presence can therefore be evaluated against operational
complexity and future demand.

---

# 📋 Business Recommendations

## 🍕 Promote Large & Medium Sizes

Focus promotional campaigns and combo pricing around Large and Medium
pizzas because together they generate more than three-quarters of total
revenue.

---

## 🛒 Increase Basket Size

Introduce:

- Multi-pizza bundles
- "Add a second pizza" prompts
- Combo offers
- Upsizing opportunities

The objective would be to increase the current **2.32 pizzas per order**.

---

## 📅 Investigate Weekend Demand

Investigate why Saturday records the lowest order volume.

Possible areas for analysis include:

- Staffing
- Operating hours
- Promotions
- Competition
- Customer demand patterns

A weekend-specific promotion could be tested and measured.

---

## 📆 Address September–October Weakness

Consider targeted promotions or limited-time offers during September and
October.

The pattern should then be monitored over additional years before being
treated as a recurring seasonal trend.

---

## ⭐ Promote High-Revenue Products

Feature high-performing products such as:

- The Thai Chicken Pizza
- The Barbecue Chicken Pizza
- The California Chicken Pizza

Ingredient availability should also be monitored for high-demand products.

---

## 🏆 Protect Classic Deluxe Performance

The Classic Deluxe Pizza is the highest-volume product by both orders and
quantity sold.

Its recipe, pricing, availability, and customer experience should be
monitored carefully.

---

## 🔍 Review Brie Carre Performance

Evaluate:

- Pricing
- Recipe
- Menu placement
- Promotion
- Product positioning

before considering a menu change.

---

## 📦 Evaluate XLarge & XXLarge Sizes

Because these sizes contribute less than 2% of total revenue, management
can evaluate whether their menu and inventory complexity is justified.

---


# 📁 Project Structure

```text
pizza-sales-analysis/
│
├── README.md
│
├── data/
│   └── PIZZA.csv
│
├── sql/
│   └── pizza.sql
│
├── dashboard/
│   └── Pizza_Sales_Dashboard.pdf
│
└── reports/
    └── Pizza_Sales_Performance_Report.pdf
