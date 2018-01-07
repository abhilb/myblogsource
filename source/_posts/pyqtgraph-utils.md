---
title: pyqtgraph-utils
tags: PyQt
date: 2016-10-23 06:46:27
---

The other day I was working on an Python app that uses PyQt4 for its GUI and pyqtgraph for plotting. I wanted to render some simple geometric shapes on top of an image that is being displayed in a pyqtgraph plot widget Only then did I realize that there is no plot item readily available for such geometric shapes. Though there is an infinite line plot item available in pyqtgraph but that doesn't meet my requirement. In the documentation however there is an example of how to create custom plot items and it is pretty straight forward. Here is the [link](https://github.com/pyqtgraph/pyqtgraph/blob/4e9e75817fb0d2b5f6880278857621af30d7d0f1/examples/customGraphicsItem.py) to the example.

I have created a few plot item types based on that example and are available at this [link](https://github.com/abhilb/pyqtgraphutils). With these custom graphic items one can draw and line, circle or a rectangle as shown below.

~~~~
plotui = pg.PlotWidget()

item = pgutils.LineSegmentItem([10,20], [40,40])
plotui.addItem(item)

item1 = pgutils.CircleItem([10, 20], 50)
plotui.addItem(item1)

item2 = pgutils.RectangleItem([80, 80], [200, 100])
plotui.addItem(item2)

~~~~

I hope this post would be helpful for guys who google for "How to draw a circle/line segment/rectangle in pyqtgraph".
