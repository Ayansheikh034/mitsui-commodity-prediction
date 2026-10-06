# MITSUI&CO. Commodity Prediction Challenge

Solution code for the [MITSUI&CO. Commodity Prediction Challenge](https://www.kaggle.com/competitions/mitsui-commodity-prediction-challenge) on Kaggle.

**Result: Silver medal, 73rd out of 1,711 teams.**

## Competition overview

The task is to predict future commodity returns, specifically price-difference series between pairs of assets, using historical data from four markets:

- London Metal Exchange (LME)
- Japan Exchange Group (JPX)
- US stocks
- Forex

There are 424 target columns. Predictions are made through Kaggle's time-series evaluation API, which serves one `date_id` at a time so models cannot look ahead. After the final submission deadline, selected notebooks were re-run against real market data during a forecasting phase.

**Metric:** a Sharpe-style score, computed as the mean Spearman rank correlation between predictions and targets divided by its standard deviation. It rewards predictions that are both accurate and stable over time.

## My approach

> TODO: fill in from your final notebook. Delete any line that doesn't apply.

- **Features:** (e.g. lagged returns, rolling statistics, cross-market spreads, use of `label_lags_1` to `label_lags_4`)
- **Model(s):** (e.g. LightGBM, Ridge, ensemble, one model per target vs. shared model)
- **Validation:** (e.g. time-based split, walk-forward CV, how you avoided leakage)
- **What worked:** ...
- **What didn't:** ...
- **Key lesson:** ...

## Repository structure

```
mitsui-commodity-prediction/
├── README.md
├── .gitignore
├── requirements.txt
└── notebooks/
    └── final_solution.ipynb    # final submission notebook
```

## How to run

1. Download the competition data from the [Data page](https://www.kaggle.com/competitions/mitsui-commodity-prediction-challenge/data) (a Kaggle account and accepting the rules are required).
2. Place the files in a local `data/` folder, or run the notebook on Kaggle where the paths below already exist:
   `/kaggle/input/mitsui-commodity-prediction-challenge/`
3. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
4. Open and run `notebooks/final_solution.ipynb`.

The notebook uses the Kaggle evaluation package (`kaggle_evaluation`), which is only available inside Kaggle's environment, so the full inference loop runs on Kaggle.

## Data

The competition data is **not included** in this repository because Kaggle's competition rules restrict redistribution. Please download it from the link above.

## Acknowledgements

- Competition host: MITSUI & CO., LTD.
- Technical support for problem design and data: AlpacaTech Co., Ltd.
- Forex data: Exchange Rates API by APILayer.

## License

Code in this repository is released under the MIT License (add a `LICENSE` file), unless you choose otherwise. The competition data remains subject to the competition's own terms.
