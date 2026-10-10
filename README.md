# Zomato Restaurant Data Analytics Using Python and AI

**Academic Internship Project**

---

## 📋 Table of Contents

1. [Project Overview](#project-overview)
2. [Problem Statement](#problem-statement)
3. [Project Objectives](#project-objectives)
4. [Dataset](#dataset)
5. [Technologies Used](#technologies-used)
6. [Project Folder Structure](#project-folder-structure)
7. [Installation Instructions](#installation-instructions)
8. [How to Run the Notebook](#how-to-run-the-notebook)
9. [Analyses and Visualizations](#analyses-and-visualizations)
10. [Key Findings](#key-findings)
11. [Limitations](#limitations)
12. [Future Improvements](#future-improvements)

---

## Project Overview

This project performs end-to-end exploratory data analysis (EDA) and machine learning on the Zomato Restaurant dataset. It uncovers patterns in restaurant ratings, cuisines, pricing, online delivery adoption, and geographic distribution across 15 countries. An AI component — a Random Forest classifier — predicts whether a restaurant will be rated highly or poorly based on its features.

---

## Problem Statement

The food-tech industry generates large volumes of restaurant data, yet actionable insights are often buried. Key questions remain unanswered:

- Why do some restaurants receive poor ratings while others excel?
- Which factors (price, delivery, cuisine, location) most influence customer satisfaction?
- Can we predict a restaurant's rating category before it accumulates enough reviews?

This project addresses these questions using real-world Zomato data.

---

## Project Objectives

1. Perform data quality checks and clean the raw dataset.
2. Explore restaurant distribution by country, city, and cuisine type.
3. Analyze the relationship between price range, online delivery, table booking, and aggregate ratings.
4. Identify the most popular cuisines globally.
5. Investigate the correlation between votes, cost, and ratings.
6. Build and evaluate an AI model to classify restaurants as high- or low-rated.
7. Derive actionable business recommendations from the findings.

---

## Dataset

### Source

The dataset is the publicly available **Zomato Restaurant Dataset** from Kaggle:

> **Kaggle:** [https://www.kaggle.com/datasets/shrutimehta/zomato-restaurants-data](https://www.kaggle.com/datasets/shrutimehta/zomato-restaurants-data)

### File

| Property | Value |
|---|---|
| File name | `Zomato Restaurant Dataset.csv` |
| Format | CSV (UTF-8 with BOM) |
| Rows | 9,551 |
| Columns | 21 |

### Column Descriptions

| Column | Description |
|---|---|
| `Restaurant ID` | Unique numeric identifier for each restaurant |
| `Restaurant Name` | Name of the restaurant |
| `Country Code` | Numeric code representing the country (mapped to country names in the notebook) |
| `City` | City where the restaurant is located |
| `Address` | Full street address |
| `Locality` | Neighbourhood or locality name |
| `Locality Verbose` | Locality and city combined |
| `Longitude` | Geographic longitude coordinate |
| `Latitude` | Geographic latitude coordinate |
| `Cuisines` | Comma-separated list of cuisine types served |
| `Average Cost for two` | Average dining cost for two people (in local currency) |
| `Currency` | Local currency name and symbol |
| `Has Table booking` | Whether the restaurant accepts table reservations (Yes/No) |
| `Has Online delivery` | Whether the restaurant offers online delivery (Yes/No) |
| `Is delivering now` | Whether the restaurant is currently delivering (Yes/No) |
| `Switch to order menu` | Whether the switch-to-order-menu option is available (Yes/No) |
| `Price range` | Ordinal scale from 1 (budget) to 4 (premium) |
| `Aggregate rating` | Overall rating score from 0.0 to 5.0 |
| `Rating color` | Color label associated with the rating band |
| `Rating text` | Text label: Excellent / Very Good / Good / Average / Poor / Not rated |
| `Votes` | Total number of user votes/reviews received |

---

## Technologies Used

| Technology | Purpose |
|---|---|
| Python 3.x | Core programming language |
| Pandas | Data loading, cleaning, and manipulation |
| NumPy | Numerical operations |
| Matplotlib | Base charting and plot customization |
| Seaborn | Statistical visualizations |
| scikit-learn | Machine learning (Random Forest, encoding, evaluation) |
| Jupyter Notebook | Interactive development environment |

---

## Project Folder Structure

```
Umesh_kumar_gupta_projects_dataanaytics/
│
├── Zomato Restaurant Dataset.csv   # Raw dataset file
├── Umesh_Data_Analytics.ipynb      # Main Jupyter Notebook
├── requirements.txt                # Python package dependencies
└── README.md                       # This file
```

---

## Installation Instructions

### Prerequisites

- Python 3.8 or higher installed on your system
- pip (Python package manager)
- Jupyter Notebook or JupyterLab

### Step 1 — Clone or Download the Project

Download the project folder to your local machine and open a terminal (or Command Prompt / PowerShell) inside the project directory.

### Step 2 — Install Dependencies from requirements.txt

Run the following command to install all required Python libraries at once:

```bash
pip install -r requirements.txt
```

This will install:

```
pandas
numpy
matplotlib
seaborn
scikit-learn
```

### Step 3 — Install Jupyter Notebook (if not already installed)

```bash
pip install notebook
```

---

## How to Run the Notebook

### Option 1 — Classic Jupyter Notebook

```bash
jupyter notebook
```

This opens a browser tab. Navigate to `Umesh_Data_Analytics.ipynb` and click to open it.

### Option 2 — JupyterLab

```bash
jupyter lab
```

### Option 3 — VS Code

Open the project folder in VS Code. Install the **Jupyter** extension, then open `Umesh_Data_Analytics.ipynb` directly.

### Running All Cells

Once the notebook is open:

1. Click **Kernel → Restart & Run All** (Jupyter Notebook)  
   or **Run → Run All Cells** (JupyterLab / VS Code)
2. The notebook runs from top to bottom without requiring any manual changes.
3. All charts and outputs will appear inline below each cell.

> **Note:** Make sure `Zomato Restaurant Dataset.csv` is in the **same folder** as the notebook before running.

---

## Analyses and Visualizations

The notebook is organized into 8 sections:

| Section | Analysis | Chart Type |
|---|---|---|
| 3 | Data quality checks: missing values, duplicates, data types | Table output |
| 4 | Data cleaning: country mapping, Yes/No encoding, type casting | — |
| 5.1 | Restaurants per country | Horizontal bar chart |
| 5.2 | Top 15 cities by restaurant count | Horizontal bar chart |
| 5.3 | Rating distribution — histogram + category breakdown | Histogram + Pie chart |
| 5.4 | Price range vs. aggregate rating | Box plot |
| 5.5 | Online delivery and table booking availability + rating impact | Pie charts + Box plot |
| 5.6 | Top 20 most common cuisines | Horizontal bar chart |
| 5.7 | Votes vs. rating relationship | Scatter plot |
| 5.8 | Online delivery rate by country | Horizontal bar chart |
| 5.9 | Average rating by country | Bar chart |
| 5.10 | Average cost for two by country (local currency) | Bar chart |
| 5.11 | Price range distribution | Bar chart |
| 6 | Correlation heatmap of numeric features | Heatmap |
| 7 | ML: Random Forest classifier + confusion matrix + feature importance | Confusion matrix + Bar chart |

---

## Key Findings

These findings are drawn directly from the dataset analysis:

1. **India dominates the dataset** — 8,652 out of 9,551 restaurants (~90.6%) are from India, making it the primary market represented.

2. **22.5% of restaurants are unrated** — 2,148 restaurants have an aggregate rating of 0.0, indicating a significant engagement gap where customers have not yet submitted reviews.

3. **Budget restaurants are most common** — Price range 1 (budget) accounts for 46.6% of all restaurants (4,444 records), followed by mid-range at 32.6%.

4. **Higher price range correlates with higher ratings** — Premium restaurants (price range 4) consistently receive higher aggregate ratings than budget restaurants.

5. **Online delivery is largely an India-only feature** — Most non-India countries on the platform show near-zero online delivery adoption.

6. **North Indian, Chinese, and Fast Food are the top 3 cuisines** — These dominate the cuisine listings, driven largely by the India-heavy dataset.

7. **Votes and ratings are positively correlated** — Restaurants with more user votes tend to have higher ratings, suggesting that active community engagement drives better scores.

8. **The Random Forest ML classifier successfully distinguishes high- vs low-rated restaurants**, with `Votes` and `Price range` being the most predictive features for rating category classification.

---

## Limitations

1. **India-heavy data** — With ~90.6% of records from India, findings for other countries (Australia, Brazil, UK, etc.) are based on a small sample and may not be statistically representative.

2. **Currency not normalized** — `Average Cost for two` is recorded in local currencies. Cross-country cost comparisons are not meaningful without currency conversion or purchasing-power-parity adjustment.

3. **22.5% unrated restaurants** — These records are excluded from the ML model and rating-based analyses, which could introduce selection bias.

4. **Static snapshot** — The dataset represents a single point in time. Restaurant ratings, delivery options, and operational status may have changed since the data was collected.

5. **No temporal data** — There are no date or timestamp columns, so trends over time (e.g., rating changes, growth in delivery adoption) cannot be analyzed.

6. **Multi-label cuisines not modeled** — Cuisines are comma-separated strings. The ML model does not use cuisine as a feature due to the complexity of multi-label encoding for a beginner-friendly scope.

---

## Future Improvements

1. **Add currency normalization** — Convert `Average Cost for two` to a common currency (e.g., USD) using exchange rate data to enable fair cross-country cost comparisons.

2. **Expand the ML model** — Include cuisine type as a feature using multi-hot encoding or TF-IDF, and experiment with XGBoost or LightGBM for better accuracy.

3. **Add geographic map visualization** — Use `Latitude` and `Longitude` columns with Folium or Plotly to create an interactive map of restaurant density.

4. **Time-series analysis** — Incorporate a date column (if available in future versions) to analyze rating trends and delivery growth over time.

5. **Deploy as a web app** — Wrap the ML model in a simple Streamlit or Flask interface so users can input restaurant attributes and receive a predicted rating category.

6. **Sentiment analysis** — If review text data becomes available, apply NLP techniques to extract customer sentiment and enrich the rating prediction model.

7. **Address class imbalance** — Apply SMOTE or class-weight adjustments in the ML model to improve precision and recall for the minority class (Poor-rated restaurants).

---

*Project by Umesh Kumar Gupta | Academic Internship — Data Analytics with AI*