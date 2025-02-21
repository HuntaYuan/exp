```mermaid
graph TD;
    A((Start)) --> B[Data Preparation:
        1) Collect ETF market and financial data\n
        2) Standardize time scale (monthly/quarterly)\n
        3) Handle missing/abnormal values]
    B --> C[Feature Engineering:
        1) Scaling adjustments\n
        2) Momentum indicators (1/3/6/9 months)\n
        3) TTM indicators and financial factors\n
        4) Industry/macroeconomic feature derivation]
    C --> D[Data Splitting:
        - In-sample (training/validation)\n
        - Out-of-sample (testing)]
    D --> E{Model Selection:
        MLP / RNN / XGBoost}
    E --> F[Model Training & Validation:
        - Hyperparameter tuning\n
        - Early Stopping\n
        - Cross-validation (or time-series validation)]
    F --> G[Model Evaluation:
        - Regression metrics (MSE/MAE/Mape)\n
        - Backtest returns / Sharpe ratio\n
        - Feature importance (SHAP)]
    G --> H[Industry/ETF Comparison:
        - Analyze predictions by industry\n
        - Construct ETF-based investment portfolios]
    H --> I[Interpretation & Attribution:
        - SHAP/Permutation Importance\n
        - Macroeconomic/financial/momentum impact analysis\n
        - Error analysis (extreme events)]
    I --> J((End))
