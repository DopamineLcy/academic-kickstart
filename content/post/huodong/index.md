---
title: '活动图'
# subtitle: 'Create a beautifully simple website in under 10 minutes :rocket:'
summary: 活动图（Activity Diagram）即UML中的流程图。用来表示系统中各种活动的次序。它既可用来描述用例的工作流程，也可以用来描述类中某个方法的操作行为
authors:
- admin
# tags:
# - Academic
# - 开源
# categories:
# - Demo
# - 教程
date: "2020-06-20T00:00:02Z"
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

&emsp;&emsp;用户进入页面后，可以通过点击地图标注或医院列表两种方式查看某医院的医疗压力情况。系统会根据用户的点击行为，获取焦点医院的名称及经纬度信息，通过获取医疗压力信息。此时地图聚焦焦点医院，具体行为有两点：一是将该医院的颜色设置为焦点色，并取消其他医院的焦点色。二是将网页的中心聚焦至该医院标注所在位置。继而医疗压力图表展示焦点医院的名称及医疗压力信息。

<!-- ## License

Copyright 2016-present [George Cushen](https://georgecushen.com).

Released under the [MIT](https://github.com/gcushen/hugo-academic/blob/master/LICENSE.md) license. -->
