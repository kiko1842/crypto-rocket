Crypto Rocket

Crypto Rocket is a lightweight, open-source toolkit for exploring cryptocurrency data and prototyping trading strategies. It includes utilities to fetch market data, compute indicators, and run local backtests — ideal for developers experimenting with crypto workflows.

Quick Summary

Purpose: Fetch crypto market data, compute indicators, and run local strategy experiments.

Status: Early-stage prototype.

License: MIT (see LICENSE file)

Features

Market and candlestick data from public APIs (configurable)

Basic indicators: SMA, EMA, RSI

Sample scripts for backtesting and analysis

Dockerfile and local run instructions

Installation (Local)

git clone https://github.com/kiko1842/crypto-rocket.git
cd crypto-rocket
python -m venv .venv
source .venv/bin/activate  # macOS/Linux
.venv\Scripts\activate     # Windows
pip install -r requirements.txt

For JavaScript/TypeScript projects:
npm install
# or
yarn install

Quick Start — Examples

# Fetch sample data
python scripts/fetch_data.py --symbol BTCUSDT --interval 1h --limit 500

# Run indicator calculation
python scripts/run_indicator.py --symbol BTCUSDT --indicator sma --period 20

# Run a backtest
python scripts/backtest.py --strategy simple_mean_reversion --symbol BTCUSDT --from 2023-01-01 --to 2024-01-01 

Configuration & Secrets

Store API keys in a .env file (never commit secrets)

Example .env:

API_KEY=your_api_key_here
API_SECRET=your_api_secret_here

Docker (Optional)
# Build
docker build -t crypto-rocket:local .

# Run
docker run --env-file .env --rm crypto-rocket:local python scripts/fetch_data.py --symbol BTCUSDT

Tests & CI

Use pytest or jest for core functions

Add GitHub Actions workflow for linting and tests

Security Checklist

Add .gitignore and LICENSE

Run pip-audit or npm audit

Use git-secrets or GitHub secret scanning

Roadmap

[x] README, LICENSE

[ ] CI setup

[ ] Core scripts: fetch, indicators, backtest

[ ] Sample configs and datasets

[ ] Strategy expansion and reporting

[ ] Docker image publishing

Contributing

Open issues with clear steps and environment info

Follow coding style and test requirements

Use linters and formatters

Contact

Maintainer: @kiko1842




