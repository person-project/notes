### series

* type: 图形的类型，如： line， bar， pie等
* name: 系列名称，用于tooltip的显示，legend图例的筛选
* label： 图像上的文本标签，可用于说明图形的一些数据信息，其属性如下：两者的区别是一个是直接显示，一个是鼠标in的时候显示提示的具体信息
	* normal
		* show: 是否显示标签
		* position: 标签的位置，默认 inside，可以设置成 top，left等，还可以设置成百分比或者像素值 [10, 10], ['10%', '10%']
		* distance: 距离图形元素的距离。当position为字符描述值的时候有效，例如： top，left
		* rotate： 标签旋转，从-90~90
		* offset： 是否对文字进行偏移，例如[30, 40]表示文字在横向上偏移30，纵向上偏移40
		* formatter： 标签显示的内容，参数 params 是一个数据集
		* 样式设置 例如： color，fontStyle，fontWeight，fontFamily，fontSzie，align，verticalAlign，lineHeight，backgroundColor，borderColor等
	* emphasis 属性和normal一样可以参考上方

* itemStyle：图形样式，有normal和emphasis。normal是图形在默认状态下的样式，；emphasis是图形在高亮的状态下的样式。
	*  normal: 
		*  color: 图形条目的颜色