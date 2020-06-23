---
title: '软件组织'
# subtitle: 'Create a beautifully simple website in under 10 minutes :rocket:'
summary: 软件组织方式描述了软件的设计模式，涵盖各个部分的设计及不同部分间的联系
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

&emsp;&emsp;系统采用C-S设计模式，主要分为后台数据处理和前端数据展示两部分。

&emsp;&emsp;后台数据处理部分主要分为两个过程。一是将出租车下客数据进行预处理，根据医院周围范围确定各个时段到各医院就诊的人数。经过预处理，我们可以得到时间—空间两个维度上的医疗负载信息。二是将与处理得到的医疗负载信息，利用时空循环深度神经网络，精准建模医院就诊需求的时空依赖，精准预测未来医院就诊需求的负载，并合理调配医疗资源。

&emsp;&emsp;前端数据展示我们采用了Web开发技术，基于当下流行的开源框架Vue，引用了百度地图API、Vuetify.js、Vue-chart等组件进行开发。地图组件作为Web界面的主体部分，基于百度地图API进行开发。从地图上可以直观看到各个医院的分布情况。通过点击地图上各个医院的标注点或医院列表组件，则唤起图表组件，展示医院在过去72小时的医疗负载变化曲线以及未来24小时的预测曲线。

<!-- ## License

Copyright 2016-present [George Cushen](https://georgecushen.com).

Released under the [MIT](https://github.com/gcushen/hugo-academic/blob/master/LICENSE.md) license. -->
