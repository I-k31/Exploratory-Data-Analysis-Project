Ontario Hotel Performance EDA (2020–2023)


Overview:
This project performs an exploratory data analysis (EDA) on Ontario hotel performance data from 2020 to 2023, covering three key metrics across 20+ regions and sub-regions. The analysis explores the impact of COVID-19 on hotel performance and the subsequent recovery across different parts of Ontario.

Dataset: Ontario Hotel Statistics — Ontario Open Data Portal (https://data.ontario.ca/dataset/hotel-statistics/resource/35d335c6-b2e9-46cc-b4b1-ca149a5a3aba)
Source: CBRE Hotels

Tools & Libraries

-Language: Python
-Packages: pandas, Matplotlib, Seaborn

Data Preprocessing: The raw Excel file contained merged headers, multi-level region hierarchies, empty spacer rows, and a source footer row. 

The following preprocessing steps were performed:

-Manual: Restructured the multi-level headers into a flat single-header format in Excel before loading into Python

-Python: Assigned clean column names, removed filler columns, stripped empty and header/footer rows, converted occupancy values to percentages, and converted ADR and RevPAR to numeric with 2 decimal places

-Region summary rows (e.g. "Greater Toronto Area", "Eastern Ontario") were separated from specific sub-regions for more accurate analysis

Analysis & Key Findings
1. COVID Recovery (2020 → 2023)

Downtown Toronto had the largest recovery, jumping from 21.9% to 70.3% occupancy — a gain of 48.4 percentage points
Toronto Airport and GTA West also showed strong recoveries
Windsor had a dramatic late recovery, going from 33% in 2020 to 72.9% in 2023 — likely driven by cross-border traffic from Detroit
Thunder Bay held up the best during COVID with the highest 2020 occupancy at 49.5%

2. Top & Bottom Performers (2023)
Occupancy:

Highest: Toronto Airport (80.0%), GTA West (74.3%), GTA East/North (73.5%)
Lowest: Other Southern Ontario (54.0%), Other Eastern Ontario (60.4%), North Bay (61.6%)

Average Daily Rate (ADR):

Highest: Downtown Toronto ($323.82), Downtown Ottawa ($220.22), Niagara Falls ($207.25)
Lowest: North Bay ($132.31), Sault Ste. Marie ($141.70), Windsor ($136.55)

3. Correlation Between Occupancy and ADR

Weak positive correlation of 0.36 between occupancy rate and ADR in 2023
Suggests occupancy and pricing are somewhat independent — some regions charge premium rates regardless of fill rate (Downtown Toronto), while others have high occupancy but keep rates low (Toronto Airport, Windsor)

4. Revenue Per Available Room (RevPAR)

Downtown Toronto dominates at $227.71 — significantly ahead of all other regions
GTA and Downtown Ottawa form a strong second tier around $150–$167
North Bay and Other Southern Ontario are the weakest markets at around $80

5. Occupancy Heatmap (2020–2023)

Clear left-to-right darkening across all regions confirms universal recovery from COVID
Niagara Falls shows the most dramatic color shift — severely impacted in 2020 (27.4%) but strongly recovered by 2023 (68.6%)
Windsor stays light through 2021 then jumps sharply in 2022–2023
