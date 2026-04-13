COMP115 Project 2: BC housing Affordability Analysis

Description:

This project analyzes the 2016 BC Census dataset using pandas to examine housing affordability across British Columbia. It identifies Community Health Service Areas (CHSAs) with high shelter rent burden (>50% renters spending 30% or more of income on shelter) and compares rental subsidization rates across Provincial Health Authorities (PHAs).

The analysis demonstrates key Python data science concepts:

Data loading and exploration ('df.head()', 'df.info()', 'df.describe()')
Filtering and sorting high-burden areas
Groupby aggregation across regions
Custom calculations (rent-to-income ratio)
Data visualization with matplotlib bar plots
Code Overview The project is structured aroung two main tasks:

Task 1: Find high-stress CHSAs and calculate rent-to-income ratios '''python high_stress = df[df["shelt_rent_30plus_rate"] > 50] task1["rent_to_income_ratio"] = (task1["shelt_rent_mo_cost_mean"] * 12) / task1["income_after_tax_mean"] '''

Task 2: PHA-level comparison with bar plot '''python task2 = df.groupby("pha").agg({...}) task2["shelt_rent_subsidized_rate_mean"].plot(kind="bar") '''

The screenshot of the bar plot is shown below:

How to Run:

Clone or download this repository
Open 'analysis.py' in your Python IDE
Install dependencies: '''pip install pandas matplotlib '''
Run the program: '''python analysis.py '''
View tables and bar plot output
Files:

'analysis.py' — Complete analysis script
'BC Census 2016 data.csv' — Dataset from eLearn
'pha_subsidies.png' — Bar plot visualization
'README.md' — Project documentation
License:

This project is open-source and free to use for educational purpose.

-COMP115 Appendix A Project 2 by Chelsea & Joaquin-
