### cytoscape.js

* contianer: 图形所要展示的区域
* element： 元素数组，内部可以进行一些具体的设置，
	* group： nodes,edges
	* data： 
		* id： 每一个element的id，如果没有的话会自动分配
		* parent：
		* source:
		* target:
	* position： 元素的位置 {x: , y:  } 
	* selected： 元素是否被选中，默认false
	* selectable： 元素是否可以被选择，默认true
	* locked： 元素的位置是否可以移动，默认false
	* grabbable： 元素是否可以被抓取
	* classes： 元素所添加的class类，‘foo bar’添加了两个class类
	* renderedPosition： 可以把点渲染在一个特定的位置
	* layout:
	* style:
	