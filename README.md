```mermaid
graph TD;
    A((Start)) --> B[Data Preparation]
    
    B --> B1[Collect ETF market & financial data]
    B --> B2[Standardize time scale: monthly or quarterly]
    B --> B3[Handle missing and abnormal values]
    
    B3 --> C[Feature Engineering]
    C --> C1[Scaling adjustments]
    C --> C2[Momentum indicators (1, 3, 6, 9 months)]
    C --> C3[TTM indicators and financial factors]
    C --> C4[Industry and macroeconomic features]

    C4 --> D[Data Splitting]
    D --> D1[In-sample: training and validation]
    D --> D2[Out-of-sample: testing]

    D2 --> E{Model Selection}
    E --> E1[MLP]
    E --> E2[RNN]
    E --> E3[XGBoost]

    E3 --> F[Model Training and Validation]
    F --> F1[Hyperparameter tuning]
    F --> F2[Early Stopping]
    F --> F3[Cross-validation]

    F3 --> G[Model Evaluation]
    G --> G1[Regression metrics: MSE, MAE, MAPE]
    G --> G2[Backtest returns and Sharpe ratio]
    G --> G3[Feature importance: SHAP]

    G3 --> H[Industry and ETF Comparison]
    H --> H1[Analyze predictions by industry]
    H --> H2[Construct ETF-based portfolios]

    H2 --> I[Interpretation and Attribution]
    I --> I1[SHAP and Permutation Importance]
    I --> I2[Macroeconomic and financial impact]
    I --> I3[Error analysis: extreme events]

    I3 --> J((End))
