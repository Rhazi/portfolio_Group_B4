A small educational framework developed for FINM367 — designed to run DFA and Factor Investing.

Overview
This repository implements a simple backtester. The repo file of interest: group_B_hmw_4.ipynb — jupyter script that wires all components together and runs experiments sequentially:

Requirements
Python 3.10+ recommended
Create and activate a virtual environment before installing dependencies.
Example (macOS / zsh):

python3 -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
If you don't have a requirements.txt, install commonly used packages: pip install pandas numpy matplotlib

use pyproject.toml for jupyter dependencies

Project structure
data/ — place CSV historical excess returns & descriptions here
README.md — this file
Data format
The backtester expects data in a timeseries CSV with at least the following columns:

timestamp — ISO-8601 datetime string (e.g. 2020-01-01T09:30:00)
excess returns — identified by a ticker symbol (e.g. TIP) Example CSV:
timestamp, excess return
Date	BWX	DBC
YYYY-00-DD 00:00:SS	24,350736618042	24,93212890625
How to run a backtest
Prepare data in data/multi_asset_etf_data.csv.

Use group_B_hmw_4.ipynb to run the backtest. It works sequentially:

load data
run computing/optimizations over data
produce a report
Reporting and analysis
solutionsUpdate.ipynb should compute common metrics: mean returns, volatility, Sharpe ratios, and generate comparison plots. Use pandas and matplotlib for visuals.

Contact
For questions about this repository, ask this course group contributors. Include the file(s) you modified and a brief description of the expected vs actual behavior.
