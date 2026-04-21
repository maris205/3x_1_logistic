# 周期3 Logistic 沙盒中转移算子的谱分析

[🇨🇳 简体中文](readme_cn.md) | [🇬🇧 English](README.md)

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.18957726.svg)](https://doi.org/10.5281/zenodo.18957726)

## 1. 介绍
本仓库包含论文 **"Spectral Analysis of the Transfer Operator in the Period-3 Logistic Sandbox: A Dynamical Heuristic for the $3x+1$ Problem"** 的全部数值模拟代码与作图脚本。

我们提出了一种粗粒化瞬态动力学框架，将离散的 $3x+1$（Collatz 猜想）算术规则映射为处于周期3窗口（$\mu \approx 1.7549$）的连续 Logistic 动力学沙盒。代码完整复现了定制阈值划分的构建、Perron-Frobenius 转移算子本征谱求解、零模型对照实验、游程长度分布对比，以及停时衰减对齐实验。

## 2. 主要结果
通过大样本数值模拟、算子谱分析和严格的零模型对照，我们证明 Logistic 沙盒在**全局**停时分布上捕捉到了简单 forbidden-11 马尔可夫链无法复现的结构，同时诚实地展示了**局部**游程长度统计量更接近简单零模型。沙盒因此是一个具有明确成功与失败边界的部分代理模型。

### 转移算子本征谱与不变密度
![Figure 6: 算子本征谱与不变密度](fig6.png)
*(对应论文 Figure 6)*

### 时间重整化与大样本衰减对齐
![Figure 7: 时间重整化与大样本衰减对齐](fig7.png)
*(对应论文 Figure 7)*

## 3. 代码说明
核心代码以 Jupyter Notebook (`.ipynb`) 形式提供，依赖 `numpy`、`matplotlib`、`scipy`、`numba` 等标准库。点击 **"Open in Colab"** 徽章可在浏览器中一键运行。

### 原始图表 (1-7)

* [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/maris205/3x_1_logistic/blob/main/Figure1-Customized%20Markov%20Partition%20.ipynb) **Figure 1 - 定制阈值划分**：基于不稳定不动点 $x^*$ 构建定制阈值划分与拓扑沙盒。
* [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/maris205/3x_1_logistic/blob/main/Figure2-Establishment%20of%20the%20Topological%20Skeleton.ipynb) **Figure 2 - 拓扑骨架**：绘制 Logistic 沙盒拓扑骨架及区间映射关系。
* [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/maris205/3x_1_logistic/blob/main/Figure3-Microscopic%20Grammar%20Emergence.ipynb) **Figure 3 - 语法涌现**：验证"禁止字11"的涌现及香农熵坍缩。
* [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/maris205/3x_1_logistic/blob/main/Figure4-stopping%20time%20distribution%20histogram.ipynb) **Figure 4 - 停时分布**：对比连续暂态行为与真实大整数停时分布。
* [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/maris205/3x_1_logistic/blob/main/Figure5-Invariant%20Measure.ipynb) **Figure 5 - 不变测度**：计算不变概率密度及 2:1 测度比。
* [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/maris205/3x_1_logistic/blob/main/Figure6-Operator%20Eigenspectrum%20and%20Invariant%20Density.ipynb) **Figure 6 - 算子本征谱**：构建经验转移矩阵并求解本征谱。
* [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/maris205/3x_1_logistic/blob/main/Figure7-Time%20Renormalization%20and%20Large-Sample%20Decay%20Alignment..ipynb) **Figure 7 - 衰减对齐**：在 $[10^{11}, 10^{13}]$ 范围内抽取大整数验证衰减率对齐。

### 新增图表 (8-11)：鲁棒性验证、对照实验与游程分析

* [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/maris205/3x_1_logistic/blob/main/Figure8-Transfer%20Operator%20Convergence%20Study.ipynb) **Figure 8 - 收敛性研究**：变化网格 $N$ 和核宽 $\sigma/h$，对比高斯核与 Ulam 离散化，验证直接轨道存活率。
* [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/maris205/3x_1_logistic/blob/main/Figure8b-Epsilon%20Sensitivity%20Analysis.ipynb) **Figure 8b - $\varepsilon$ 敏感性**：测试瞬态衰减率对吸收邻域大小 $\varepsilon \in [10^{-5}, 5\times10^{-2}]$ 的鲁棒性。
* [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/maris205/3x_1_logistic/blob/main/Figure9-Null%20Model%20Control%20Experiment.ipynb) **Figure 9 - 零模型对照**：对比真实 Collatz、Logistic 沙盒和 forbidden-11 马尔可夫链的停时分布。
* [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/maris205/3x_1_logistic/blob/main/Figure10-Parameter%20Sensitivity%20and%20PWL%20Control.ipynb) **Figure 10 - $\mu$ 扫描与 PWL 对照**：在周期3窗口内扫描 $\mu$，并测试具有相同符号语法的分段线性映射。
* [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/maris205/3x_1_logistic/blob/main/Figure11-Run-Length%20Distribution%20Comparison.ipynb) **Figure 11 - 游程长度统计**：对比 Collatz、沙盒和零模型的连续偶数步游程长度分布（$\nu_2$-赋值类比）。

## 4. 论文引用
如果您使用了本仓库代码或受到本研究启发，请引用：

**APA 格式:**
> Wang, L. (2026). Spectral Analysis of the Transfer Operator in the Period-3 Logistic Sandbox: A Dynamical Heuristic for the $3x+1$ Problem (v1.0). Zenodo. https://doi.org/10.5281/zenodo.18957726

**BibTeX 格式:**
```bibtex
@misc{wang2026spectral,
  title={Spectral Analysis of the Transfer Operator in the Period-3 Logistic Sandbox: A Dynamical Heuristic for the 3x+1 Problem},
  author={Wang, Liang},
  year={2026},
  publisher={Zenodo},
  version={v1.0},
  doi={10.5281/zenodo.18957726},
  url={https://doi.org/10.5281/zenodo.18957726}
}
```
