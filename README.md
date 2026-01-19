# SIT220 - Data Wrangling

**Course:** SIT220 - Data Wrangling  

---

## 📚 Project Overview

This repository contains a comprehensive collection of data analysis tasks completed as part of the SIT220 Data Wrangling course. The project demonstrates proficiency in data manipulation, statistical analysis, and visualization using Python libraries including NumPy, Pandas, Seaborn, and Matplotlib.

---

## 📁 Project Structure

```
SIT220/
├── task1p/              # NumPy Vectors - BTC-USD Analysis
├── task2p/              # NYC Weather Data Analysis
├── task3p/              # NYC Flights Data Analysis
├── task4p/              # Pandas DataFrames - Melbourne Tram Data
├── task5c/              # Challenge Task 5
├── task6c/              # Text Analysis Challenge
└── README.md           # This file
```

---

## 🔬 Task Descriptions

### Task 1P: Working with NumPy Vectors (Unidimensional Data)
**Focus:** BTC-USD Daily Closing Prices for 2023

**Dataset:** `BTC-to-USD.csv` (Yahoo Finance data)

**Key Activities:**
- Loaded BTC-USD daily closing prices for 2023 using NumPy's `genfromtxt`
- Analyzed Q3 2023 data (days 182-273)
- Computed summary statistics without explicit loops:
  - Arithmetic mean, minimum, maximum
  - Quartiles (Q1, median, Q3)
  - Standard deviation and IQR
- Identified days with lowest and highest prices
- Visualized Q3 price evolution using Matplotlib

**Key Findings:**
- 365 daily observations for 2023
- Q3 showed significant volatility with mid-quarter dip
- Demonstrated efficient vectorized operations in NumPy

---

### Task 2P: NYC Weather Data Analysis
**Focus:** Hourly Weather Data from NYC Airports (2013)

**Dataset:** `nycflights13_weather.csv` (26,130 hourly observations)

**Airports Analyzed:** EWR, JFK, LGA

**Key Activities:**
- Converted all measurements to SI units:
  - Temperature: Fahrenheit → Celsius
  - Precipitation: inches → mm
  - Visibility: miles → meters
  - Wind speed: mph → m/s
- Calculated daily mean wind speeds for LaGuardia Airport (LGA)
- Generated 364 daily wind speed averages
- Created time-series visualization of wind patterns
- Identified seasonal trends and variability

**Technical Approach:**
- Used vectorized NumPy operations for unit conversions
- Implemented efficient grouping using `unique` and `bincount`
- No explicit loops in calculations

---

### Task 3P: NYC Flights Data Analysis
**Focus:** Comprehensive Flight Data Analysis (2013)

**Datasets:**
- `nycflights13_flights.csv` (336,776 flights)
- `nycflights13_weather.csv`
- `nycflights13_airports.csv`
- `nycflights13_airlines.csv`
- `nycflights13_planes.csv`

**Key Activities:**
- Analyzed carrier performance (delays, cancellations)
- Examined seasonal flight patterns
- Investigated weather impacts on operations
- Created comprehensive visualizations with Seaborn
- Merged multiple datasets for integrated analysis

**Insights Provided:**
- Carrier reliability comparisons
- Peak travel periods identification
- Weather-delay correlations
- Airport operational efficiency

---

### Task 4P: Working with Pandas DataFrames (Heterogeneous Data)
**Focus:** Melbourne Tram Network Analysis (2017)

**Datasets:**
- `myki_2017_top20_tram_routes_ScanOnTransaction.csv` (1,904,721 records)
- `myki_2017_top20_tram_routes_ScanOffTransaction.csv` (611,293 records)
- `stop_locations.txt` (27,614 stops)

**Key Activities:**
- Merged touch-on and touch-off transaction data
- Linked stop information (names, locations) to transactions
- Identified top 10 busiest tram stops by average daily touch-ons
- Analyzed routes with highest passenger activity
- Calculated average travel times by route
- Created horizontal bar charts with Seaborn

**Top Findings:**
- Melbourne University/Swanston St: busiest stop (173.5 daily touch-ons)
- Flinders Street Railway Station: 128.8 daily touch-ons
- Federation Square/Swanston St: 114.4 daily touch-ons

**Technical Implementation:**
- Pandas DataFrame operations (merge, groupby, aggregate)
- Efficient data joining using multiple keys
- Professional data visualization techniques

---

### Task 5C: Challenge Task
**Focus:** Advanced data manipulation and analysis techniques

**Status:** Completed with advanced statistical methods and visualization techniques

---

### Task 6C: Text Analysis Challenge
**Focus:** Stack Overflow Data Analysis

