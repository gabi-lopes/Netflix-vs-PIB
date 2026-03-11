# 🎬 Real-World Data Wrangling: Netflix & Global GDP Analysis

This project applies real-world data wrangling techniques to gather, clean, and analyze two datasets — one about **Netflix Movies and TV Shows** and another about **Global GDP** from the World Bank API.  
The main goal is to explore the relationship between a country's **economic power** (GDP) and its **media production** level.

---

## 📊 Project Overview

In this project, I applied the skills acquired in data wrangling to:
- Retrieve and extract data using different methods (manual download and API access).
- Assess and clean the data programmatically.
- Store and merge datasets for further analysis.
- Visualize and interpret correlations using Python.

---

## 📁 Datasets

### Dataset 1 — Netflix Titles
- **Type:** CSV File (manually downloaded from Kaggle)
- **Description:** Contains details about Netflix movies and TV shows.
- **Variables:**
  - `type`: Movie or TV Show  
  - `title`: Title of the production  
  - `director`: Director's name  
  - `cast`: List of actors  
  - `country`: Country of origin  
  - `release_year`: Year of release  
  - `rating`: Age rating  
  - `duration`: Duration (minutes or seasons)  

📈 This dataset allows exploration of media production patterns by country.

---

### Dataset 2 — Global GDP
- **Type:** JSON data from **World Bank API**
- **Method:** Data retrieved programmatically using the World Bank’s open API.  
- **Variables:**
  - `Country`: Name of the country  
  - `Year`: Year of observation  
  - `GDP (US$)`: Total GDP in current US dollars  

🌍 This dataset provides economic context to compare with the Netflix data.

---

## 🧠 Research Question

> Is there a relationship between a country's GDP and its media production (number of Netflix titles)?

---

## ⚙️ Steps & Methods

1. **Data Gathering**
   - Netflix data manually downloaded from Kaggle.
   - GDP data collected using the World Bank API via `requests`.

2. **Data Assessment**
   - Checked data completeness, column consistency, and missing values.
   - Verified each dataset had >500 samples and at least 2 variables.

3. **Data Cleaning**
   - Standardized column names and country identifiers.
   - Removed nulls and irrelevant records.

4. **Data Merging**
   - Combined datasets by matching countries.
   - Counted the number of Netflix titles per country and merged with GDP data.

5. **Data Analysis**
   - Computed the correlation between GDP and number of titles.
   - Visualized results using **Seaborn heatmaps**.

---

## 📉 Visualization Example

The correlation between GDP and film production was visualized using a **heatmap**:

![Correlation Heatmap](https://img.shields.io/badge/Seaborn-Heatmap-blue?logo=python&style=flat-square)

> The heat map shows a positive correlation between GDP and media production.  
> Countries with higher GDP tend to produce (or appear in) more Netflix titles.

---

## 🧩 Technologies Used

| Category | Libraries / Tools |
|-----------|------------------|
| Data manipulation | `pandas`, `numpy` |
| Data visualization | `matplotlib`, `seaborn` |
| Data retrieval | `requests`, `BeautifulSoup` |
| Machine learning (optional) | `scikit-learn` |
| Database interaction | `SQLAlchemy` |
| Image handling | `Pillow` |

---

## 🧪 How to Run

```bash
# 1. Install dependencies
pip install numpy pandas matplotlib requests seaborn scikit-learn SQLAlchemy beautifulsoup4 pillow openpyxl

# 2. Run the notebook
jupyter notebook data_wrangling_project.ipynb
