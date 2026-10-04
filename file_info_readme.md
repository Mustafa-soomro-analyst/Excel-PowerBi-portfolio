# 📊 Executive Sales Analytics Dashboard (Excel & Power Query)

An interactive, end-to-end sales analytics dashboard engineered in Microsoft Excel using Power Query and Pivot data modeling. This project tracks multi-channel retail operations across Pakistan (2025–2026), providing executive-level visibility into top-line revenue, regional distribution, channel contribution, order fulfillment rates, and product performance.

## 📸 Dashboard Preview


*(Replace `dashboard_screenshot.png` with your exported dashboard image)*

## 🎯 Executive Summary & Core KPIs

| Metric | Value | Business Definition | 
| ----- | ----- | ----- | 
| **Total Revenue** | **PKR 2.98B** | Gross transaction value across all channels and order statuses | 
| **Total Quantity** | **33K** | Total volume of physical inventory units sold | 
| **Average Order Value (AOV)** | **PKR 596.04K** | Mean transaction size per generated order (`Total Revenue / Total Orders`) | 
| **Total Orders** | **5K** | Unique volume of customer transactions processed | 

## 🚀 Key Business Insights

1. **Top Revenue Generators:**

   * **External HDDs** and **Mechanical Keyboards** are the highest revenue-generating product lines, with External HDDs leading at nearly PKR 600M.

   * Peripherals and storage hardware consistently outperform general consumer electronics.

2. **Regional Distribution:**

   * Sales are well-distributed across tier-1 and tier-2 logistics hubs across Pakistan.

   * **Islamabad**, **Faisalabad**, and **Karachi** are the top three performing territories, each driving over PKR 300M in revenue.

3. **Multi-Channel Equilibrium:**

   * Sales channels maintain an exceptionally balanced volume share:

     * **Online Portal:** 25.78%

     * **Marketplace:** 25.38%

     * **Physical Stores:** 24.56%

     * **WhatsApp Business:** 24.28%

   * This indicates balanced omni-channel customer acquisition with low platform dependency risk.

4. **Fulfillment Pipeline:**

   * **Completed Orders:** PKR 1.74B (\~58% of gross gross pipeline).

   * **Pending Pipeline:** PKR 0.40B currently in fulfillment.

   * **Operational Leakage:** PKR 0.44B in cancellations and PKR 0.40B in returns, highlighting an opportunity to tighten fulfillment SLA and return rates.

## 🛠️ Data Architecture & Pipeline

### 1. Data Ingestion & Transformation (Power Query)

* **Source File:** `Power_Query_Dataset.xlsx`

* **ETL Cleaning Steps:**

  * Standardized date types and derived calendar columns (`Year`, `Quarter`, `Month`).

  * Cast numerical dimensions (`Quantity`, `Unit Price`, `Total Amount`) to clean currency and integer types.

  * Trimmed categorical strings (`Sales Channel`, `Region`, `Order Status`, `Product Category`).

  * Filtered null values and trailing blanks to maintain dimensional integrity.

### 2. Analytical Modeling

* Utilized an analytical data schema linking transaction records to regional and product dimensional tables.

* Leveraged Excel Pivot Tables and calculated fields to aggregate data across multiple slicing dimensions.

## 🎛️ Interactive Controls & Slicers

The dashboard features a dedicated left-rail filtering pane linked via slicer cache connections across all visual components:

* **Temporal Slicers:** `Year` (2025, 2026), `Quarter` (Q1–Q4), and `Month` (January–December).

* **Channel Slicers:** `Marketplace`, `Online`, `Store`, and `WhatsApp`.

* Dynamic cross-filtering enabled across all visuals simultaneously.

## 📂 Repository Structure

```
├── data/
│   └── Power_Query_Dataset.xlsx   # Cleaned dataset and source data model
├── assets/
│   └── dashboard_screenshot.png    # High-resolution dashboard capture
├── Sales_Dashboard.xlsx            # Primary interactive workbook
└── README.md                       # Project documentation

```

## 💻 How to Use

1. **Clone the repository:**

   ```
   git clone https://github.com/your-username/sales-performance-dashboard.git
   
   ```

2. **Open the Workbook:**

   * Open `Sales_Dashboard.xlsx` in **Microsoft Excel 2019, 2021, or Office 365** (desktop edition recommended for full slicer interactivity).

3. **Refresh Data Connections (Optional):**

   * Navigate to the **Data** tab on the ribbon $\rightarrow$ click **Refresh All** to reload calculations from the underlying Power Query model.

## 👤 Author

* **Portfolio / Profile:** Mustafa-soomro-analyst