# E-commerce 360° Business Intelligence Suite

A comprehensive, three-page interactive Power BI dashboard designed to bridge the gap between high-level executive KPIs and granular operational data. This project replicates a real-world enterprise analytics system, focusing on three core business pillars: Sales & Product Intelligence, Supply Chain & Logistics Operations, and Digital Marketing Web Analytics.

---

## 📂 Project Assets & Downloads

> 📌 **Access the Full Project Portfolio:**
> You can download the complete interactive files and high-resolution presentation formats from the official Google Drive folder linked below:
> 
> 👉 **Download .PBIX Dashboard ([Dashboard](https://drive.google.com/file/d/1nBjmy1gXLuSlKWkQK5WRg-HE4hJxYnWg/view?usp=drive_link))**
>     **Download PDF Presentation ([Presentation](https://drive.google.com/file/d/193092AkRXwS8sEv_bVyitDgC0E90IoxZ/view?usp=drive_link))**
> *   `Ecom_Operations_and_Web_Analytics.pbix` — The complete Power BI Desktop model to inspect relationships, data transforms, and DAX calculations.
> *   `Ecom_Operations_and_Web_Analytics_Presentation.pdf` — A static, executive-ready presentation of the dashboard pages for instant viewing.

---

## 📊 Product Performance & Sales Intelligence

### 🎯 Business Objective
Designed for Chief Commercial Officers (CCOs) and Category Managers to drive strategic assortment management. The interface isolates high-margin revenue drivers from dead stock that ties up working capital, while validating pricing strategy health.

### 🛠️ Key Metrics & DAX Calculations
Built using complex conditional logic and robust DAX statistical measures:
*   **Total Revenue & Profit:** End-to-end calculations dynamically responding to multi-tier filtering across calendar years and business lines.
*   **Margin % (Profitability Matrix):** A dynamic ratio measure evaluating commercial efficiency, calculated as:
    $$Margin\% = \frac{Total\ Profit}{Total\ Revenue}$$
*   **AOV (Average Order Value):** Monitored across brands to analyze customer purchasing power and validate cross-selling marketing campaigns.

### 🔬 Analytical Frameworks
*   **ABC / Pareto Analysis (80/20 Rule):** Features a dual-axis combination chart mapping cumulative profit concentration. It explicitly categorizes "Class A" products and brands responsible for generating 80% of total company profit.
*   **Product Price Scatter Matrix:** A spatial distribution chart plotting brands by order volume against average retail price. This maps out structural price segments (Low-cost, Mass-market, Premium) and highlights performance anomalies.
*   **Full Contextual Cross-Filtering:** Clicking any product tier or brand instantly morphs the summary cards, allowing rapid drill-downs without needing additional report pages.

---

## 🚛 Logistics & Supply Chain Operations

### 🎯 Business Objective
Engineered for Operations Directors and Supply Chain Managers to audit carrier fulfillment efficiency, identify bottlenecks in the distribution network, and monitor real-time order backlogs.

### 🛠️ Key Metrics & DAX Calculations
*   **Fulfillment Performance Limits:** Measures maximum and median transit durations to expose tail-end service degradation rather than just relying on generic averages.
*   **Dynamic Order Tracking Log:** A low-level micro-data table that cleanly renames native system columns into readable business components (`Order ID`, `Order Date`, `Carrier`, `Delivery Days`, `Status`).

### 🔬 Analytical Frameworks
*   **Carrier Delivery Days Breakdown:** A side-by-side comparison chart matching median delivery times against maximum delays for every distributor. This directly visualizes operational risk and SLA (Service Level Agreement) breaches.
*   **Order Status Distribution (Donut Hub):** Captures the operational load by status (`Shipped`, `Processing`, `Cancelled`, `Complete`, `Returned`). 
*   **Root-Cause Drill-Down:** Selecting the `Returned` sector instantly filters the entire page, mapping exactly which cities, countries, and carriers are causing the highest product return rates.

---

## 🌐 Digital Marketing & Web Analytics

### 🎯 Business Objective
Built for Chief Marketing Officers (CMOs) and Performance Marketers to audit traffic acquisition quality, evaluate customer behavior patterns, and optimize advertising budget allocation.

### 🛠️ Key Metrics & DAX Calculations
*   **Traffic Session Aggregations:** Processes thousands of raw clickstream logs to isolate true traffic volume independent of sales data.
*   **Temporal Performance Modifiers:** Models web events over distinct date dimensions to pinpoint specific engagement windows.

### 🔬 Analytical Frameworks
*   **100% Stacked Traffic Source Mix:** Solves the challenge of disconnected fact tables with different granularities (`web_traffic_events` and `orders_master_data`). By charting acquisition mix directly within geographic dimensions, it visualizes marketing footprints across international regions.
*   **Dual-Timeline Trend Analysis:** 
    *   *Macro-Trend (Monthly Line):* Tracks long-term traffic growth and seasonal e-commerce surges toward the end of the fiscal year.
    *   *Micro-Trend (Weekday Area):* Isolates weekly patterns, highlighting consistent peak engagement on Thursdays followed by predictable weekend drops.
*   **Platform & Browser Segmentation:** Maps user session distribution across core software ecosystems (`Chrome`, `Safari`, `Firefox`, `IE`), defining optimization priorities for frontend engineering.

---

## ⚡ Technical Core & Architecture

*   **Data Modeling:** Star Schema design utilizing central Fact tables (`orders_master_data`, `web_traffic_events`) conformed to shared Dimension tables (`Calendar table`, `Geography`).
*   **UX/UI Optimization:** Clean, modern enterprise UI utilizing a dedicated left-anchored navigation drawer (`Page Navigator`) and space-saving dropdown slicing controls for a seamless web-app feel.
