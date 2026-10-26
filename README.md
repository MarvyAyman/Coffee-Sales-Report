# ☕ Brew & Co. — Coffee Shop Sales Dashboard

An interactive **Looker Studio** dashboard analyzing six months of sales (Jan – Jun 2023) across three coffee shop locations in New York City. It turns raw transaction data into clear answers: *how much are we earning, what is selling, when are customers coming, and which store performs best?*

🔗 **Live Dashboard:** [Open in Looker Studio]([YOUR_LOOKER_STUDIO_LINK_HERE](https://datastudio.google.com/reporting/6478f49e-8614-435e-b49a-a178820a0337))

---

## 📸 Dashboard Preview

<!-- Upload your screenshot to the /images folder and keep this file name (or update the path) -->
![Brew & Co. Dashboard](images/dashboard-overview.png)

---

## 🎯 Business Objective

Give management a single-page view of store performance so they can:

- Track revenue, transactions, and average order value over time
- Identify best-selling categories and products
- Understand peak hours to plan staffing and inventory
- Compare performance across store locations

---

## 📊 Key Metrics (KPIs)

| Metric | Value | Description |
|---|---|---|
| **Total Revenue** | $699K | Total sales across all stores |
| **Transactions** | 149K | Number of completed orders |
| **Avg Order Value** | $4.69 | Revenue ÷ Transactions |
| **Units Sold** | 214K | Total quantity of items sold |

---

## 🧮 Calculated Fields

| Field | Formula (Looker Studio) |
|---|---|
| **Revenue** | `SUM(unit_price * transaction_qty)` |
| **Avg Order Value** | `SUM(Revenue) / COUNT(transaction_id)` |
| **Units Sold** | `SUM(transaction_qty)` |
| **Transactions** | `COUNT(transaction_id)` |

---

## 🔍 Dashboard Sections & Insights

### 1. Revenue & Transaction Trends
Daily revenue line chart for Jan–Jun 2023.
**Insight:** Revenue grew steadily, with monthly revenue roughly **doubling from ~$82K in January to ~$166K in June**.

### 2. Revenue by Category
Share of sales by product category.
**Insight:** **Coffee ($270K)** and **Tea ($196K)** together generate about two-thirds of total revenue, followed by Bakery, Drinking Chocolate, and Coffee Beans.

### 3. Top Products
Top 5 products ranked by total revenue.
**Insight:** Large-size items dominate the ranking (Sustainably Grown Organic Lg, Dark Chocolate Lg, Cappuccino Lg, Morning Sunrise Chai Lg), alongside the regular Latte.

### 4. Hourly Traffic
Transaction volume by hour of day.
**Insight:** Traffic peaks between **8 and 10 AM** (~18K transactions per hour), drops sharply after 11 AM, and stays flat through the afternoon.

### 5. Store Performance
Revenue share per location.
**Insight:** The three stores are almost evenly balanced: Hell's Kitchen (33.84%), Astoria (33.23%), and Lower Manhattan (32.92%).

### 🎛️ Interactive Filters
- **Store Location** — focus on a single store
- **Date Range** — analyze any custom period

---

## 🛠️ Tools & Technologies

- **Looker Studio** — dashboard design and visualization
- **Excel / Google Sheets** — data source
- **Calculated fields** — Revenue, Average Order Value

---

## 📁 Dataset

- **Source:** [Maven Analytics — Coffee Shop Sales]([https://mavenanalytics.io/data-playground](https://mavenanalytics.io/data-playground/coffee-shop-sales)) 
- **Period:** 1 Jan 2023 – 30 Jun 2023
- **Size:** 149,116 rows × 11 columns (one row per transaction)
- **Quality:** Cleaned, no missing values
- **Coverage:** 3 stores, 9 product categories, 29 product types, 80 products

### Data Dictionary

| Column | Type | Description |
|---|---|---|
| `transaction_id` | Integer | Unique ID for each transaction |
| `transaction_date` | Date | Date of the sale (MM/DD/YY) |
| `transaction_time` | Time | Time of the sale (HH:MM:SS) |
| `transaction_qty` | Integer | Quantity of items sold |
| `store_id` | Integer | Unique ID of the store |
| `store_location` | Text | Store location (Hell's Kitchen, Astoria, Lower Manhattan) |
| `product_id` | Integer | Unique ID of the product |
| `unit_price` | Decimal | Retail price of one unit |
| `product_category` | Text | Product group (Coffee, Tea, Bakery, ...) |
| `product_type` | Text | Product sub-category |
| `product_detail` | Text | Product name including size (e.g., Latte Rg, Cappuccino Lg) |

---

## 📂 Repository Structure

```
Coffee-Sales-Report/
│
├── README.md                      # Project documentation
│
├── data/
│   └── Coffee_Shop_Sales.xlsx     # Cleaned dataset used in the dashboard
│
├── images/
│   └── dashboard-overview.png     # Dashboard screenshot used in the README
```

| Folder / File | Purpose |
|---|---|
| `README.md` | Overview, KPIs, formulas, insights, and links |
| `data/` | The cleaned dataset connected to Looker Studio |
| `images/` | Screenshots used in the README |
| `LICENSE` | Usage terms (optional) |

---

## 🚀 How to Use

1. Open the [live dashboard]([YOUR_LOOKER_STUDIO_LINK_HERE](https://datastudio.google.com/reporting/6478f49e-8614-435e-b49a-a178820a0337)).
2. Use the **Store Location** and **Date Range** filters at the top.
3. Hover over charts for exact values.

**To rebuild it yourself:**
1. Upload `data/Coffee_Shop_Sales.xlsx` to Google Sheets.
2. Create a new Looker Studio report and connect the sheet.
3. Add the calculated fields from the table above.
4. Build the charts as described in the dashboard sections.

---

## 💡 Recommendations

- Staff up and prep inventory for the **8–10 AM** rush.
- Promote **Bakery** items alongside coffee and tea to raise average order value.
- Large sizes lead the top products, so highlight them in menu and upsell strategies.
- Stores perform almost equally, so test location-specific promotions to find growth opportunities.

---

## 👤 Author

**Marvy** — Freelance Full-Stack Developer & Data Analyst
- GitHub: [@MarvyAyman](https://github.com/your-username)
- LinkedIn: [Marvy Ayman](https://linkedin.com/in/your-profile)
- Khamsat: https://khamsat.com/user/marvy_ayman
- Upwork: https://www.upwork.com/freelancers/~01162cc3d042c59e01

---

⭐ If you found this project useful, consider giving it a star!
