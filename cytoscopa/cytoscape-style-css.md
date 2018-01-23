###edge
* style
	* css
		* curve-style: 两个点之间的连接线的形状，选项有，bezier, unbundled-bezier,haystack,segments
		* control-point-distance:控制连接线的弧的大小
		* control-point-weights：控制连接线和点连接的部分的弧度
		* source-arrow-shape: 控制箭头的形状，同target-arrow-shape，箭头指向源或者指向目标
		* source/target -arrow-color: 控制箭头的颜色
		* source/target-distance-from-node：设置两个端点距离node之间的距离
		* edge-text-rotation: 文本的方向autorotate是跟随线的方向, none, 或者设置一个集体的旋转角度
		* min-zoomed-font-size： 设置当文本小于设置的值得时候，则不显示文本只显示线条
		* source-text-rotation/target-text-rotation 目标和源的文本的旋转角度

**定义样式可以有三种形式，第一种：以字符串的形式，第二种以对象的形式，第三种以函数的形式**

例子： 

	  cytoscape({
	  container: document.getElementById('cy'),
	
	  // 以字符串的形式
	
	  style: 'node { background-color: green; }' 
	
	  // 以对象的形式
		style: [
	    {
	      selector: 'node',
	      style: {
	        'background-color': 'red'
	      }
	    }
	  ]

	  // 以函数的形式
	  style: cytoscape.stylesheet()
	    .selector('node')
	      .style({
	        'background-color': 'blue'
	      })
	});

   * 如果想重新设置样式可以，
   
   			cy.style()
               .resetToDefault()
				.selector('node')
					.style('background-color', 'red')
					.update()//没有这个方法新定义的样式是不会生效的
* 覆盖原来定义的样式，代码同上
* 以对象的形式重设样式

		cy.style()
		  .fromJson([
		    {
		      selector: 'node',
		      style: {
		        'background-color': 'red'
		      }
		    }
		  ])
		  .update();

* label:
	* source-label:展示源头的线的文本
	* target-label: 展示目标的线的文本
	* 样式的一些设置，如 color，text-opacity, font-family, font-size, font-style, font-weight, text-transform
	* text-max-width: 设置文本的最大的宽度，要配合text-wrap使用
	* text-wrap： none、ellipsis
	* text-halign： 文本在node上水平方向的位置设置，left，center，right
	* text-valign: 文本在node上垂直方向上的位置设置，top，center，bottom
	* text-margin-x: node下方的文本会沿着x轴移动，同 text-margin-y
	* source-text-margin-x/target-text-margin
	* transition animation过渡动画效果
	 