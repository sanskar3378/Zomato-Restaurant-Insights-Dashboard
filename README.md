# 🍽️ Zomato Restaurant Insights Dashboard

A comprehensive data analysis and visualization platform for exploring Zomato restaurant data. This project combines exploratory data analysis (EDA), statistical insights, and interactive dashboards to uncover restaurant trends, ratings patterns, cuisine preferences, and delivery metrics.

---

## 📋 Project Overview

This repository contains a complete end-to-end solution for analyzing Zomato restaurant data using multiple visualization and analysis techniques. The project includes:

- **Data Cleaning & Preprocessing**: Jupyter Notebook-based data cleaning pipeline
- **Statistical Analysis**: Comprehensive EDA with quantitative insights
- **Interactive Dashboard**: Power BI dashboard for visual exploration
- **Research Document**: Detailed case study with findings and recommendations

### Key Metrics Analyzed
- Restaurant ratings and customer satisfaction (vote patterns)
- Cost analysis for different restaurant types
- Online ordering vs. table booking capabilities
- Cuisine preferences and restaurant classifications
- Price segments and service offerings

---

## 📊 Dashboard Preview

The Power BI dashboard (`zomato_dashboard.pbix`) provides interactive visualizations including:

- **Restaurant Performance Metrics**: Rating distributions, top-rated restaurants
- **Cost Analysis**: Price segments, cost vs. rating correlations
- **Service Offerings**: Online ordering adoption, table booking availability
- **Cuisine Analytics**: Popular cuisines, cuisine diversity
- **Customer Engagement**: Vote counts, customer preference patterns
- **Restaurant Classification**: Distribution by type (Buffet, Delivery, Dine-out, etc.)

*Note: View the `.pbix` file in Power BI Desktop for full interactive functionality*

---

## 📂 Repository Structure

```
Zomato-Restaurant-Insights-Dashboard/
├── README.md                          # Project documentation
├── zomato_data.ipynb                  # Data cleaning notebook
├── Zomato_data.csv                    # Original dataset (148 restaurants)
├── zomato_data_cleaned.csv            # Processed dataset
├── zomato_dashboard.pbix              # Power BI interactive dashboard
├── zomato_case_study.pdf              # Detailed case study & analysis
└── (Solution files)                   # Analysis scripts & outputs
```

---

## 📊 Dataset Information

### Dataset Specifications
- **Records**: 148 restaurants
- **Features**: 7 columns
- **Data Quality**: No missing values (100% complete dataset)

### Column Descriptions

| Column | Type | Description |
|--------|------|-------------|
| `name` | String | Restaurant name |
| `online_order` | Boolean | Whether restaurant accepts online orders (Yes/No) |
| `book_table` | Boolean | Whether restaurant allows table reservations (Yes/No) |
| `rate` | Float | Customer rating (0-5 scale) |
| `votes` | Integer | Number of customer votes/reviews |
| `approx_cost(for two people)` | Float | Estimated cost for two people (in local currency) |
| `listed_in(type)` | String | Restaurant type (Buffet, Delivery, Dine-out, etc.) |

### Data Sample
```
name                       online_order  book_table  rate  votes  cost  type
Jalsa                      Yes           Yes        4.1   775    800   Buffet
Spice Elephant             Yes           No         4.1   787    800   Buffet
San Churro Cafe            Yes           No         3.8   918    800   Buffet
Addhuri Udupi Bhojana      No            No         3.7   88     300   Buffet
Grand Village              No            No         3.8   166    600   Buffet
```

---

## 🔧 Setup & Installation

### Prerequisites
- Python 3.7+
- Power BI Desktop (for dashboard viewing)
- Jupyter Notebook

### Required Libraries
```bash
pip install pandas numpy matplotlib seaborn scipy plotly jupyter
```

### Quick Start

1. **Download the dataset** (if needed):
   ```bash
   # Dataset is included as Zomato_data.csv
   # Alternative source: https://media.geeksforgeeks.org/wp-content/uploads/20250117023324808265/Zomato-data-.csv
   ```

2. **Install dependencies**:
   ```bash
   pip install pandas numpy matplotlib seaborn scipy plotly
   ```

3. **Run the data cleaning notebook**:
   ```bash
   jupyter notebook zomato_data.ipynb
   ```
   This will generate `zomato_data_cleaned.csv`

4. **Explore the Power BI Dashboard**:
   - Open `zomato_dashboard.pbix` in Power BI Desktop
   - Interact with filters and visualizations
   - Export reports as needed

---

## 📈 Key Insights & Analysis

