# Ontario Hotel Performance Analysis (2020–2023)

##  Executive Summary
This extensive Exploratory Data Analysis (EDA) investigates the performance dynamics of Ontario's hotel industry from the onset of the COVID-19 pandemic through its recovery phase (2020–2023). By analyzing distinct geospatial metrics—Occupancy Rate, Average Daily Rate (ADR), and Revenue Per Available Room (RevPAR)—this study highlights region-specific vulnerabilities, recovery trajectories, and emerging pricing strategies.

##  Business Context
The hospitality sector faced unprecedented disruptions starting in 2020. Understanding the recovery spectrum across over 20 sub-regions in Ontario is critical for:
- **Investment & Capital Allocation:** Identifying high-yield regions for future hotel development.
- **Pricing Strategy Optimization:** Understanding the elasticity between Occupancy and ADR.
- **Tourism Board Policy:** Directing targeted marketing campaigns to lagging regions.

##  Dataset Information
- **Source:** [Ontario Open Data Portal - Hotel Statistics](https://data.ontario.ca/dataset/hotel-statistics/resource/35d335c6-b2e9-46cc-b4b1-ca149a5a3aba) via CBRE Hotels.
- **Scope:** 20+ regions and sub-regions across Ontario.
- **Key Metrics:**
  - `Occupancy Rate (%)`: Percentage of available rooms sold.
  - `Average Daily Rate (ADR)`: Average rental revenue per occupied room.
  - `Revenue Per Available Room (RevPAR)`: Total room revenue divided by total available rooms.

##  Methodology & Tech Stack
- **Language:** Python 3.x
- **Libraries:** `pandas` (Data manipulation), `matplotlib` & `seaborn` (Data visualization)
- **Data Engineering:**
  - Resolved multi-level hierarchical headers and unified them into a flat schema.
  - Cleansed data by removing non-analytical spacer rows, metadata footers, and aggregated provincial summary rows to prevent double-counting.
  - Standardized string formats and enforced numeric typings across all target metric columns.

##  Key Analytical Insights

### 1. The Post-Pandemic Rebound (2020 vs. 2023)
- **Urban Resurgence:** Downtown Toronto exhibited the most aggressive recovery, scaling from a devastating 21.9% occupancy in 2020 to 70.3% in 2023 (+48.4 pts).
- **Border Town Anomalies:** Windsor displayed a unique "hockey-stick" recovery heavily concentrated in late 2022-2023, likely catalyzed by the resumption of cross-border commercial traffic from Detroit.
- **Resilient Markets:** Thunder Bay maintained the highest baseline occupancy during the peak pandemic year (49.5% in 2020), showcasing the stability of northern essential travel.

### 2. Pricing Power Dynamics
- **Volume vs. Premium Pricing:** There is only a weak positive correlation (r = 0.36) between Occupancy and ADR in 2023. This indicates decoupled strategies: 
  - *High Volume, Moderate Rate:* Toronto Airport runs at peak capacity (80.0% occupancy) but moderates rates.
  - *Moderate Volume, Premium Rate:* Downtown Toronto leverages its localized monopoly on luxury and corporate bookings to command peak market ADR ($323.82) despite trailing the airport in raw occupancy.

### 3. Revenue Leadership (RevPAR)
- Downtown Toronto completely dominates the RevPAR landscape at $227.71, eclipsing the secondary tier (GTA and Downtown Ottawa at ~$150-$167). 
- Northern and rural southern regions lag significantly (RevPAR ~$80), representing either low-cost transit accommodations or suppressed demand.

##  How to Run the Analysis
1. Clone the repository: `git clone https://github.com/I-k31/Exploratory-Data-Analysis-Project.git`
2. Ensure you have the required dependencies: `pip install pandas matplotlib seaborn openpyxl`
3. Execute the Jupyter Notebook: `jupyter notebook "EDA Project.ipynb"`
