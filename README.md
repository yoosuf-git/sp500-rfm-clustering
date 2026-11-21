# S&P 500 share segmentation (6BUIS017W CWK1)

Risk-return and adapted RFM (Recency, Frequency, Monetary) clustering of S&P 500 shares, 1 January 2021 to 1 January 2025 (end date exclusive).

## Run order
1. `notebooks/CWK1_Task1.ipynb` - data acquisition, validation, weekly return and beta, adapted RFM. Creates `data/features_task1.csv` and `data/weekly_returns.csv`.
2. `notebooks/CWK1_Task2.ipynb` - Ward and K-means clustering, profiles, sensitivity analysis. Needs `features_task1.csv`; creates `data/features_with_clusters.csv`.
3. `notebooks/CWK1_Task3.ipynb` - evidence for the business review. Needs `features_with_clusters.csv` and `weekly_returns.csv`.

Each Colab notebook has its own file space, so upload the files named above when a notebook asks for them.

## Data and provenance
- `data/` holds the price snapshots (Adjusted Close, Close, Volume), the constituent list, feature tables, cluster assignments and the output tables.
- `data/retrieval_metadata.json` records the retrieval date, Wikipedia revision, data source, package versions and file hashes.
- `figures/` holds the figures used in the report.
- Package versions are in `requirements.txt`.

## Open in Colab
[Task 1](https://colab.research.google.com/github/yoosuf-git/sp500-rfm-clustering/blob/main/notebooks/CWK1_Task1.ipynb) |
[Task 2](https://colab.research.google.com/github/yoosuf-git/sp500-rfm-clustering/blob/main/notebooks/CWK1_Task2.ipynb) |
[Task 3](https://colab.research.google.com/github/yoosuf-git/sp500-rfm-clustering/blob/main/notebooks/CWK1_Task3.ipynb)
