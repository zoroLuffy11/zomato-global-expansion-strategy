# 🍽️ Zomato Global Expansion Strategy

**Tools Used:** Advanced Excel · Pivot Tables · VLOOKUP · XLOOKUP · Dynamic Slicers · Dashboards  
**Domain:** Business Intelligence · Market Analysis · Data Analytics  

---

## 📌 Project Objective

Zomato operates across diverse global markets where customer preferences, pricing, and competition vary significantly. Without market-specific insights, expansion decisions risk mispricing and lower customer acceptance.

This project analyzes Zomato's global restaurant dataset across **15 countries and 9,500+ records** to identify the best countries and cities for new restaurant openings, backed entirely by data.

---

## 📂 Files in this Repository

| File | Description |
|------|-------------|
| `Zomato_Global_Expansion_Analysis.xlsx` | Full Excel workbook — raw data, cleaned data, pivot tables, and interactive dashboard |
| `Analysis_Questions_and_Answers.docx` | Detailed written answers to 10 objective analytical questions |
| `Zomato_Expansion_Presentation.pptx` | Management-level presentation summarizing findings and recommendations |

---

## 🧹 Data Cleaning — Issues Identified & Fixed

The raw dataset had 5 major data quality issues that were resolved before analysis:

| Issue | Problem | Solution |
|-------|---------|----------|
| Missing Cuisines | 9 null values, all in USA | Replaced with most frequent USA cuisine (Mexican) using Pivot Table |
| Zero Lat/Long | 498 records with 0 coordinates | Flagged with conditional formatting — not imputed (coordinates are unique) |
| Cost Inconsistency | Values in different currencies + zero costs | Converted all costs to INR using exchange rates; zero values replaced with city-wise average |
| Date Format | `Datekey_Opening` in raw string format (e.g. `2013_9_21`) | Converted to proper date format; extracted Opening Year for time-based analysis |
| City Name Issues | Encoding errors (e.g. `ÛÁstanbul`), extra spaces, mixed case | Cleaned using `PROPER()`, `TRIM()`, and manual correction |

---

## 🔍 Key Analysis Performed

- **Market Saturation:** Counted restaurants by country to identify low-competition markets
- **Price Range Distribution:** Analyzed which price segments are over/under-served globally
- **Price vs Rating Correlation:** Calculated correlation (~0.34) between average cost and customer rating
- **Cuisine Performance:** Identified highest-rated cuisines by country using pivot analysis
- **Service Feature Impact:** Measured how online delivery and table booking affect ratings
- **Country-wise Cost Benchmarking:** Standardized all costs to INR for fair cross-country comparison

---

## 🌍 Recommended Countries for Expansion

| Country | Current Restaurants | Competition | Recommendation |
|---------|-------------------|-------------|----------------|
| Canada | 4 | Low | ✅ Open Immediately |
| Qatar | 20 | Low | ✅ Open Immediately |
| Singapore | 20 | Low | ✅ Open Immediately |
| Australia | 24 | Low-Medium | ✅ Open Immediately |
| Indonesia | 21 | Low | ✅ Open Immediately |
| Philippines | 22 | Low | ✅ Open Immediately |
| Turkey | 34 | Low-Medium | ✅ Consider |
| New Zealand | 40 | Medium | ✅ Consider |
| Sri Lanka | 20 | Low | ✅ Consider |

---

## 💡 Key Findings

- **Price ≠ Rating:** Correlation of ~0.34 — higher price gives only a slight rating boost; quality matters more
- **Online Delivery Gap:** 100% of recommended countries have NO online delivery — first-mover advantage available
- **Table Booking:** Only 7% of restaurants offer it globally — strong differentiator
- **Best Price Segment:** Price Range 3–4 has fewer restaurants but better ratings — less competition, better perception
- **Top Cuisines:** Café, Desserts, Italian, and Chinese consistently score highest in target markets

---

## 📊 Dashboard

The Excel file includes an interactive dashboard with:
- Country and Year slicers for scenario filtering
- Restaurant distribution by country and price range
- Cuisine performance by rating
- Cost vs Rating analysis
- Expansion country recommendations

---

## 🛠️ Excel Features Used

- `VLOOKUP` / `XLOOKUP` for country code mapping
- `PROPER()`, `TRIM()` for city name cleaning
- `DATEVALUE()`, `TEXT()`, `DATE()` for date parsing
- `COUNTIFS()`, `AVERAGEIF()` for conditional aggregation
- Pivot Tables with dynamic slicers
- Conditional formatting for data flagging
- Exchange rate conversion formulas
- `CORREL()` for statistical correlation

---

## 📁 Dataset Source

Newton School of Technology — provided as part of the Data Science certification program.
