+++
widget = "blank"
headless = true  # This file represents a page section.
active = true  # Activate this widget? true/false
weight = 50  # Order that this section will appear in.


# ... Put Your Section Options Here (title etc.) ...
title = "核心算法"
[design]
  # Choose how many columns the section has. Valid values: 1 or 2.
  columns = "2"
+++
&emsp;&emsp;对于医院就诊需求处理与预测部分，我们选取厦门出租车2016、2017年九月轨迹数据集进行训练测试。其包括出租车乘客状态、经度、纬度、记录的时间点等信息。经过数据处理，我们得到了出租车的下客点。然后结合厦门市三级医院的边界数据，提取厦门市20家三级医院的下车点，得到各医院每小时乘坐出租车到达医院的就诊需求。

&emsp;&emsp;为了评估我们的预测结果，我们将数据集的前80%作为训练数据、后20%作为测试数据，并将医院就诊需求统计时间设定为1小时。我们使用时间序列预测中常用的两个指标(1)均方根误差(RMSE)和(2)平均绝对误差(MAE)来测量预测误差，定义如下：

