# Predictive Tax Compliance Risk & Revenue Assurance Analytics Platform

Academic prototype for BAN6800. The project uses the public UCI Online Retail II dataset as a proxy for transaction analytics. It is informed by Kenyan tax-administration workflows but is not a KRA system and does not use confidential KRA data.

## Scope boundary
The dataset contains UK retail transactions, not Kenyan tax returns, eTIMS records or verified tax-compliance outcomes. Outputs are anomaly indicators for human review only; they do not establish fraud, evasion, VAT liability or legal non-compliance.

## Repository
- `data/raw/`: local source files (excluded from Git)
- `data/processed/`: derived datasets (publish only safe aggregates/sample data)
- `data/data_dictionary/`: field definitions
- `notebooks/`: EDA, feature engineering and experiments
- `src/`: ingestion, cleaning, features and models
- `sql/`: schema and analytical queries
- `dashboards/`: Power BI files and screenshots
- `reports/`: reports and validation outputs
- `tests/`: data and model tests
- `docs/`: architecture, ethics, governance and project controls
- `api/`: optional FastAPI prototype

## Setup
```bash
python -m venv .venv
# activate the environment, then:
pip install -r requirements.txt
```

## Data governance
Do not commit raw row-level data, customer identifiers, credentials, confidential taxpayer records or internal KRA material. Record source filename, retrieval date, checksum and transformation version. Publish aggregate outputs only.

## Planned delivery
Four sprints: project/data setup; preparation and EDA; anomaly detection, explainability and fairness; dashboard, testing and reporting.
