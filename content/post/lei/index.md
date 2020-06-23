---
title: '类图'
# subtitle: 'Create a beautifully simple website in under 10 minutes :rocket:'
summary: 类图(Class Diagram)是最常用的UML图。类图体现了各个类的结构以及类与类之间的组织关系
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

**&emsp;&emsp;本项目主要由地图主体、医院、地图标注、医疗压力信息、医疗压力图表五个类组成。地图主体与地图标注相互配合，展示各个医院的地理位置以及标注当前焦点医院。医院位置信息依赖于医院类。通过地图标注，可以触发相应的医疗压力图表，展示真实以及预测的就诊人数信息。其中医院名称依赖于医院类，过去72小时的真实就诊人数和未来24小时的预测就诊人数信息依赖于医疗压力信息类。**

## License

Copyright 2016-present [George Cushen](https://georgecushen.com).

Released under the [MIT](https://github.com/gcushen/hugo-academic/blob/master/LICENSE.md) license.
