# GitHub上传指南
# GitHub Upload Guide

## 🚀 快速上传到GitHub

### 1. 创建GitHub仓库

1. 登录GitHub账号
2. 点击右上角 "+" 号，选择 "New repository"
3. 填写仓库信息：
   - **Repository name**: `megestrol-acetate-data-mining`
   - **Description**: `甲地孕酮数据挖掘项目 - 基于FAERS数据的药物安全性分析`
   - **Visibility**: 选择 Public 或 Private
   - **不要**勾选 "Add a README file" (我们已经有了)
4. 点击 "Create repository"

### 2. 本地Git初始化

```bash
# 进入项目目录
cd /path/to/甲地孕酮202503

# 初始化Git仓库
git init

# 添加远程仓库
git remote add origin https://github.com/YOUR_USERNAME/megestrol-acetate-data-mining.git
```

### 3. 添加文件到Git

```bash
# 添加所有文件
git add .

# 或者选择性添加核心文件
git add README.md
git add PROJECT_STRUCTURE.md
git add main.py
git add requirements.txt
git add .gitignore
git add src/
```

### 4. 提交更改

```bash
# 首次提交
git commit -m "Initial commit: 甲地孕酮数据挖掘项目

- 项目结构和核心模块
- HTML数据提取器
- 特征选择器 (8个核心特征)
- 主程序框架
- 完整的项目文档"

# 后续提交
git commit -m "feat: 添加数据预处理模块"
git commit -m "feat: 实现特征选择功能"
git commit -m "docs: 更新项目文档"
```

### 5. 推送到GitHub

```bash
# 推送到主分支
git branch -M main
git push -u origin main

# 后续推送
git push
```

## 📁 推荐的文件结构

### 核心文件 (必须上传)
```
megestrol-acetate-data-mining/
├── README.md                    # 项目说明
├── PROJECT_STRUCTURE.md         # 项目结构说明
├── main.py                      # 主程序
├── requirements.txt              # 依赖包
├── .gitignore                   # Git忽略文件
└── src/                         # 源代码
    ├── __init__.py
    ├── data_processing/
    │   ├── __init__.py
    │   └── html_extractor.py
    └── feature_engineering/
        ├── __init__.py
        └── feature_selector.py
```

### 可选文件 (根据需要上传)
```
├── data/                        # 数据文件 (如果不大)
├── results/                     # 结果文件 (如果不大)
├── notebooks/                   # Jupyter笔记本
└── docs/                        # 详细文档
```

### 不建议上传的文件
```
├── *.png                        # 图片文件 (通常很大)
├── *.jpg                        # 图片文件
├── *.pdf                        # PDF文件
├── *.xlsx                       # Excel文件
├── *.csv                        # CSV数据文件
├── __pycache__/                 # Python缓存
├── .DS_Store                    # macOS系统文件
└── 甲地孕酮202503/              # 原始数据目录
```

## 🔧 Git配置建议

### 1. 设置用户信息
```bash
git config --global user.name "Your Name"
git config --global user.email "your.email@example.com"
```

### 2. 设置默认分支名称
```bash
git config --global init.defaultBranch main
```

### 3. 设置行尾符处理
```bash
# Windows
git config --global core.autocrlf true

# macOS/Linux
git config --global core.autocrlf input
```

## 📝 提交信息规范

### 提交类型
- `feat`: 新功能
- `fix`: 修复bug
- `docs`: 文档更新
- `style`: 代码格式调整
- `refactor`: 代码重构
- `test`: 测试相关
- `chore`: 构建过程或辅助工具的变动

### 示例
```bash
git commit -m "feat: 添加信号检测模块"
git commit -m "fix: 修复特征选择器的数组维度问题"
git commit -m "docs: 更新README文档"
git commit -m "style: 统一代码格式"
```

## 🌟 仓库设置建议

### 1. 仓库描述
```
甲地孕酮(Megestrol Acetate)数据挖掘项目 - 基于FDA不良事件报告系统(FAERS)数据的药物安全性分析，包含数据预处理、特征工程、信号检测、机器学习建模和可视化等完整流程。
```

### 2. 标签 (Topics)
```
data-mining
drug-safety
pharmacovigilance
machine-learning
feature-engineering
signal-detection
python
pandas
scikit-learn
```

### 3. 仓库设置
- ✅ **Issues**: 启用
- ✅ **Wiki**: 启用
- ✅ **Discussions**: 启用
- ❌ **Projects**: 可选
- ❌ **Security**: 可选

## 📊 项目展示

### 1. 添加项目截图
在README.md中添加项目截图，展示：
- 数据流程图
- 核心特征热力图
- 模型性能对比图
- 信号检测结果图

### 2. 添加徽章
```markdown
![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)
![License](https://img.shields.io/badge/License-MIT-green.svg)
![Status](https://img.shields.io/badge/Status-Development-orange.svg)
```

### 3. 添加贡献者
```markdown
## 🤝 贡献者

<a href="https://github.com/YOUR_USERNAME/megestrol-acetate-data-mining/graphs/contributors">
  <img src="https://contributors-img.web.app/image?repo=YOUR_USERNAME/megestrol-acetate-data-mining" />
</a>
```

## 🚨 注意事项

### 1. 数据隐私
- 确保不包含敏感的个人医疗数据
- 使用示例数据或匿名化数据
- 在README中说明数据来源和用途

### 2. 文件大小
- 单个文件不要超过100MB
- 大文件使用Git LFS或外部存储
- 图片文件考虑压缩或使用链接

### 3. 许可证
- 选择合适的开源许可证
- 在README中明确说明
- 考虑项目的商业使用需求

## 📚 后续维护

### 1. 定期更新
```bash
# 每周更新
git add .
git commit -m "docs: 更新项目文档和依赖"
git push
```

### 2. 版本管理
```bash
# 创建版本标签
git tag -a v1.0.0 -m "第一个正式版本"
git push origin v1.0.0
```

### 3. 分支管理
```bash
# 创建开发分支
git checkout -b develop
git push -u origin develop

# 创建功能分支
git checkout -b feature/signal-detection
git push -u origin feature/signal-detection
```

---

## 🎯 上传检查清单

- [ ] 创建GitHub仓库
- [ ] 初始化本地Git仓库
- [ ] 添加核心代码文件
- [ ] 配置.gitignore
- [ ] 编写README.md
- [ ] 首次提交和推送
- [ ] 设置仓库描述和标签
- [ ] 添加项目截图
- [ ] 配置分支保护规则
- [ ] 邀请协作者 (如果需要)

完成以上步骤后，您的项目就成功上传到GitHub了！🎉

---

*最后更新: 2025年1月*
