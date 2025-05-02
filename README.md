# 📚 Open Library  Data Warehouse Design and Implementation 



## 🎯 Project Overview

This project is designed to showcase a simplified data warehouse using **Open Library Book Data**. I implemented an ETL pipeline, designed a star schema, and executed analytical queries to uncover insights from rich metadata involving books, ratings, authors, and editions.

---

## 📦 Dataset Description

The dataset was acquired from [Open Library](https://openlibrary.org/developers/dumps) and includes:

- **Works**: Title, author, subject, revision, etc.
- **Editions**: ISBNs, physical format, publish date
- **Authors**: Names, IDs, and metadata
- **Ratings**: User ratings and rating counts

### 🧾 File Format
- Format: JSON (preprocessed into PostgreSQL-compatible structure)

---

## 📐 Dimensional Modeling: Star Schema

### ⭐ Fact Table
- `fact_book_ratings`: Captures book ratings, related to editions, works, and authors

### 🌟 Dimension Tables
- `dim_editions`
- `dim_works`
- `dim_authors`
- `dim_ratings`

---

---

## 🔄 ETL Process
Developed in **Python** using `pandas`, `json`, and `sqlalchemy`, the ETL pipeline:
- Extracts JSON dump data
- Transforms and cleans inconsistencies (dates, nulls, lists)
- Loads the data into **PostgreSQL**

Implemented in **Python** using:
- `pandas` for data wrangling
- `sqlalchemy` for database connection
- `json` for parsing
- ETL stages: extraction, cleaning, date parsing, relationship normalization

---
Code is modular and includes exception handling and inline documentation.

## 📊 OLAP Operations Performed
- Roll-Up: Aggregating data from detailed to summary levels.
- Drill-Down: Breaking down data into finer levels of detail.
- Slice: Filtering data based on a single dimension.
- Dice: Filtering data across multiple dimensions.
- Pivot: Transforming rows into columns for better insights.



| OLAP Operation | Sample Examples |
|----------------|-------------|
| Roll-Up        | Count books published per year |
| Drill-Down     | Monthly publication breakdown |
| Slice          | Filter books by year or format |
| Dice           | Filter by multiple dimensions (e.g., year + format) |
| Pivot          | Display rating distribution (1–5) as columns |



## 📈 Visualizations

Generated using **Matplotlib**:
- Bar graph: Books published annually
- Pie chart: Distribution of ratings

---

## 📥 Installation

```bash
git clone https://github.com/Haile-12/Open-Library-Data-Warehouse.git
cd Open-Library-Data-Warehouse
```

Install required Python libraries and PostgreSQL.

---
## 📥 Usage


After setting up the database, you can execute the SQL queries provided in the sql codes to perform analyses on the data. Additionally, Python and Matplotlib can be used for data visualization to gain insights from the dataset.



## 🔍 Sample Findings

- Publications surged after 2016
- Most books are rated 3 or higher
- Paperback is the dominant format
- Some authors have significantly more publications

---

## 🤝 Contribution

Feel free to fork and contribute. you are welcome!

---

## ⚖ License

This project is under the **MIT License**. See the `LICENSE` file for details.

---

## 🙏 Acknowledgments


I would like to express my gratitude to [Open Library](https://openlibrary.org/)  for providing the dataset  to complete this project.



---

📫 Fore more info  Contact: hailetassew4545@gmail.com | +251 945 987 335
