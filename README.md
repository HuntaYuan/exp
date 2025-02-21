```mermaid
graph TD;
    A((Start)) --> B[Data Preparation:
        1) Collect ETF market and financial data
        2) Standardize time scale (monthly/quarterly)
        3) Handle missing/abnormal values]
    B --> C[Feature Engineering:
        1) Scaling adjustments
        2) Momentum indicators (1/3/6/9 months)
        3) TTM indicators and financial factors
        4) Industry/macroeconomic feature derivation]
    C --> D[Data Splitting:
        - In-sample (training/validation)
        - Out-of-sample (testing)]
    D --> E{Model Selection:
        MLP / RNN / XGBoost}
    E --> F[Model Training & Validation:
        - Hyperparameter tuning
        - Early Stopping
        - Cross-validation (or time-series validation)]
    F --> G[Model Evaluation:
        - Regression metrics (MSE/MAE/Mape)
        - Backtest returns / Sharpe ratio
        - Feature importance (SHAP)]
    G --> H[Industry/ETF Comparison:
        - Analyze predictions by industry
        - Construct ETF-based investment portfolios]
    H --> I[Interpretation & Attribution:
        - SHAP/Permutation Importance
        - Macroeconomic/financial/momentum impact analysis
        - Error analysis (extreme events)]
    I --> J((End))
