# 🚀 Q-Commerce Data Analysis

A comprehensive data analysis project exploring Quick Commerce (Q-Commerce) order data from platforms like **Blinkit**, **Zepto**, and **Swiggy Instamart**. The project covers end-to-end data analytics — from data cleaning to business insights and a mini dashboard.

---

## 📋 Table of Contents

- [Project Overview](#project-overview)
- [Dataset](#dataset)
- [Technologies Used](#technologies-used)
- [Project Structure](#project-structure)
- [Analysis Workflow](#analysis-workflow)
- [Business Questions Answered](#business-questions-answered)
- [Key Insights](#key-insights)
- [How to Run](#how-to-run)
- [Author](#author)

---

## 📌 Project Overview

Quick Commerce platforms promise ultra-fast deliveries (10–30 minutes). This project uses a **synthetic Q-Commerce dataset** to simulate real-world order data and extract meaningful business insights through data cleaning, exploratory data analysis (EDA), and visualizations.

---

## 📂 Dataset

The dataset is a **synthetic Quick Commerce Analytics Dataset** containing order-level records with the following key features:

| Feature | Description |
|---|---|
| `Order_ID` | Unique identifier for each order |
| `Company` | Q-Commerce platform (Blinkit, Zepto, Swiggy Instamart, etc.) |
| `City` | City where the order was placed |
| `Category` | Product category |
| `Items_Count` | Number of items in the order |
| `Order_Value` | Total value of the order (INR) |
| `Delivery_Time_Min` | Delivery time in minutes |
| `Customer_Rating` | Rating given by the customer (1–5) |
| `Delivery_Partner_Rating` | Rating given to the delivery partner (1–5) |
| `Discount_Applied` | Discount applied on the order |
| `Revenue` | Revenue generated from the order |

---

## 🛠️ Technologies Used

- **Python 3**
- **Pandas** — Data manipulation and cleaning
- **NumPy** — Numerical computations
- **Matplotlib** — Static visualizations
- **Seaborn** — Statistical data visualization
- **Plotly Express** — Interactive visualizations
- **Jupyter Notebook** — Interactive development environment

---

## 📁 Project Structure

```
Q-Commerce-Data-Analysis/
│
├── Project+15+-+Quick+Commerce+Data+Analysis.ipynb   # Main analysis notebook
└── README.md                                          # Project documentation
```

---

## 🔄 Analysis Workflow

1. **Data Loading** — Load the raw Q-Commerce CSV dataset
2. **Data Exploration** — Understand structure, data types, and summary statistics
3. **Data Cleaning**
   - Drop rows with missing values in critical columns (e.g., `City`)
   - Fill missing values using mode (e.g., `Items_Count`)
   - Group-wise mean/median imputation (e.g., `Customer_Rating`, `Delivery_Partner_Rating`)
4. **Outlier Removal** — Filter extreme values using box plots and threshold filtering
5. **Data Type Conversion** — Cast columns to appropriate data types
6. **Business Analysis** — Answer 8 key business questions
7. **Mini Dashboard** — Visual summary of key metrics

---

## ❓ Business Questions Answered

| # | Question |
|---|---|
| 1 | Which quick commerce platform has the **highest total revenue**? |
| 2 | Which platform has the **highest average order value (AOV)**? |
| 3 | How does **Customer Rating** vary across platforms? |
| 4 | Does **Delivery Time** affect **Delivery Partner Ratings**? |
| 5 | What is the most popular **Product Category** on Swiggy Instamart for customers aged 30–40 in Mumbai? |
| 6 | Which **cities** should these companies expand into based on performance? |
| 7 | Are **discounts** increasing order volume or just reducing revenue? |
| 8 | Which company has the best **Operational Efficiency** (Delivery Time vs Order Volume)? |

---

## 💡 Key Insights

- Platform revenue and average order values vary significantly, helping identify market leaders.
- Customer ratings and delivery partner ratings are closely linked to delivery time.
- Targeted analysis by age group and city reveals niche market opportunities.
- Discounts have a nuanced effect — they boost volume but may erode margins.
- Operational efficiency metrics guide strategic expansion and resource allocation.

---

## ▶️ How to Run

1. **Clone the repository**
   ```bash
   git clone https://github.com/technicalabinesh/Q-Commerce-Data-Analysis.git
   cd Q-Commerce-Data-Analysis
   ```

2. **Install the required libraries**
   ```bash
   pip install pandas numpy matplotlib seaborn plotly
   ```

3. **Open the Jupyter Notebook**
   ```bash
   jupyter notebook "Project+15+-+Quick+Commerce+Data+Analysis.ipynb"
   ```

4. **Update the dataset path** in the notebook to point to your local CSV file:
   ```python
   df = pd.read_csv("path/to/quick_commerce_data_raw.csv")
   ```

5. **Run all cells** to reproduce the analysis.

---

## 👤 Author

Original notebook by **Rohit Grewal** — [Data Science Lovers](https://www.youtube.com/@DataScienceLovers)

---

> ⭐ If you found this project helpful, please consider giving it a star!