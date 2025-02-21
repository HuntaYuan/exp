```mermaid
graph TD;
    A((Start)) --> B[Data Preparation:  
                    1) Collect ETF market and financial data<br>
                    2) Standardize time scale (monthly/quarterly)<br>
                    3) Handle missing/abnormal values]
    B --> C[Feature Engineering:  
                    1) Scaling adjustments<br>
                    2) Momentum indicators (1/3/6/9 months)<br>
                    3) TTM indicators and financial factors<br>
                    4) Industry/macroeconomic feature derivation]
    C --> D[Data Splitting:  
                    - In-sample (training/validation)<br>
                    - Out-of-sample (testing)]
    D --> E{Model Selection:  
            MLP / RNN / XGBoost}
    E --> F[Model Training & Validation:  
                    - Hyperparameter tuning<br>
                    - Early Stopping<br>
                    - Cross-validation (or time-series validation)]
    F --> G[Model Evaluation:  
                    - Regression metrics (MSE/MAE/Mape)<br>
                    - Backtest returns / Sharpe ratio<br>
                    - Feature importance (SHAP)]
    G --> H[Industry/ETF Comparison:  
                    - Analyze predictions by industry<br>
                    - Construct ETF-based investment portfolios]
    H --> I[Interpretation & Attribution:  
                    - SHAP/Permutation Importance<br>
                    - Macroeconomic/financial/momentum impact analysis<br>
                    - Error analysis (extreme events)]
    I --> J((End))
