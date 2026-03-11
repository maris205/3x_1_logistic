# Spectral Analysis of the Transfer Operator in the Period-3 Logistic Sandbox

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.18957726.svg)](https://doi.org/10.5281/zenodo.18957726)

## 1. 介绍 (Introduction)
本仓库包含了论文 **"Spectral Analysis of the Transfer Operator in the Period-3 Logistic Sandbox: A Dynamical Heuristic for the $3x+1$ Problem"** 的所有数值模拟实验代码与作图脚本。

我们提出了一种计算物理与非线性动力学的跨学科新范式，将离散的 $3x+1$（Collatz 猜想）算术规则映射为处于周期 3 窗口（$\mu \approx 1.7549$）的连续 Logistic 动力学沙盒。本仓库中的代码完整复现了定制马尔可夫划分的构建、Perron-Frobenius 转移算子的本征谱求解、信息熵坍缩过程，以及 $10^8$ 级别大样本整数的停时衰减对齐实验。

## 2. 主要结果 (Main Results)
通过大样本的数值模拟与算子谱分析，我们不仅在现象学上重现了系统宏观统计特征，更在物理层面上证明了 $3x+1$ 的随机游走与一维耗散动力系统的暂态混沌属于同一个普适类（Universality Class）。

### 转移算子本征谱与不变密度 (Operator Eigenspectrum and Invariant Density)
下图展示了主特征向量对应的概率密度函数（呈现三根 Delta 分形尖峰）以及转移算子在复平面上的本征谱。
![Figure 6: Operator Eigenspectrum and Invariant Density](fig6.png)
*(对应论文 Figure 6)*

### 时间重整化与大样本衰减对齐 (Time Renormalization and Large-Sample Decay Alignment)
下图展示了经过时间标度因子重整化后的理论逃逸率（红线）与 $10^8$ 个大整数真实停时经验分布（蓝色散点）的完美平行契合。
![Figure 7: Time Renormalization and Large-Sample Decay Alignment](fig7.png)
*(对应论文 Figure 7)*

## 3. 代码说明 (Code Description)
本仓库的核心代码均以 Jupyter Notebook (`.ipynb`) 形式提供。由于全程只依赖 `numpy`, `matplotlib`, `scipy` 等标准科学计算库，您无需进行任何复杂的环境配置，可直接点击下方 **"Open in Colab"** 徽章，在浏览器中一键运行和复现所有结果。

* [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/maris205/3x_1_logistic/blob/main/Figure1-Customized%20Markov%20Partition%20.ipynb) **Figure1-Customized Markov Partition**: 基于不稳定不动点 $x^*$ 构建定制马尔可夫划分与拓扑沙盒。
* [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/maris205/3x_1_logistic/blob/main/Figure2-Establishment%20of%20the%20Topological%20Skeleton.ipynb) **Figure2-Establishment of the Topological Skeleton**: 绘制 Logistic 沙盒拓扑骨架及区间映射关系。
* [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/maris205/3x_1_logistic/blob/main/Figure3-Microscopic%20Grammar%20Emergence.ipynb) **Figure3-Microscopic Grammar Emergence**: 验证转移概率矩阵中“禁止字 11”的涌现及香农信息熵的坍缩过程。
* [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/maris205/3x_1_logistic/blob/main/Figure4-stopping%20time%20distribution%20histogram.ipynb) **Figure4-stopping time distribution histogram**: 对比连续轨迹暂态行为与真实大整数停时的右偏长尾分布。
* [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/maris205/3x_1_logistic/blob/main/Figure5-Invariant%20Measure.ipynb) **Figure5-Invariant Measure**: 计算百万次迭代后的不变概率密度及状态 0 与状态 1 的 2:1 测度积分。
* [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/maris205/3x_1_logistic/blob/main/Figure6-Operator%20Eigenspectrum%20and%20Invariant%20Density.ipynb) **Figure6-Operator Eigenspectrum and Invariant Density**: 采用高斯核扩散方法构建超大规模经验转移矩阵并求解本征谱。
* [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/maris205/3x_1_logistic/blob/main/Figure7-Time%20Renormalization%20and%20Large-Sample%20Decay%20Alignment..ipynb) **Figure7-Time Renormalization and Large-Sample Decay Alignment**: 在 $10^{11}$ 至 $10^{13}$ 值域内抽取一亿大整数进行衰减率对齐验证。

## 4. 论文引用 (Citation)
如果您在研究中使用了本仓库的代码或受到了本研究的启发，请引用我们的工作：

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
  url={[https://doi.org/10.5281/zenodo.18957726](https://doi.org/10.5281/zenodo.18957726)}
}
