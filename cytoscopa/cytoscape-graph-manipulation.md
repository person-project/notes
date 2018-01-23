### Graph manipulation
* cy.add() 向现有的数据中添加其他元素
	* 可以添加单个，以对象的形式添加
	* 可以添加多个，以数组的而形式添加
* cy.remove() 移除元素
	* 可以移除一个页面的元素
	* 可以移除一组元素
	
			例子：
				var arr = cy.elements("node[id > 'a']"); 移除id>a的一组元素 
				cy.remove(a);
				var a = cy.$('#a);
				cy.remove(a)
	* 元素选择器：
		* cy.nodes()
		* cy.edges()
		* cy.filter()
		
				例子：
				var filterArr = cy.filter(function(ele, i) {
					if (ele.isNode() && ele.data('id') > 'b') {
						return ele;
					} else {
						return false
					}
				});
		* cy.destroy() 显示的销毁cy实例
		* cy.container() 获取graph的页面元素
		* cy.center等同cy.centre 
			* cy.center()获取graph的中心元素
			* cy.center(ele)设置以ele元素为中心
		* cy.fit() 适应所有元素
		* cy.fit(cy.$('#a, #b)); 适应id是a和b的元素
		* cy.reset() 将graph重置为默认缩放级别和平移位置
		* cy.pan() 获取graph的位置
		* cy.pan( { x: 数值， y: 数值} ) 设置graph的布局位置
		* cy.panBy( { x: 数值， y: 数值} ) 设置graph的相对位置
		* cy.panningEnabled() graph是否可以被整个平移， true或者false
		* cy.userPainningEnabled() 获取是否启用了平移，如果传递参数是设置是否开启平移
		* cy.zoom() 获取缩放比例
		* cy.zoom(level, position, renderPosition) 设置缩放的比例，设置缩放的位置，设置缩放之后渲染的位置
		* cy.zommingEnabled(), userZoomingEnabled(), minZoom(), maxZoom()等设置
		* cy.viewport({zoom： 数值, pan： {x:数值， y:数值}) 设置视图的缩放和渲染的位置
		* cy.boxSelectionEnabled() 获取或者设置是否启动了pan的选择
		* cy.width()/height() 获取视图的宽度/高度
		* cy.extent()获取整个视图的高度，宽度，沿x轴开始和结束的位置，沿y轴开始和结束的位置
		* cy.autolock() 获取或设置nodes是否被锁定，锁定的话不能移动，但是整个pan可以移动
		* cy.resize() 调整graph尺寸和位置的时候调用
		* cy.animated() 获取或设置视图是否处于动画阶段,参数有：
			* zoom{level, position, renderPosition}
			* pan{x:, y:}
			* panBy
			* fit
			* center
			* duration 动画的时间
			* queue 
			* complete function 动画是否完成
			* step
			* easing 设置动画的类型
		* cy.animation()参数和上方基本相同
		* cy.delay() 设置动画的延迟时间
			 
				例子： 
				// 先完成上面的，延迟1s之后再去完成下面的
				cy
				  .animate({
				    fit: { eles: '#j' }
				  })
				
				  .delay(1000)
				
				  .animate({
				    fit: { eles: '#e' }
				  })
				;
		* cy.delayAnimation() 
		* cy.clearQueue() 清楚所有的动画队列
		* cy.layout（）等同 createLayout(), makeLayout()
			
					