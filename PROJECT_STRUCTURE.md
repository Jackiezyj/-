# 项目结构说明
# Project Structure Documentation

## 📁 目录结构
```
megestrol-acetate-data-mining/
├── README.md                           # 项目说明文档
├── PROJECT_STRUCTURE.md                # 项目结构说明 (本文件)
├── main.py                            # 主程序入口
├── requirements.txt                    # Python依赖包
├── .gitignore                         # Git忽略文件
├── src/                               # 源代码目录
│   ├── __init__.py                    # 包初始化文件
│   ├── data_processing/               # 数据预处理模块
│   │   ├── __init__.py
│   │   ├── html_extractor.py         # HTML数据提取器
│   │   ├── data_cleaner.py           # 数据清洗器 (待实现)
│   │   └── data_validator.py         # 数据验证器 (待实现)
│   ├── feature_engineering/           # 特征工程模块
│   │   ├── __init__.py
│   │   ├── feature_builder.py        # 特征构建器 (待实现)
│   │   ├── feature_selector.py       # 特征选择器 ✅
│   │   └── feature_transformer.py    # 特征变换器 (待实现)
│   ├── signal_detection/              # 信号检测模块
│   │   ├── __init__.py               # (待实现)
│   │   ├── signal_detector.py        # 信号检测器 (待实现)
│   │   └── statistical_methods.py    # 统计方法 (待实现)
│   ├── machine_learning/              # 机器学习模块
│   │   ├── __init__.py               # (待实现)
│   │   ├── model_trainer.py          # 模型训练器 (待实现)
│   │   └── model_evaluator.py        # 模型评估器 (待实现)
│   └── visualization/                 # 可视化模块
│       ├── __init__.py               # (待实现)
│       ├── chart_generator.py        # 图表生成器 (待实现)
│       └── report_generator.py       # 报告生成器 (待实现)
├── data/                              # 数据文件目录
│   ├── raw/                          # 原始数据
│   ├── processed/                    # 处理后数据
│   └── engineered/                   # 工程化特征
├── results/                           # 结果文件目录
│   ├── models/                       # 训练好的模型
│   ├── reports/                      # 分析报告
│   └── visualizations/               # 可视化图表
├── notebooks/                         # Jupyter笔记本
├── docs/                             # 文档目录
└── tests/                            # 测试文件目录
```

## 🔧 核心模块说明

### 1. 数据预处理模块 (`src/data_processing/`)
- **HTML数据提取器** (`html_extractor.py`): ✅ 已完成
  - 从HTML文件中提取表格数据
  - 支持批量处理多个文件
  - 输出JSON格式的分析结果
  
- **数据清洗器** (`data_cleaner.py`): ⏳ 待实现
  - 数据去重、缺失值处理
  - 异常值检测和处理
  - 数据格式标准化
  
- **数据验证器** (`data_validator.py`): ⏳ 待实现
  - 数据完整性检查
  - 数据质量评估
  - 一致性验证

### 2. 特征工程模块 (`src/feature_engineering/`)
- **特征选择器** (`feature_selector.py`): ✅ 已完成
  - 从168个特征中筛选8个核心特征
  - 支持统计方法和互信息方法
  - 生成特征重要性报告
  
- **特征构建器** (`feature_builder.py`): ⏳ 待实现
  - 构建148个高级特征
  - 特征变换和组合
  - 风险评分计算
  
- **特征变换器** (`feature_transformer.py`): ⏳ 待实现
  - 特征标准化和归一化
  - 对数、平方根等数学变换
  - PCA降维

### 3. 信号检测模块 (`src/signal_detection/`)
- **信号检测器** (`signal_detector.py`): ⏳ 待实现
  - 实现ROR、PRR、IC、EBGM方法
  - 识别36个潜在不良事件信号
  - 信号强度排序和筛选
  
- **统计方法** (`statistical_methods.py`): ⏳ 待实现
  - 各种信号检测统计方法
  - 置信区间计算
  - 显著性检验

### 4. 机器学习模块 (`src/machine_learning/`)
- **模型训练器** (`model_trainer.py`): ⏳ 待实现
  - 多种算法实现
  - 参数优化
  - 交叉验证
  
- **模型评估器** (`model_evaluator.py`): ⏳ 待实现
  - 性能指标计算
  - 模型比较
  - 特征重要性分析

### 5. 可视化模块 (`src/visualization/`)
- **图表生成器** (`chart_generator.py`): ⏳ 待实现
  - 生成各种分析图表
  - 支持多种图表类型
  - 自定义样式和主题
  
- **报告生成器** (`report_generator.py`): ⏳ 待实现
  - 生成分析报告
  - 支持多种格式
  - 自动化报告生成

## 📊 8个核心特征

基于项目分析，已识别的8个核心特征：

1. **`signal_strength_score`** - 信号强度综合评分
2. **`PRR_main_sqrt`** - PRR主要值的平方根变换
3. **`EBGM_main_sqrt`** - EBGM主要值的平方根变换
4. **`ROR_main_sqrt`** - ROR主要值的平方根变换
5. **`PRR_main_log`** - PRR主要值的对数变换
6. **`EBGM_main_log`** - EBGM主要值的对数变换
7. **`ROR_main_log`** - ROR主要值的对数变换
8. **`IC_main`** - IC主要值

## 🚀 使用方法

### 1. 安装依赖
```bash
pip install -r requirements.txt
```

### 2. 运行主程序
```bash
python main.py
```

### 3. 运行特定模块
```bash
# 数据预处理
python src/data_processing/html_extractor.py

# 特征选择
python src/feature_engineering/feature_selector.py
```

### 4. 查看帮助
```bash
python main.py --help
```

## 📈 项目进度

- ✅ **已完成**: 项目结构、HTML数据提取器、特征选择器、主程序
- ⏳ **进行中**: 核心模块框架搭建
- 🔄 **待实现**: 信号检测、机器学习建模、可视化、测试等模块

## 🎯 下一步计划

1. **完善核心模块**: 实现信号检测、机器学习建模等核心功能
2. **添加测试**: 为每个模块编写单元测试
3. **优化性能**: 提升数据处理和模型训练效率
4. **扩展功能**: 支持更多数据格式和分析方法
5. **文档完善**: 编写详细的API文档和用户指南

## 🤝 贡献指南

欢迎提交Issue和Pull Request！

1. Fork项目
2. 创建功能分支
3. 提交更改
4. 推送到分支
5. 创建Pull Request

## 📄 许可证

MIT License

---

*最后更新: 2025年1月*
