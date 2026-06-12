# 威斯康辛州乳腺癌分类实验
**Breast Cancer Wisconsin Classification**

## 项目结构

```
project/
├── data/
│   └── data.csv          ← 从 Kaggle 下载后放到这里
├── notebook/
│   └── experiment.ipynb  ← 完整实验代码
├── app/                  ← 打包程序（可选）
├── report/               ← 实验图表自动保存到此处
└── README.md
```

## 数据集下载

前往 Kaggle 下载 `data.csv`：  
 https://www.kaggle.com/datasets/uciml/breast-cancer-wisconsin-data

下载后放到 `data/data.csv`。

## 环境依赖

```bash
conda install pandas numpy matplotlib seaborn scikit-learn jupyter
pip install xgboost imbalanced-learn
```

## 运行步骤

1. 下载数据集，放到 `data/data.csv`
2. 进入 `notebook/` 目录，启动 Jupyter：
   ```bash
   cd notebook
   jupyter notebook experiment.ipynb
   ```
3. 按顺序运行所有 Cell

## 分类方法

| 方法 | 说明 |
|------|------|
| Logistic Regression | 逻辑回归，线性分类基准 |
| SVM (RBF Kernel) | 支持向量机，RBF 核非线性分类 |
| Random Forest | 随机森林，集成学习 |
| XGBoost | 梯度提升树，高精度集成方法 |

## 实验输出图表

运行后，所有图表自动保存到 `report/` 目录：

| 文件名 | 内容 |
|--------|------|
| fig_01_class_distribution.png | 类别分布饼图+条形图 |
| fig_02_boxplot_mean_features.png | 特征箱线图 |
| fig_03_correlation_heatmap.png | 特征相关性热力图 |
| fig_04_kde_top6_features.png | Top6 特征 KDE 分布 |
| fig_05_pairplot.png | Pair Plot |
| fig_06_metric_comparison.png | 多指标对比条形图 |
| fig_07_confusion_matrices.png | 四模型混淆矩阵 |
| fig_08_roc_curves.png | ROC 曲线对比 |
| fig_09_feature_importance.png | 随机森林特征重要性 |
| fig_10_learning_curves.png | 学习曲线 |
| fig_11_cv_comparison.png | 5折交叉验证对比 |