```mermaid
graph TD;
    A((开始)) --> B[数据准备: \n1. 采集ETF行情、财务数据 \n2. 统一时间尺度(月度/季度) \n3. 缺失值/异常值处理];
    B --> C[特征工程: \n1. 规模调整(Scaling) \n2. 动量指标 (1/3/6/9个月) \n3. TTM指标等财务因子 \n4. 行业/宏观特征衍生];
    C --> D[数据分割: \n- In-sample (训练/验证) \n- Out-of-sample (测试)];
    D --> E[模型选择: \nMLP / RNN / XGBoost];
    E --> F[模型训练与验证: \n- 超参数调优 \n- Early Stopping \n- 交叉验证(或时序验证)];
    F --> G[模型评估: \n- 回归指标 (MSE/MAE/Mape) \n- 回测收益/夏普比率 \n- 特征重要度(Shap)];
    G --> H[行业/ETF对比: \n- 分行业查看预测表现 \n- 按ETF构建投资组合];
    H --> I[解释与归因: \n- SHAP/Permutation Importance \n- 宏观/财务/动量影响分析 \n- 错误分析(极端事件)];
    I --> J((结束));
