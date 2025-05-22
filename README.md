
# 🏅 Tokyo Olympics 2020 Dashboard — End-to-End Data Engineering with Azure & Power BI

## 🎯 Project Overview
This project demonstrates how to build a **production-ready, full-stack Olympic Dashboard** using **Azure Data Engineering tools** and **Power BI**. The primary objective was to simulate real-world enterprise data workflows using the **Medallion Architecture**, incorporating scalable ingestion, transformation, and visualization of Tokyo 2020 Olympics data.

> 🔍 **Goal**: Build an end-to-end data pipeline — from raw ingestion to beautiful insights — using cloud-native tools in Azure and Power BI.

---

## 🧱 Architecture Used – Medallion Architecture on Azure

The project follows the **Medallion Architecture** pattern — Bronze (Raw), Silver (Cleaned), and Gold (Business-ready) — implemented via the following Azure services:

### 🔹 1. Data Ingestion – *Azure Data Factory (ADF)*
- **Source**: Olympic Web API (JSON/CSV).
- **Task**: Ingest raw data (medals, countries, athletes).
- **Output**: Stored in **Bronze layer** in Azure Data Lake Gen2.

### 🔹 2. Data Storage – *Azure Data Lake Gen2*
Structured into three zones:
- **Bronze** – Raw untouched data as received from the API.
- **Silver** – Cleaned, deduplicated, and schema-aligned datasets.
- **Gold** – Business-ready metrics like:
  - Total medals by country
  - Gender-based participation
  - Event participation trends

### 🔹 3. Data Processing – *Azure Databricks (PySpark)*
- Ingested Bronze layer files into Databricks notebooks.
- Applied:
  - Schema validation
  - Null handling
  - Aggregations and joins
- Saved processed data to **Silver & Gold zones**.

### 🔹 4. Data Visualization – *Power BI*
- Connected directly to Gold zone datasets.
- Developed a **dark-themed** interactive dashboard using:
  - KPI Cards
  - Maps
  - Bar charts
  - Pie charts
  - Slicers and tooltips

---

## 📊 Dashboard Features

| Feature | Description |
|--------|-------------|
| 🌍 **Interactive Map** | Heatmap of medal-winning countries |
| 🥇 **KPI Cards** | Total medals (Gold, Silver, Bronze), Teams, and Athletes |
| 📊 **Bar Charts** | Medal counts by country |
| 🧑‍🤝‍🧑 **Gender Insights** | Gender distribution by events |
| 📅 **Event Participation** | Discipline-wise breakdown with gender split |

---

## 💡 Key Learnings

- ✅ Designed and orchestrated scalable ETL pipelines in **ADF**
- ✅ Applied **Medallion Architecture** for modular data processing
- ✅ Developed efficient **PySpark** notebooks in **Azure Databricks**
- ✅ Leveraged **Azure Data Lake Gen2** for multi-layer storage
- ✅ Built dynamic **Power BI** dashboards for real-time insights

---

## 🔍 Folder Structure

```
📁 olympics-dashboard/
├── 📂 notebooks/              # PySpark notebooks for ETL
├── 📂 powerbi/                # PBIX file and screenshots
├── 📂 pipeline-templates/     # ADF pipeline JSON templates
├── 📂 data-samples/           # Sample raw & transformed data
├── 📜 README.md               # This file
```

---

## 🚀 How to Run Locally

### Pre-requisites
- Azure Subscription (with ADF, Data Lake, and Databricks)
- Power BI Desktop
- Web API or dataset (public Olympic dataset)

### Steps
1. **Ingest Data with ADF**  
   Set up ADF pipeline using provided JSON template or GUI.

2. **Create Zones in ADLS Gen2**  
   - `/bronze/olympics/raw_data/`  
   - `/silver/olympics/cleaned/`  
   - `/gold/olympics/metrics/`  

3. **Process with PySpark in Databricks**  
   - Use `notebooks/bronze_to_silver.ipynb` and `silver_to_gold.ipynb`

4. **Visualize in Power BI**  
   - Load `powerbi/dashboard.pbix`
   - Connect to ADLS Gen2 via Azure Data Lake connector.

---

## 📌 Project Objectives Met

- ✅ Applied cloud-native tools for modern data engineering
- ✅ Demonstrated multi-layer architecture for data lakes
- ✅ Created an accessible and informative BI dashboard
- ✅ Simulated enterprise-level data flow with real-world relevance

---

## 🙌 Acknowledgments

- Tokyo Olympics 2020 datasets (open data)
- Microsoft Azure for student credits
- Databricks Community Edition
- Power BI for real-time visualization tools

---

## 📫 Let's Connect!

If you'd like to collaborate or have feedback:

**👨‍💻 Himanshu Rathod**  
Data Engineer | Cloud Analytics Enthusiast  
🔗 [LinkedIn](https://www.linkedin.com/in/himanshurathod1047)  
🌐 [Dribbble](https://dribbble.com/himan_1047)
