# 6BUIS017W CWK1 - Market Analysis and Stock Segmentation Using RFM

## Assessment Details
- **Module:** 6BUIS017W CRM & CM With Business Intelligence (University of Westminster)
- **Study Period:** `2021-01-01` to `2025-01-01` (end date exclusive; 1,005 trading days, 207 aligned weekly return periods)
- **Explicit Observation Date:** `2024-12-31`
- **Data Retrieval Timestamp:** `2026-11-22 17:52:57 UTC`
- **Universe:** `503` S&P 500 symbols extracted from Wikipedia → `17` transparently excluded (`5` failed post-2024 downloads, `10` partial histories, `2` zero-volume stale-price shares) → **`486` common valid shares**

## Repository Structure
| Path         | Description |
|--------------|-------------|
| `CWK1.ipynb` | Runnable Google Colab / Jupyter notebook covering Tasks 1, 2 and 3 (Cells 1–21). |
| `data/`      | Saved raw daily CSV snapshots (`Close`, `Adj Close`, `Volume`, `Stock Splits`, `Dividends`, `^GSPC`, Wikipedia tickers) and `data_provenance.json` with SHA-256 checksums.|
| `outputs/`   | Reproducible analytical tables: `package_versions.csv`, `exclusion_log.csv`, `worked_example_AAPL_60d.csv`, `task1_feature_table.csv`, `master_feature_and_cluster_assignments.csv` (all 4 baseline models + R-F sensitivity), `k=2..8` evaluation metrics, original-unit profiles, PCA loadings, correlations, cross-tabs and GICS sector breakdowns. |
| `figures/`  | Saved 150-DPI PNG charts: feature distributions, Ward dendrograms, Elbow/Silhouette comparisons, labelled Risk-Return scatter plots, RFM 2D PCA & snake plots, Monetary-removal boxplots, Data Mart star schema and GICS sector stacked bars. |

## How to Reproduce
1. Clone this repository or open `CWK1.ipynb` in Google Colab (Python 3.10-3.13).
2. Run all cells top-to-bottom. With `USE_CACHE_FIRST = True`, Cell 4 verifies SHA-256 hashes against `data/data_provenance.json` and reproduces identical results without live Yahoo Finance revisions.

## Software Environment
Python `3.13.18` | `pandas 2.2.3` | `numpy 2.4.6` | `yfinance 0.2.66` | `scikit-learn 1.6.1` | `scipy 1.16.3` | `matplotlib 3.10.0` | `seaborn 0.13.2`
