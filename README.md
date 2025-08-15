# 甲地孕酮(Megestrol Acetate)数据挖掘项目

## 📋 项目概述

本项目基于甲地孕酮(Megestrol Acetate)的不良事件报告数据，运用数据挖掘技术进行全面的药物安全性分析。甲地孕酮是一种合成孕激素，主要用于治疗晚期乳腺癌和子宫内膜癌，以及改善癌症患者的食欲和体重。

## 🎯 项目目标

1. **信号检测**: 识别与甲地孕酮相关的不良事件信号
2. **数据预处理**: 清洗和标准化原始数据
3. **特征工程**: 构建预测性特征
4. **关联规则挖掘**: 发现不良事件之间的关联关系
5. **机器学习建模**: 构建风险预测模型
6. **模型优化**: 通过特征筛选提升模型性能

## 🏗️ 项目结构

```
megestrol-acetate-data-mining/
├── src/                    # 源代码
│   ├── data_processing/    # 数据预处理
│   ├── feature_engineering/ # 特征工程
│   ├── signal_detection/   # 信号检测
│   ├── machine_learning/   # 机器学习建模
│   └── visualization/      # 数据可视化
├── data/                   # 数据文件
├── results/                # 结果文件
├── notebooks/              # Jupyter笔记本
└── docs/                   # 文档
```

## 🚀 快速开始

### 环境要求
- Python 3.8+
- 依赖包见 requirements.txt

### 安装依赖
```bash
pip install -r requirements.txt
```

### 运行主要脚本
```bash
# 数据预处理
python src/data_processing/main.py

# 特征工程
python src/feature_engineering/main.py

# 信号检测
python src/signal_detection/main.py

# 机器学习建模
python src/machine_learning/main.py

# 可视化
python src/visualization/main.py
```

## 📊 主要功能

### 1. 数据预处理
- HTML数据提取和清洗
- 数据完整性检查
- 格式标准化

### 2. 特征工程
- 构建148个高级特征
- 特征选择和降维
- 筛选出8个核心特征

### 3. 信号检测
- 多种统计方法：ROR、PRR、IC、EBGM
- 识别36个潜在不良事件信号
- 交叉验证信号可靠性

### 4. 机器学习建模
- 多种算法：逻辑回归、随机森林、SVM、XGBoost等
- 特征筛选前后性能对比
- 模型优化和评估

### 5. 关联规则挖掘
- Apriori算法
- 发现2,408条关联规则
- 识别高风险事件组合

## 📈 核心结果

### 信号检测结果
- **最显著信号**: 继发性肾上腺皮质功能不全 (ROR=617.83)
- **主要影响系统**: 内分泌系统、心血管系统、神经系统
- **高风险事件**: 脑膜瘤、肾上腺功能不全、血栓栓塞事件

### 特征工程成果
- **原始特征**: 168个
- **核心特征**: 8个 (减少95.2%)
- **信息保留**: 保持核心预测能力

### 模型性能
- **最佳模型**: 朴素贝叶斯 (90.91%准确率)
- **特征筛选效果**: 提升模型稳定性1.51%
- **计算效率**: 显著提升

## 🔬 技术栈

- **编程语言**: Python 3.8+
- **数据处理**: Pandas, NumPy
- **机器学习**: Scikit-learn, XGBoost
- **数据可视化**: Matplotlib, Seaborn, Plotly
- **统计分析**: SciPy
- **关联规则**: MLxtend

## 📚 文档

- [完整技术报告](docs/complete_report.md)
- [API文档](docs/api.md)
- [用户指南](docs/user_guide.md)

## 🤝 贡献

欢迎提交Issue和Pull Request！

## 📄 许可证

MIT License

## 📞 联系方式

如有问题，请提交Issue或联系项目维护者。

---

*项目生成时间: 2025年1月*
*数据来源: FDA不良事件报告系统(FAERS)*
