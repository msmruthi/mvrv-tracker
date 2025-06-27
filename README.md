This repository contains code for calculating and analyzing the MVRV (Market Value to Realized Value) ratio for Bitcoin and Solana. The project uses freely available price and volume data from the CoinGecko API. For full details on system design, methodology, assumptions, limitations, and validation, please refer to the main report: MVRV_Assignment.pdf

**Features**
- Volume Weighted Average Price (VWAP) used as a proxy for Realized Price
- Daily and hourly MVRV tracking
- CSV-based outputs for quick inspection
- SQLite-based implementation for scalable tracking (Bitcoin)
- Rolling average smoothing applied to calculate Solana’s VWAP
- Data validation against Yahoo Finance for accuracy

**Contents**
|File|Description|
|----|------|
|Data_Validation.ipynb|Compares CoinGecko price data against Yahoo Finance for both BTC and SOL to validate consistency.|
|Bitcoin_MVRV_Calculation.ipynb|Calculates daily and hourly MVRV for Bitcoin using CoinGecko data. Outputs are saved as downloadable CSVs.|
|Solana_MVRV_Calculation.ipynb|Similar to the Bitcoin notebook but for Solana. Includes a smoothing function for VWAP to reduce noise.|
|MVRV_Tracker_using_SQLite.ipynb|Implements a scalable system to fetch, calculate, and store Bitcoin MVRV in a SQLite database using Python’s schedule module.|
|sample output folder containg daily_mvrv.csv, hourly_mvrv.csv, sol_daily_mvrv.csv, sol_hourly_mvrv.csv|Sample CSV outputs for plotting and inspection.|
|MVRV_Assignment.pdf|Main report with system design, methodology, assumptions, limitations, and validation.|

**Notes**
- The Solana system was implemented as a standalone notebook with CSV output, but its functions can be easily swapped into the SQLite tracker for full automation.
- The full methodology and system design are documented in the accompanying MVRV_Assignment report.
