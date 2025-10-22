A small educational framework developed for FINM367 — designed to run DFA and Factor Investing.

Overview

This repository implements a simple backtester. The repo file of interest: group_B_hmw_4.ipynb — jupyter script that wires all components together and runs experiments sequentially:

Requirements
 <br />
Python 3.10+ recommended
 <br />
Create and activate a virtual environment before installing dependencies.
 <br />
 
Example (macOS / zsh):
 <br />
python3 -m venv .venv
 <br />
source .venv/bin/activate
 <br />
pip install -r requirements.txt
 <br />
If you don't have a requirements.txt, install commonly used packages: pip install pandas numpy matplotlib

use pyproject.toml for jupyter dependencies

Project structure
 <br />
data/ — place CSV historical excess returns & descriptions here
 <br />
README.md — this file
 <br />
Data format
 <br />
The backtester expects data in a timeseries CSV with at least the following columns:
 <br />
timestamp — ISO-8601 datetime string (e.g. 2020-01-01T09:30:00)
excess returns — identified by a ticker symbol (e.g. TIP) Example CSV:
timestamp, excess return
Date	BWX	DBC
YYYY-00-DD 00:00:SS	24,350736618042	24,93212890625

 <br />
How to run a backtest
 <br />
Prepare data in data/multi_asset_etf_data.csv.
 <br />
Use group_B_hmw_4.ipynb to run the backtest. It works sequentially:
 <br />
load data
 <br />
run computing/optimizations over data
 <br />
produce a report
 <br />
Reporting and analysis
 <br />
group_b_hmw_4.ipynb should compute common metrics: mean returns, volatility, Sharpe ratios, and generate comparison plots. Use pandas and matplotlib for visuals.

Contact
For questions about this repository, ask this course group contributors. Include the file(s) you modified and a brief description of the expected vs actual behavior.
