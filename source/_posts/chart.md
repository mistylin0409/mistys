---
title: 数据可视化设计思考
cover_index: http://github.com/mistylin0409/mistys/raw/pics/cover_index_chart.png
cover_detail: http://github.com/mistylin0409/mistys/raw/pics/cover_detail_chart.png
date: 2018-08-02
---

> 在健身房管理SaaS系统中，数据的统计和展示是对B端用户很有价值的一部分，健身房管理者需要通过数据来了解内部员工情况、场馆运营情况、会员消费情况等等，所以数据如何统计和展示将影响SaaS产品的使用效率，关系到付费客户对于产品的满意度和续费率。在设计数据可视化的项目中，我通过学习和实践总结了数据图表的一些设计方法。

<br/>

# Part 1 图表的使用场景

首先，在开始具体的图表设计之前要思考和明确的问题是，为什么使用图表？
图表在一些情况下很有价值，但并不是所有情况。图表可以帮助用户快速地将复杂、多样和庞大的数据量提取为单个或几个信息，以说明趋势、差异、构成和因果关系。所以如果当用户需要通过将大量数据转化为更容易理解的东西来解决问题的时候，可视化是一个很好的工具。但是，可视化在说明数据精确度这方面不是特别有效，这也不是可视化应该承载的功能，所以如果用户需要知道的是精确的值，这时候应该要使用表格或者其他形式来表达这些精确数据。
同时，数据可视化可以帮助用户：
1. **演示宣讲**
图表是一个帮助用户更好地讲述故事的手段，不同图形、表格、指标组合起来可以更好地评估事物的发展情况。所以将数据可视化设计为有效并且高效的沟通工具尤为重要。
<br/>
2. **探索数据价值**
很多时候，用户实际上还不知道通过数据可以得到那么多信息，反而是通过产品所提供的数据展示，让他们可以探索和分析数据，从而更好地利用数据，所以，让用户可以控制和访问他们的底层数据同样重要，引导帮助用户重视数据价值。

<br/>

# Part 2 图表的设计原则

1. **保证数据准确**
图表的价值在于其数据的有效性，一个小错误可能会使整个图表的完整性无效，数据准确性的一些错误也会损害产品的可信度。
<br/>
2. **根据表达重点选择图表形式**
在开始制作图表之前，明确想要表达的重点，是趋势、差异、构成还是因果关系，相同的数据可以有不同的表达形式，这取决于设计想表达的是什么内容。
<br/>
3. **提炼数据结论**
用一个简短的句子来表达数据中有价值的结论，引导用户关注图表的表达重点，比如：会员出勤率较昨日提升20%。
<br/>
4. **补充有必要的详细说明**
为了增加图表的可信度和透明度，图表的数据来源说明是有必要的，图表中应该包含获取原始数据的链接。
如果图表存在数据准确性的问题（比如四舍五入），还需要增加注释部分额外说明。
<br/>
5. **清晰易懂优先于美观程度**
图表可以很好看，可是过度的视觉元素和不必要的视觉效果反而会导致严重的误导后果。其中，颜色的使用应该尽可能地精简。

<br/>

# Part 3 图表类型的选择

专业领域的图表类型多达数十种，这里只简单梳理最常见的几种数据图表，包括各自的特点和适用场景。
![](http://github.com/mistylin0409/mistys/raw/pics/chart_table.png) 

## 折线图

**概述：**
简单的折线图展示单个或分组数据，最常见的是在横轴展示时间维度。
**适用于：**
表达重点为趋势
连续的数据
随时间变化的数据
多个数据在同一时间段内的变化
![](http://github.com/mistylin0409/mistys/raw/pics/chart_line.png) 

## 面积图

**概述：**
面积图本质上是添加了填充的折线图，通过这种方式表达总体趋势和关系的数量。最常见的面积图是“堆叠”类型，各部分数据堆叠展示，堆叠总和代表各部分数据组成的总体。
**适用于：**
表达一段时间，组成总体的各部分随时间变化的差异
![](http://github.com/mistylin0409/mistys/raw/pics/chart_area.png) 

## 柱状图/条形图

**概述：**
简单的柱状图展示单个或分组数据。柱状图的图形在视觉上引导用户关注各元素的相对差异，柱的顶部非常明显，最适合显示具体数值。
分组数据柱状图适用于表达在不同时间点多个数据随时间变化的差异。
堆叠柱状图用于展示总体和各部分随时间变化的差异。100%堆叠柱状图则是堆叠柱状图的变体，展示百分比而不是具体数值。
**适用于：**
比较同类型的几个数据间的差异
比较在不同时间点多个数据随时间变化的差异
比较总体和各部分随时间变化的差异
![](http://github.com/mistylin0409/mistys/raw/pics/chart_bar.png) 

## 饼图/圆环图

**概述：**
以饼图和圆环图显示各部分数据，图形上切片的大小与其表示的数据成比例，视觉上引导用户关注各部分的相对大小。
**适用于：**
表达构成整体的各部分组成关系
![](http://github.com/mistylin0409/mistys/raw/pics/chart_pie.png) 

<br/>

# Part 4 图表设计视觉要求

## 颜色

图表中的颜色用于识别数据和提高易读性，在具体设计中，可以根据数据类型选择配色。

1. **递增/递减数据**
如果数据带有递增/递减的关系，则可以使用渐变配色，通常是通过不透明度或明度来区别。
![](http://github.com/mistylin0409/mistys/raw/pics/chart_gradient.png)

2. **同类型数据**
如果数据之间没有增量关系，仅仅是不同分类数据，则可以使用平级配色。
![](http://github.com/mistylin0409/mistys/raw/pics/chart_flat.png)

3. **正面/负面数据**
如果数据带有明显的正面和负面关系，则可以使用语义配色，通常是红色和绿色。
![](http://github.com/mistylin0409/mistys/raw/pics/chart_biased.png)

颜色虽然可以提高易读性，但当颜色使用过多时，反而会降低易读性，这个时候可以采用图案来增加辨识元素。
![](http://github.com/mistylin0409/mistys/raw/pics/chart_pattern.png)

## 坐标轴

1. 坐标轴的有效处理和布局可以使数据更容易和快速地被理解
2. 但同时坐标轴也不可以太过引人注目，喧宾夺主
3. 当坐标轴刻度过多时，适当跳过显示，不要尝试将所有刻度挤在一起
4. 为了数据更好地展示，可以考虑坐标轴不从0开始

<br/>

> 参考链接：
Predix Design System: [https://www.predix-ui.com/#/design/data-vis](https://www.predix-ui.com/#/design/data-vis)
Nutanix Design System: [http://nutanix.design/2.0/#Diagrams_Colors](http://nutanix.design/2.0/#Diagrams_Colors)
Lexicon Design System: [https://lexicondesign.io/docs/patterns/Charts/charts.html](https://lexicondesign.io/docs/patterns/Charts/charts.html)
Opattern Design System: [https://ux.opower.com/opattern/how-to-charts.html](https://ux.opower.com/opattern/how-to-charts.html)
HubSpot Canvas Design System: [https://canvas.hubspot.com/graphs](https://canvas.hubspot.com/graphs)
Shopify Polaris Design System: [https://polaris.shopify.com/design/data-visualizations#navigation](https://polaris.shopify.com/design/data-visualizations#navigation)
Pega UX Design System: [https://design.pega.com/patterns-charting](https://design.pega.com/patterns-charting)
QuickBooks Design System: [https://designsystem.quickbooks.com/data-viz/](https://designsystem.quickbooks.com/data-viz/)