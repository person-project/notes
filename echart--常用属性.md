###极坐标(polar)：
  * radiusAxis(极坐标系的径向轴)：
    * name: 坐标轴的名称
    * nameLoaction: 坐标轴名称显示位置 start，center/middle， end
    * nameTextStyle； 设置坐标轴名称的文字样式
    * nameRotate: 坐标轴名字旋转，角度值(number)
    * nameGap: 坐标轴线和坐标名称之间的距离(number)
    * boundaryGap: 坐标轴两边留白
    * axisLine: 坐标轴轴线相关设置，包括： show,lineStyle
    * axisLabel: 坐标轴刻度标签的相关设置，包括： show,inside(刻度标签的朝向)，rotate(刻度标签的旋转角度 -90~90)， formatter(支持字符串模板和毁掉函数两种形式)，color(标签文字的颜色)，fontStyle(文字问题的风格，normal，italic，oblique)，fontWeight,fontFamily,fontSize,align(left,center,right)
    * data 类目数据，可以是单纯的数组，也可以是数组包含对象，格式如下：
    
	    	// 所有类目名称列表
			data: ['周一', '周二', '周三', '周四', '周五', '周六', '周日']
			// 每一项也可以是具体的配置项，此时取配置项中的 `value` 为类目名
			data: [{
			    value: '周一',
			    // 突出周一
			    textStyle: {
			        fontSize: 20,
			        color: 'red'
			    }
			}, '周二', '周三', '周四', '周五', '周六', '周日']

* angleAxis(极坐标系的角度轴):
	* startAngle: 起始刻度的角度。默认90度  
	* boundryGap: 坐标轴两边留白
	* axisLine: 坐标轴轴线相关设置. show,lineStyle
	* axislabel: 坐标轴刻度标签的相关设置。show,inside,formatter,color等一个样式的设置
	* splitLine: 坐标轴在grid区域中的分割线，show，lineStyle
	* data 类目数据
	
	**注意在data都可以接受单纯的数组类型和数组包对象的数组类型可以对每一个坐标类目单独设置，设置的方法是：data[i].textStyle.样式名称以及具体的样式**

* radar(雷达图):
	* indictor:雷达图的指示器，用来制定雷达图的维度，还可以在里面对指示器的样式进行设置，color	 
	* center: 设置图像的坐标的中心位置，默认[50%，50%]
	* radius: 设置半径的大小，默认 75%
	* startAngle: 坐标系起始角度
	* name: 雷达图中每一个指示器名称的配置项，包括：show,formatter,color等一些样式设置属性
	* nameGap: 设置指示器名称和指示器轴之间的距离
	* shape: 绘制雷达图的类型，polygon(多边形，看数据的条数)，circle（圆形）
	* axisLine: 坐标轴轴线相关设置(从圆心向外的线)
	* axisTick: 坐标轴刻度相关设置
	* axisLabel: 坐标轴刻度标签的相关设置
	* splitNumber： 把整个区域分成几块(以圆环的形式分割)
	* splitArea: 根据默认或者上边splitNumber对区块进行设置，show，areaStyle
	
* dataZoom: 用于区域缩放
	* start,startValue: 数据窗口范围的设置，分别是：百分比，绝对值。 
	* end，endValue：同上
	* type： inside，side
	* disabled：是否停用组件的功能
	* xAxisIndex：设置dataZoom-inside组件控制的x轴
	

* visualMap：视觉映射组件
	* type： 定义是分段性(piecewise)还是连续性(continous)
	* splitNumber：自动平均分割成入几块
	* pieces：定义每一块的范围
	* min： 组件允许的最小值
	* max： 组件允许的最大值
	* range： 指定手柄对应的数值的位置
	* setOption：改变min，max，和range的值
	* calculable: 是否显示拖拽的手柄，也就是是否允许调整
	* realtime: 手柄拖拽的时候是否实时更新图标视图
	* precision：数据展示的小数精度。默认是0，无小数点
	* text: 两端的文本,[开头的文本， 结束的文本]
	* textGap: 文本和主题之间的距离，数值型
	* formatter: 设置两端位文本的显示文字
	* 
	