# Enzyme Kinetic Fitting

<img src="https://github.com/ManuelGehl/Enzyme-kinetic-fitting/blob/main/WT.png?raw=true" height=400>

## Overview

The Enzyme Kinetic Fitting repository provides a Python script that takes Excel files with specific activity measurements for enzymes (and corresponding mutants) and performs a curve fitting to the Michaelis-Menten equation. I have used this code to determine the kinetic constants of wild-type and mutant enzymes. For example in:
* [Crystal structure of FAD-independent methylene-tetrahydrofolate reductase from Mycobacterium hassiacum](https://onlinelibrary.wiley.com/doi/10.1002/prot.26504)
* [Convergent evolution of (βα)8-barrel fold methylene-tetrahydropterin reductases utilizing a common catalytic mechanism](https://www.biorxiv.org/content/10.1101/2023.09.18.558202v1)

## How It Works

1. **Data Input**: The script takes an Excel file as input, which should contain specific activity measurements. Each mutant (or wild type) should be represented as a separate tab in the Excel file (e.g., "WT" or "E9Q"). The data should be structured in a specific table format.

2. **Data Format**: The table in the Excel file should be organized as follows:

| row | substrate_1 | substrate_2 | specific activity 1 | specific activity 2 | specific activity 3 | mean | stdev |
|-----|-------------|-------------|---------------------|---------------------|---------------------|------|-------|
| 1 | 0 | 0 | 0 | 0 | 0 | 0 | 0 |
| 2 | 20 | 300 | X | X | X | X | X |
| 3 | 40 | 300 | X | X | X | X | X |
| 4 | 60 | 300 | X | X | X | X | X |
| 5 | 80 | 300 | X | X | X | X | X |
| 6 | 100 | 300 | X | X | X | X | X |
| 7 | 130 | 300 | X | X | X | X | X |
| 8 | 0 |
| 9 | 0 | 0 | 0 | 0 | 0 | 0 | 0 |
| 10 | 100 | 50 | X | X | X | X | X |
| 11 | 100 | 100 | X | X | X | X | X |
| 12 | 100 | 200 | X | X | X | X | X |
| 13 | 100 | 300 | X | X | X | X | X |
| 14 | 100 | 400 | X | X | X | X | X |
| 15 | 100 | 500 | X | X | X | X | X |

>The table in the Excel file should contain measurements for 7 different substrate concentrations. The concentration of substrate 2 is fixed in the first 7 rows (e.g. 300 mM) and different concentrations of substrate 1 are measured as triplicates (specific activity 1, specific activity 2, specific activity 3).
Row 8 is just a blank for a better overview. From row 9 to row 15, the concentration of substrate 1 is fixed (e.g. 100 mM) and the specific activity is measured for different concentrations of substrate 2. The mean and standard deviation columns contain the mean and standard deviation over the triplicates for a specific substrate concentration combination.
