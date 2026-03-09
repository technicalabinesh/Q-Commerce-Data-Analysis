# 🚀 Q-Commerce Data Analysis

A comprehensive data analysis project on **Quick Commerce (Q-Commerce)** platforms — exploring order patterns, delivery efficiency, customer behaviour, and revenue insights across platforms like Blinkit, Zepto, Swiggy Instamart, BigBasket Now, Dunzo, and JioMart Express.

---

## 📁 Repository Structure

```
Q-Commerce-Data-Analysis/
├── quick_commerce_data_raw.csv           # Raw synthetic dataset (5,000 orders)
├── Project+15+-+Quick+Commerce+Data+Analysis.ipynb  # Main analysis notebook
└── README.md
```

---

## 📊 Dataset Description

**File:** `quick_commerce_data_raw.csv`  
**Rows:** 5,000 | **Columns:** 12

This is a **synthetic Quick Commerce dataset** simulating real-world order data from major Q-Commerce platforms in India. It contains order-level features including city, category, delivery time, ratings, discounts, and revenue — making it ideal for practising data cleaning, EDA, visualisation, and business insight extraction.

| Column | Type | Description |
|---|---|---|
| `Order_ID` | String | Unique identifier for each order (e.g. `ORD000001`) |
| `Company` | String | Quick commerce platform name |
| `City` | String | City where the order was placed (contains ~3% nulls) |
| `Customer_Age` | Integer | Age of the customer (18–64) |
| `Product_Category` | String | Category of the ordered product |
| `Discount_Applied` | String | Whether a discount was applied (`Yes` / `No`) |
| `Order_Value` | Float | Total order value in INR (₹100–₹3,000) |
| `Delivery_Time_Min` | Float | Delivery time in minutes (5–60 mins) |
| `Distance_Km` | Float | Delivery distance in kilometres (0.5–10 km) |
| `Items_Count` | Float | Number of items in the order (contains ~3% nulls) |
| `Customer_Rating` | Float | Customer satisfaction rating (1–5; contains ~4% nulls) |
| `Delivery_Partner_Rating` | Float | Delivery partner rating (1–5; contains ~4% nulls) |

### Platforms Covered
- **Blinkit** · **Zepto** · **Swiggy Instamart** · **BigBasket Now** · **Dunzo** · **JioMart Express**

### Cities Covered
- Mumbai · Delhi · Bangalore · Hyderabad · Chennai · Kolkata · Pune · Ahmedabad

### Product Categories
Groceries, Dairy & Eggs, Fruits & Vegetables, Beverages, Snacks & Munchies, Personal Care, Baby Care, Household Essentials, Meat & Seafood, Bakery

---

## 🔍 Business Questions Answered

| # | Question |
|---|---|
| 1 | Which quick commerce platform has the **highest total revenue**? |
| 2 | Which platform has the highest **Average Order Value (AOV)**? |
| 3 | How does **Customer Rating** vary across platforms? |
| 4 | Does **Delivery Time** affect **Delivery Partner Ratings**? |
| 5 | What is the most popular **Product Category** on Swiggy Instamart for customers aged 30–40 in Mumbai? |
| 6 | Which **cities** should companies expand into based on performance? |
| 7 | Are **discounts** increasing order volume or just reducing revenue? |
| 8 | Which company has the best **Operational Efficiency** (Delivery Time vs Order Volume)? |

---

## 🛠️ Data Cleaning Steps

1. **Remove rows** with null values in the `City` column
2. **Fill missing** `Items_Count` values using the **mode**
3. **Fill missing** `Customer_Rating` using **group-wise mean** (grouped by `Company`)
4. **Fill missing** `Delivery_Partner_Rating` using **group-wise mean** (grouped by `Delivery_Time_Min`)
5. **Remove outliers** in `Order_Value` (cap at ₹2,500)
6. **Type casting** — convert float columns to integers, `Order_ID` to string
7. **Round-off** float values for cleaner presentation

---

## 📈 Visualisations Used

- Bar Charts · Line Charts · Box Plots · Stem Charts
- Grouped Bar Charts · Scatter Bubble Plots (Plotly)
- Mini KPI Dashboard (Matplotlib subplot grid)

---

## ⚙️ Requirements

```bash
pip install pandas numpy matplotlib seaborn plotly scikit-learn
```

---

## 🚀 Getting Started

1. Clone the repository:
   ```bash
   git clone https://github.com/technicalabinesh/Q-Commerce-Data-Analysis.git
   cd Q-Commerce-Data-Analysis
   ```
2. Install dependencies:
   ```bash
   pip install pandas numpy matplotlib seaborn plotly scikit-learn
   ```
3. Open the notebook:
   ```bash
   jupyter notebook "Project+15+-+Quick+Commerce+Data+Analysis.ipynb"
   ```
4. The notebook will load `quick_commerce_data_raw.csv` from the repository root. Update the file path in **Cell 5** if needed:
   ```python
   df = pd.read_csv("quick_commerce_data_raw.csv")
   ```

---

## 📌 Key Insights (from Analysis)

- Platforms with **lower delivery times** tend to receive **higher delivery partner ratings**
- **Discounted orders** show different order-value patterns compared to non-discounted ones
- City-level performance varies significantly — enabling targeted **expansion strategies**
- Operational efficiency scores reveal clear leaders in **high-volume, fast-delivery** combinations

---

*by Rohit Grewal / Data Science Lovers*