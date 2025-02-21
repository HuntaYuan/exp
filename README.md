```mermaid
graph TD;
    A((Start)) --> B[Data Preparation]
    B --> C[Feature Engineering]
    C --> D[Data Splitting]
    D --> E{Model Selection}
    E --> F[Model Training & Validation]
    F --> G[Model Evaluation]
    G --> H[Industry/ETF Comparison]
    H --> I[Interpretation & Attribution]
    I --> J((End))
