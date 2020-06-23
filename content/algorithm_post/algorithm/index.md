---
title: '核心算法'
# subtitle: 'Create a beautifully simple website in under 10 minutes :rocket:'
summary: 核心算法为时空循环神经网络，可以捕捉时间和空间两个维度上的特征。从而精准建模医院就诊需求的时空依赖，精准预测未来医院就诊需求的负载，并合理调配医疗资源。
authors:
- admin
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

**&emsp;&emsp;对于医院就诊需求处理与预测部分，我们选取厦门出租车2016、2017年九月轨迹数据集进行训练测试。其包括出租车乘客状态、经度、纬度、记录的时间点等信息。经过数据处理，我们得到了出租车的下客点。然后结合厦门市三级医院的边界数据，提取厦门市20家三级医院的下车点，得到各医院每小时乘坐出租车到达医院的就诊需求。**

**&emsp;&emsp;为了评估我们的预测结果，我们将数据集的前80%作为训练数据、后20%作为测试数据，并将医院就诊需求统计时间设定为1小时。我们使用时间序列预测中常用的两个指标(1)均方根误差(RMSE)和(2)平均绝对误差(MAE)来测量预测误差，定义如下：**


```tex
$$\gamma_{n} = \frac{ 
\left | \left (\mathbf x_{n} - \mathbf x_{n-1} \right )^T 
\left [\nabla F (\mathbf x_{n}) - \nabla F (\mathbf x_{n-1}) \right ] \right |}
{\left \|\nabla F(\mathbf{x}_{n}) - \nabla F(\mathbf{x}_{n-1}) \right \|^2}$$
```

renders as

$$\gamma_{n} = \frac{ \left | \left (\mathbf x_{n} - \mathbf x_{n-1} \right )^T \left [\nabla F (\mathbf x_{n}) - \nabla F (\mathbf x_{n-1}) \right ] \right |}{\left \|\nabla F(\mathbf{x}_{n}) - \nabla F(\mathbf{x}_{n-1}) \right \|^2}$$

## License

Copyright 2016-present [George Cushen](https://georgecushen.com).

Released under the [MIT](https://github.com/gcushen/hugo-academic/blob/master/LICENSE.md) license.