### Data Cleaning Process
- Converted rating column from "X.X/5" format to numeric values
- Converted cost column to float for numerical analysis
- Validated data completeness (0 null values confirmed)
- Generated cleaned dataset for further analysis

### Analysis Highlights
The notebook performs:
- ✅ Descriptive statistics on ratings, costs, and votes
- ✅ Categorical analysis of restaurant types and services
- ✅ Distribution analysis of customer engagement
- ✅ Correlation analysis between features
- ✅ Price segmentation analysis
- ✅ Service adoption metrics

---

## 📊 Dashboard Features

### Interactive Visualizations
- **Rating Distribution Charts**: Histogram of restaurant ratings
- **Cost Analysis**: Box plots and scatter plots showing price patterns
- **Service Adoption**: Pie charts for online ordering and table booking
- **Top Restaurants**: Ranked lists by ratings and customer votes
- **Cuisine Distribution**: Word clouds or bar charts for cuisine types
- **Slicers & Filters**: Dynamic filtering by restaurant type, price range, and service type

### Power BI Capabilities
- Drill-down analysis for detailed exploration
- Cross-filtering across multiple visualizations
- Interactive tooltips with detailed information
- Custom measures and calculated columns
- Export functionality for reports and presentations

---

## 🔍 Questions Addressed

This analysis provides answers to:
1. What is the average rating of restaurants?
2. How does cost correlate with customer ratings?
3. What percentage of restaurants offer online ordering?
4. Which restaurant types are most popular?
5. What is the price range for different restaurant categories?
6. How engaged are customers (based on vote counts)?
7. Are table booking options common?
8. Which cuisines have the highest ratings?
9. What is the relationship between service offerings and ratings?
10. How does customer satisfaction vary by price segment?

---

## 📄 Case Study

Detailed analysis and findings are documented in `zomato_case_study.pdf`, including:
- Problem statement and business context
- Methodology and data approach
- Comprehensive findings and patterns
- Statistical summaries and conclusions
- Recommendations for restaurant businesses
- Visual presentations of key metrics

---

## 🛠️ Tools & Technologies

| Component | Technology |
|-----------|-----------|
| Data Processing | Python, Pandas, NumPy |
| EDA & Visualization | Matplotlib, Seaborn, Plotly |
| Interactive Dashboard | Power BI |
| Notebook Environment | Jupyter |
| Data Format | CSV |

---

## 📌 How to Use This Repository

### For Data Analysis:
1. Open `zomato_data.ipynb` in Jupyter
2. Follow the cells to understand data cleaning procedures
3. Modify and extend the analysis as needed

### For Business Intelligence:
1. Open `zomato_dashboard.pbix` in Power BI Desktop
2. Explore interactive visualizations
3. Use slicers to filter data by restaurant type, price, and services
4. Generate reports and export insights

### For Academic/Research:
1. Review `zomato_case_study.pdf` for comprehensive documentation
2. Use the cleaned dataset `zomato_data_cleaned.csv` for further analysis
3. Adapt the methodology for similar restaurant datasets

---

## 📝 Data Processing Summary

**Input**: `Zomato_data.csv` (raw data)
```python
# Data Types Before Processing:
- name: object
- online_order: object
- book_table: object
- rate: object (string format "X.X/5")
- votes: int64
- approx_cost: int64
- listed_in(type): object
```

**Output**: `zomato_data_cleaned.csv` (processed data)
```python
# Data Types After Processing:
- name: object
- online_order: object
- book_table: object
- rate: float64 ✓ (converted from string)
- votes: int64
- approx_cost: float64 ✓ (converted to float)
- listed_in(type): object
```

---

## 🎯 Potential Extensions

- Sentiment analysis on customer reviews
- Machine learning for rating prediction
- Geolocation-based analysis
- Time series analysis for trends
- Recommendation system for restaurants
- Price optimization analysis
- Customer segmentation clustering

---

## 📧 Questions & Contributions

For questions about the analysis or to contribute improvements:
1. Review the existing documentation
2. Check the Power BI dashboard for visual insights
3. Explore the Jupyter notebook for detailed code
4. Refer to the case study for comprehensive findings

---

## 📜 License

This project is provided for educational and analytical purposes.

---

## 🙏 Acknowledgments

- Dataset source: GeeksforGeeks
- Analysis methodology based on exploratory data analysis best practices
- Power BI for interactive visualization capabilities
- Python data science ecosystem (Pandas, Matplotlib, Seaborn)

---

**Last Updated**: October 2026  
**Repository Owner**: sanskar3378  
**Project Status**: ✅ Complete with comprehensive analysis and visualizations
