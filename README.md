# 🚖 Uber Real-Time Data Engineering Project

![Python](https://img.shields.io/badge/Python-3.10+-blue?style=for-the-badge&logo=python)
![Azure](https://img.shields.io/badge/Azure-Cloud-0078D4?style=for-the-badge&logo=microsoftazure)
![Databricks](https://img.shields.io/badge/Databricks-Platform-FF3621?style=for-the-badge&logo=databricks)
![PySpark](https://img.shields.io/badge/PySpark-Distributed-E25A1C?style=for-the-badge&logo=apachespark)

> End-to-end real-time data engineering pipeline built on Uber trip data using **Python**, **Azure**, and **Databricks**. Covers data ingestion, transformation, and analytics with star schema data modeling and dashboard visualization.

---


---

## 🏗️ Project Architecture

![Architecture](architecture.png)

---

## 🛠️ Tech Stack

| Technology | Usage |
|------------|-------|
| **Python** | Data processing & scripting |
| **Azure Data Lake Storage** | Raw data storage |
| **Azure Blob Storage** | File storage layer |
| **Databricks** | Distributed data processing platform |
| **PySpark** | Large-scale data transformation |
| **SQL** | Analytical queries & reporting |
| **Jupyter Notebook** | Exploration & development |

---

## 📂 Project Structure

```
Uber_Data_Engineer_Project/
│
├── Code_Files/          # PySpark transformation scripts
├── Data/                # Raw Uber trip dataset
├── templates/           # Reusable pipeline templates
├── api.py               # API connection layer
├── connection.py        # Azure & Databricks connection setup
├── data.py              # Data loading utilities
├── architecture.png     # Project architecture diagram
└── README.md
```

---

## 🔄 Pipeline Overview

```
Raw Data → Azure Blob Storage → Databricks (PySpark ETL) → Star Schema → Analytics
```

1. **Ingestion** — Raw Uber trip data is loaded and stored in **Azure Blob Storage / Data Lake**
2. **Transformation** — Data is cleaned and transformed using **PySpark on Databricks**
3. **Modeling** — Data is structured using a **Star Schema** (fact & dimension tables)
4. **Analytics** — SQL queries are run on structured data to generate business insights
5. **Visualization** — Key metrics like trip trends, fare analysis, and demand patterns are visualized

---

## 📊 Data Model (Star Schema)

```
              ┌──────────────────┐
              │    fact_trips    │
              └────────┬─────────┘
                       │
       ┌───────────────┼───────────────┐
       ▼               ▼               ▼
dim_datetime      dim_location     dim_payment
```

**Fact Table:**
- `fact_trips` — trip_id, datetime_id, pickup_location_id, dropoff_location_id, payment_type_id, fare_amount, tip_amount, total_amount

**Dimension Tables:**
- `dim_datetime` — hour, day, month, year, weekday
- `dim_location` — latitude, longitude, borough, zone
- `dim_payment` — payment_type_name

---

## 🚀 How to Run

### Prerequisites
- Python 3.10+
- Azure account (Blob Storage / Data Lake Gen2)
- Databricks workspace

### Steps

```bash
# 1. Clone the repository
git clone https://github.com/Ajinkya49/uber-data-engineer-project-
cd Uber_Data_Engineer_Project

# 2. Install dependencies
pip install -r requirements.txt

# 3. Configure Azure connection
# Update connection.py with your Azure credentials

# 4. Run the pipeline
python data.py
```

---

## 📈 Key Insights Generated

- 🕐 Trip demand trends across hours, days, and months
- 💰 Fare and tip analysis by distance and trip type
- 📍 Pickup & dropoff hotspot identification
- 👥 Passenger count distribution
- 🔝 Peak hours and high-demand zones


---

## ⭐ Support

If you found this project helpful, please consider giving it a ⭐ on GitHub — it means a lot!
