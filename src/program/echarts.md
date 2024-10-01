加载动画的显示与隐藏：

　　Echarts已经内置好了加载数据的动画，我们只需要在合适的时机显示或者隐藏即可。

　　显示加载动画：myCharts.showLoading()

　　隐藏加载动画：myCharts.hideLoading()

增量动画的使用：

　　不管是更改数据还是增加数据都要通过 myCharts.setOption 实现。

　　不用考虑数据到底产生了哪些变化。

　　Echarts会找到两组数据之间的差异然后通过合适的动画去表现数据的变化。

动画的常用配置：（在option中进行配置）

（1）开启动画：

animation:true;

（2）动画的时长：

animationDuration:5000（以毫秒为单位）

​      // 可以对不同元素产生不同的动画时长的效果

​      // arg打印的是数字，平均值、最大值、最小值、横坐标

​      animationDuration:function(arg){

​        return 2000*arg

​      },

（3）缓动动画： 

animationEasing:'bounceOut',

#### [series-pie.animationType](https://echarts.apache.org/zh/option.html#series-pie.animationType)：

'expansion' 默认沿圆弧展开的效果。

'scale' 缩放效果，配合设置 animationEasing='elasticOut' 

#### [DurationUpdate](https://echarts.apache.org/zh/option.html#animationDurationUpdate)

（4）动画元素的阈值：

animationThreshold:5,

　　单独形式的元素数量大于这个阈值时会关闭动画。

 this.chart.clear()配合

饼图的属性需要写在series里

 animation: true,

​    animationDuration: 10000,

​    animationEasing: 'cubicOut',