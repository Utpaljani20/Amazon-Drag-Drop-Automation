# 📊 Automated 12-Month Amazon Sales Dashboard

An end-to-end automated sales analytics dashboard designed to process and analyze monthly e-commerce sales datasets. Built to seamlessly handle **all 12 monthly data files**, the pipeline automates data ingestion, cleaning, feature extraction, KPI calculation, and interactive visual reporting.

Simply drag and drop your dataset files, and the app automatically transforms raw transactions into actionable business insights.

---

## ✨ Features

* **⚡ Automated End-to-End Pipeline:** Drag and drop your monthly data files (`.csv` or `.xlsx`) to trigger the automated cleaning, processing, and visualization workflow.
* **🧹 Smart Data Cleaning:**
  * Drops blank and fully empty rows automatically.
  * Filters out redundant header rows introduced by multi-month exports.
  * Handles numerical type conversion and cleans missing data.
  * Dynamically calculates missing revenue metrics (`Sales = Quantity Ordered × Price Each`).
* **⚙️ Feature Engineering:**
  * Extracts granular temporal features: `Year`, `Month`, `MonthName`, `DayName`, and `Hour` from timestamps.
  * Splits delivery locations (`Purchase Address`) into distinct `City` and `State` variables.
* **📌 Real-Time KPI Tracking:**
  * Total Revenue & Total Orders
  * Unique Products & Average Order Value (AOV)
  * Top-performing product by revenue and highest-selling city.
* **📈 Dynamic Visualizations:**
  * Built using a modular charting engine (Bar, Line, and Histogram primitives).
  * Automatically plots monthly sales trends, peak ad hours, regional performance, top products, and pricing distributions.
* **🤝 Co-Purchase Affinity Analysis:**
  * Evaluates order combinations to identify product pairs most frequently purchased together.
* **🎛️ Interactive Filtering:**
  * Dynamically slice data across cities and products via sidebar controls.

---

## 🏗️ Project Architecture

```text
├── Amazon_frontend_simple.py   # Streamlit UI (file uploads, sidebar filters, KPI cards, visual layout)
├── Amazon_backend_simple.py    # Core analytics engine (ETL pipeline, feature extraction, chart config)
└── README.md                  # Project documentation