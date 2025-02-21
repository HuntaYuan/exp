```mermaid
graph TD;
    A((开始)) --> B[数据准备<br/>1. 采集ETF行情、财务数据<br/>2. 统一时间尺度(月度/季度)<br/>3. 缺失值/异常值处理];
    B --> C[特征工程<br/>1. 规模调整(Scaling)<br/>2. 动量指标 (1/3/6/9个月)<br/>3. TTM指标等财务因子<br/>4. 行业/宏观特征衍生];
    C --> D[数据分割<br/>- In-sample (训练/验证)<br/>- Out-of-sample (测试)];
    D --> E{模型选择<br/>MLP / RNN / XGBoost...};
    E --> F[模型训练与验证<br/>- 超参数调优<br/>- Early Stopping<br/>- 交叉验证(或时序验证)];
    F --> G[模型评估<br/>- 回归指标 (MSE/MAE/Mape)<br/>- 回测收益/夏普比率<br/>- 特征重要度(Shap)];
    G --> H{行业/ETF对比<br/>- 分行业查看预测表现<br/>- 按ETF构建投资组合};
    H --> I[解释与归因<br/>- SHAP/Permutation Importance<br/>- 宏观/财务/动量影响分析<br/>- 错误分析(极端事件)];
    I --> J((结束));
