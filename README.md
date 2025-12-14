# 🚀 NEO Data Pipeline – NASA API

## 📌 Project Overview
This project implements an **end-to-end data pipeline** to extract, transform, store, and **visualize** information about **Near-Earth Objects (NEOs)** using the **official NASA NeoWs API**.

The workflow covers everything from API consumption to exploratory analysis and data visualization.

---

## 🧠 Technologies
- Python
- Pandas
- Requests
- NASA NeoWs API
- Supabase (PostgreSQL)
- **Looker Studio**
- Google Colab / Jupyter

---

## 📊 Data Source
- **NASA Near-Earth Object Web Service (NeoWs)**
- Real-world asteroid close-approach data (*close approach data*).

### 🗓️ Analysis Period
**December 5, 2025 to December 11, 2025**.

---

## ⚙️ Data Pipeline
1. **Extraction**  
   HTTP requests to the NASA API with proper error handling.

2. **Transformation**  
   Normalization of deeply nested JSON using `pd.json_normalize`, ensuring **one row per close-approach event**.

3. **Load**  
   Data persistence in **Supabase (PostgreSQL)** via REST API.

4. **Analysis & Visualization**  
   Connecting Supabase to **Looker Studio** to build dashboards with metrics such as:
   - Miss Distance
   - Relative Velocity
   - Hazard Classification (PHA)

---

## 📁 CSV Export
The generated CSV contains **all columns and records** from the final DataFrame and is used for:
- Schema validation
- Automatic column creation in Supabase
- Data consistency checks against API-based inserts

---

## 🔐 Security
- No sensitive credentials are versioned
- Keys are configured via environment variables

---

## 🎯 Objective
To demonstrate best practices in **Data Engineering and Data Analysis**, including:
- Public API consumption
- Complex JSON handling
- Database persistence
- Data visualization with Looker Studio
