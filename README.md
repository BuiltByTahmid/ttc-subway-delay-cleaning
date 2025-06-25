# ttc-subway-delay-cleaning
Cleaning and preparing Toronto's TTC Subway Delay Logs for analysis (2023).
# TTC Subway Delay Data Cleaning 🧹🚇

This project focuses on cleaning and preparing Toronto's TTC Subway Delay Logs for analysis. The raw data comes from the [City of Toronto Open Data portal](https://open.toronto.ca/dataset/ttc-subway-delay-data/) and includes subway delay reports spanning multiple years.

---

## 📌 Objective

To transform messy, inconsistent real-world public transit data into a structured, analysis-ready dataset through data cleaning, validation, and documentation.

---

## 🧱 Raw Data Challenges

- Column formats vary year to year 
- Time stored in 12-hour format
- All station names are uppercase — normalize casing
- Delay codes (`Code`) are non-descriptive and need mapping to real meanings
- `Min Delay` and `Min Gap` include zeros and may have missing or invalid values
- Some station and line values may need cleaning (e.g., trailing/leading spaces)
- Duplicate reports may exist and should be filtered by `Date`, `Time`, `Station`, and `Code`


---

## 🧼 Cleaning Tasks Performed

- Standardized all column names and formats
- Parsed and combined `Date` + `Time` into a full timestamp
- Cleaned and normalized station names and line identifiers
- Mapped numeric delay `Code` to its corresponding description
- Removed duplicate and invalid rows
- Handled missing and negative values in delay durations

---

## 🛠 Tech Stack

- Python 3.11  
- pandas  
- openpyxl  
- pyarrow  
- Great Expectations (for data quality checks)  
- JupyterLab  

---

## 📁 Project Structure


---

## 📦 Output

The cleaned dataset is saved in:
- `data/clean/ttc_delays_clean.parquet`
- `data/clean/ttc_delays_clean_sample.csv` (preview version)

---

## 🔍 Example (Before vs. After)

| Raw Station Entry | Cleaned |
|-------------------|---------|
| `kennedy `        | `Kennedy` |
| `Warden`          | `Warden` |
| `dundas west`     | `Dundas West` |

---

## 📚 Data Source

- [City of Toronto Open Data – TTC Subway Delays](https://open.toronto.ca/dataset/ttc-subway-delay-data/)

---

## 📄 License

This project is licensed under the [MIT License](LICENSE).

---

## 👋 Author

**Mohammed Tahmid**  
[GitHub](https://github.com/BuiltByTahmid) · [LinkedIn](https://www.linkedin.com/) *(Add your real link)*

