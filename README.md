# RouteLineProject
折线图，均线图(日K图)，股市行情折线图，带有手指滑动交互；适用于上证指数，欧元汇率，黄金汇率。

###RouterLine

折线图，均线图(日K图)，股市行情折线图，带有手指滑动交互；适用于上证指数，欧元汇率，黄金汇率。

因为最开始的时候，没有想着把这两个控件开源，所以，从设计模式上来说，就没有更多地去考虑通用。这个工作，可以开发者自己根据需求，自己去改写。

折线图，实时变化图：

·提供了初始化的API，和增加点的方法。

·需要说明的是，一天的变化的点数，不可能全部描绘到手机屏幕的宽度上。所以，先让后台吧所得到的点，按照一天的总点数，平均到几分钟一个点左右。也就是说，后台 会从数据供应商那里拿来的数据，抛弃很多点的信息。这个是可以理解的。

· 因为数据量比较大，哪怕json解析，目前也是子线程解析。

### 均线图(日K图)：

·这个均值可以后台计算，也可以前台计算。项目中采用的是后台计算，前台展示(如果我记得还清楚的话)。