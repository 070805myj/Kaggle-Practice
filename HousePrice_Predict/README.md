🏠 房价预测项目 (House Prices Prediction)
本项目是基于 Kaggle 经典的入门比赛 House Prices: Advanced Regression Techniques 开发的机器学习模型。其目标是根据房屋的各项特征（如面积、建造年份、房间数等）预测房屋的最终销售价格。
📋 项目概述
在这个项目中，我们完成了一个从原始数据处理到模型提交的完整机器学习工作流。我们通过对比**决策树（Decision Tree）和随机森林（Random Forest）**模型，最终选择了泛化能力更强的随机森林算法。

🛠️ 技术栈
语言: Python 3

库:
pandas: 数据处理与清洗
scikit-learn: 机器学习模型构建（RandomForestRegressor）
train_test_split: 数据集拆分
mean_absolute_error: 模型评估指标

📊 数据特征
模型使用了以下 7 个关键特征进行训练：
LotArea: 占地面积
YearBuilt: 建造年份
1stFlrSF: 一楼面积
2ndFlrSF: 二楼面积
FullBath: 浴室数量
BedroomAbvGr: 卧室数量（地下室除外）
TotRmsAbvGrd: 总房间数（不含浴室）

🚀 核心流程
数据加载: 使用 pandas 读取 train.csv。
模型选择: 比较了 DecisionTreeRegressor 和 RandomForestRegressor。
参数调优: 探索了 max_leaf_nodes 对模型过拟合的影响。
模型评估: 采用 MAE (平均绝对误差) 作为衡量标准。
全量训练: 使用全部训练数据重新拟合模型，以获得最强性能。
结果生成: 对 test.csv 进行预测并导出 submission.csv。

📈 结果与发现
基准模型: 单棵决策树容易出现过拟合。
改进模型: 随机森林通过集成学习显著降低了 MAE，提升了预测的稳定性和准确性。
结论: 随着数据量的增加和算法的升级，模型的平均预测误差明显下降。

📂 文件说明
notebook.ipynb: 包含所有分析、绘图和建模过程的 Jupyter Notebook。
submission.csv: 最终生成的预测结果文件，可直接提交至 Kaggle。

kaggle训练集地址：/kaggle/input/home-data-for-ml-course/train.csv
      测试集地址：/kaggle/input/home-data-for-ml-course/test.csv
