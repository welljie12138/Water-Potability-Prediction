# 饮用水水质多指标预测与分类算法评估论文复现

## 一、 小组基本信息

* **小组名称：** 水质数据科学与机器学习探索小组
* **小组成员：**
  * 万雨捷 @welljie12138
  * 邓宇晴 @den-160
  * 李亚森 @ARSEN-4321
  * 唐成翰 @Downey888
* **项目名称：** 基于多维理化指标的饮用水水质机器学习预测全流程复现
* **原始开源参考：** [Water-Classification-Capstone-Project](https://github.com/annsam0115/Water-Classification-Capstone-Project)
* **本组作业仓库链接：** [https://github.com/welljie12138/Water-Potability-Prediction]

---

## 二、 项目简介

本项目聚焦于环境水质检测与公共健康领域，利用 Python 及数据科学工具链，复现并优化了基于 9 项核心水质理化指标（如 pH 值、硬度、硫酸盐、氯胺等）预测水质是否适合饮用（Potability）的机器学习建模全流程。

**本组复现的核心工作与优化：**
1. **数据预处理重构：** 修复了原开源代码中利用 Z-score 剔除异常值时因未处理 NaN 导致数据被清空的严重 Bug，改用特征均值插补（Mean Imputation）成功挽救了数据集。
2. **类别均衡处理：** 针对目标变量的不平衡问题，成功应用随机过采样（Random Over-sampling）消除先验偏差。
3. **多模型交叉验证：** 完整评估了逻辑回归（Logistic Regression）、K近邻（KNN）、决策树（Decision Tree）及随机森林（Random Forest）等分类器。验证了在复杂水质非线性特征下，集成学习（树模型）的压倒性优势。

**📁 仓库内容说明（数据与代码齐全）：**
* `Water_potability.ipynb`：本组复现、修复并添加了完整中文学术解读（Markdown）的核心代码文件。
* `water_potability.csv`：复现所需的核心水质数据集。
* `原项目文件.pdf`：复现的项目原始文章
* `复现评估报告.pdf`：汇总环境搭建与复现结果

## 三、 环境配置与复现步骤 (Python)

### 1. 环境配置信息
* **编程语言：** Python 3.9+ (推荐)
* **核心依赖包：**
  * `pandas` (数据清洗与特征处理)
  * `numpy` (数值计算)
  * `matplotlib` & `seaborn` (探索性数据分析与结果可视化)
  * `plotly` (交互式数据可视化)
  * `scikit-learn` (机器学习建模、评估与降维)
  * `xgboost` (梯度提升树高级集成模型)

### 2. 一键复现步骤 (Windows CMD / VS Code 终端)

```bash
# 1. 克隆本组作业仓库到本地 
git clone [https://github.com/welljie12138/Water-Potability-Prediction.git]

# 2. 进入项目目录 
cd Water-Potability-Prediction

# 3. 安装分析所需的全部依赖包
pip install pandas numpy matplotlib seaborn plotly scikit-learn xgboost

# 4. 运行复现脚本
# 请在 VS Code 或 Jupyter 环境中打开 `Water_potability.ipynb` 文件
# 点击顶部的 "全部运行 (Run All)" 即可一键输出所有图表与模型评估结果。
