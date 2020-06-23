---
title: '核心算法'
# subtitle: 'Create a beautifully simple website in under 10 minutes :rocket:'
summary: 核心算法为时空循环神经网络，可以捕捉时间和空间两个维度上的特征。从而精准建模医院就诊需求的时空依赖，精准预测未来医院就诊需求的负载，并合理调配医疗资源。
authors:
- zhiyuan-wang
math: true
# tags:
# - Academic
# - 开源
# categories:
# - Demo
# - 教程
date: "2020-06-20T00:00:01Z"
# lastmod: "2019-04-17T00:00:00Z"
featured: false
draft: false

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder.
# Placement options: 1 = Full column width, 2 = Out-set, 3 = Screen-width
# Focal point options: Smart, Center, TopLeft, Top, TopRight, Left, Right, BottomLeft, Bottom, BottomRight
image:
  placement: 1
  # caption: 'Image credit: [**Unsplash**](https://unsplash.com/photos/CpkOjOcXdUY)'
  focal_point: ""
  preview_only: false

# Projects (optional).
#   Associate this post with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
#   E.g. `projects = ["internal-project"]` references `content/project/deep-learning/index.md`.
#   Otherwise, set `projects = []`.
projects: []
---

&emsp;&emsp;对于医院就诊需求处理与预测部分，我们选取厦门出租车2016、2017年九月轨迹数据集进行训练测试。其包括出租车乘客状态、经度、纬度、记录的时间点等信息。经过数据处理，我们得到了出租车的下客点。然后结合厦门市三级医院的边界数据，提取厦门市20家三级医院的下车点，得到各医院每小时乘坐出租车到达医院的就诊需求。

&emsp;&emsp;为了评估我们的预测结果，我们将数据集的前80%作为训练数据、后20%作为测试数据，并将医院就诊需求统计时间设定为1小时。我们使用时间序列预测中常用的两个指标(1)均方根误差(RMSE)和(2)平均绝对误差(MAE)来测量预测误差，定义如下：

<center>
$$
\begin{equation*}
RMSE=\sqrt{\frac{1}{n}\sum_{i=1}^{n}(y_i-\widehat{y_l})^2}\qquad
MAE=\frac{1}{n}\sum_{i=1}^{n}|y_i-\widehat{y_l}|
\end{equation*}
$$
</center>

&emsp;&emsp;我们将我们的方法与两组基准进行比较:机器学习算法和深度学习算法。我们选择了一些最先进的时间序列模型:ARIMA、SVR、FNN和LSTM作为基线方法。

* ARIMA:自回归综合移动平均线(ARIMA)广泛应用于时间序列分析。该方法将医院就诊需求建模为时间序列的值，不考虑相关随机变量的变化。
* SVR：支持向量回归(SVR)是支持向量机的一种回归方法。SVR使用与SVM相同的原理来最小化误差，个性化超平面，最大化类与类之间的边界。
* 前馈神经网络(FNN)是深度学习方法的基本架构。设计了具有两个隐层的神经网络，并利用Adam优化算法对网络权值进行迭代。
* LSTM:长短时记忆(LSTM)神经网络具有反馈连接，即记忆单元和遗忘门，在克服梯度消失和梯度爆炸问题的同时，捕获访问模式的时间依赖性。该基线使用带LSTM隐藏单元的递归神经网络预测医院就诊需求。

最终的测试结果如下表所示：
{{< figure library="true" src="result.png" title="表 不同模型测试结果" lightbox="true" >}}
&emsp;&emsp;将预测结果打印，可以发现我们提出的模型对数据的拟合效果更好，尤其体现在对于数量激增情况的预测更灵敏。

<!-- ## License

Copyright 2016-present [George Cushen](https://georgecushen.com).

Released under the [MIT](https://github.com/gcushen/hugo-academic/blob/master/LICENSE.md) license. -->