**Datasets:**
- `Posts.csv`
- `Comments.csv`
- `Tags.csv`
- `Votes.csv`

**Key Activities:**
- Natural language processing on technical posts
- Sentiment and topic analysis
- User engagement patterns
- Tag distribution analysis
- Community interaction metrics

---

## 🛠️ Technologies & Libraries

### Core Technologies
- **Python 3.12.4**
- **Jupyter Notebook**

### Primary Libraries
```python
import numpy as np              # Numerical computing
import pandas as pd             # Data manipulation
import matplotlib.pyplot as plt # Visualization
import seaborn as sns          # Statistical visualization
```

### Development Environment
- Anaconda (conda base environment)
- IPython kernel for interactive computing

---

## 📊 Key Methodologies

### Data Loading
- NumPy: `genfromtxt()` for CSV files
- Pandas: `read_csv()` for structured data
- Custom delimiter handling for non-standard formats

### Data Processing
- **Vectorized Operations:** Avoiding explicit loops
- **Unit Conversions:** SI standardization
- **Data Merging:** Multi-key joins across datasets
- **Aggregation:** Grouping and statistical summaries

### Statistical Analysis
- Summary statistics (mean, median, quartiles, std)
- Time-series analysis
- Distribution analysis
- Correlation studies

### Visualization
- Line plots for temporal data
- Horizontal bar charts for rankings
- Seaborn styling for professional appearance
- Matplotlib for custom visualizations

---

## 🎯 Learning Outcomes

Throughout this project, I have demonstrated proficiency in:

1. **Data Manipulation**
   - Efficient handling of large datasets
   - Complex data transformations
   - Multi-source data integration

2. **Statistical Computing**
   - Vectorized operations for performance
   - Appropriate statistical method selection
   - Meaningful metric calculation

3. **Data Visualization**
   - Clear, informative chart design
   - Appropriate visualization type selection
   - Professional presentation standards

4. **Programming Best Practices**
   - Clean, documented code
   - Reproducible analysis workflows
   - Efficient algorithm implementation

5. **Domain Knowledge**
   - Financial data analysis (cryptocurrency)
   - Transportation systems (tram networks)
   - Weather pattern analysis
   - Text and community data analysis

---

## 📈 Dataset Summary

| Task | Primary Dataset | Records | Key Variables |
|------|----------------|---------|---------------|
| 1P | BTC-to-USD | 365 | Date, Close Price |
| 2P | NYC Weather | 26,130 | Temperature, Humidity, Wind |
| 3P | NYC Flights | 336,776 | Carrier, Time, Delays |
| 4P | Melbourne Tram | 2,516,014 | Touch-on/off, Stops, Routes |
| 6C | Stack Overflow | Varies | Posts, Comments, Tags, Votes |

---

## 🚀 How to Use This Repository

### Prerequisites
```bash
# Install required packages
conda install numpy pandas matplotlib seaborn jupyter

# Or using pip
pip install numpy pandas matplotlib seaborn jupyter
```

### Running the Notebooks
1. Navigate to the desired task directory
2. Open the Jupyter notebook:
   ```bash
   jupyter notebook "Task [number] [name].ipynb"
   ```
3. Run all cells to reproduce the analysis

### Data Files
- All datasets are included in their respective task directories
- CSV files are the primary format
- Some tasks use pipe-delimited (|) text files

---

## 📝 Notes

### Code Quality
- All code follows PEP 8 style guidelines
- Comprehensive inline comments explain methodology
- Clear variable naming for readability
- Modular approach to complex operations

### Documentation
- Each notebook includes markdown explanations
- Statistical reasoning is provided
- Visualizations include appropriate labels and titles
- Results are interpreted in context

### Data Sources
- Bitcoin data: Yahoo Finance
- NYC data: nycflights13 R package
- Melbourne tram data: Public Transport Victoria
- Stack Overflow data: Stack Exchange Data Dump

---

## 🎓 Academic Integrity

This work represents original analysis completed as part of SIT220 coursework. All data sources are properly attributed, and methodologies follow industry best practices for data analysis and visualization.

---

## 📧 Contact

**Barbara Calma**  
s224712709@deakin.edu.au  
Deakin University

---

## 🏆 Course Completion

This project demonstrates comprehensive data wrangling skills across:
- ✅ Numerical computing with NumPy
- ✅ Data manipulation with Pandas
- ✅ Statistical analysis and interpretation
- ✅ Professional data visualization
- ✅ Real-world dataset handling
- ✅ Reproducible research workflows

---

*Last Updated: January 2026*  
*Course: SIT220 - Data Wrangling*  
*Institution: Deakin University*
