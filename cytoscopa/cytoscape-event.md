* cy 引用cytoscape的整个实例
* target 引发事件的核心
* type 触发事件的事件类型
* namespace 事件名称
* timeStamp时间戳
* name： 这只布局的类型，包括，
	* null（所有的点都会渲染在0，0的位置）
	* random 把点随意的渲染在视图中
	* preset 将点渲染在预设的位置
	* grid 将点放在间隔良好的网格中
	* circle 圆形布局
	* concentric 
	* breadthfirst 根据等级制度布局
	* cose 
* cy.layout 可以设置一些事件 
	* start() 开始运行layout，同 stop()
	* on()等同于 bind(), listen(), addListener() 绑定事件，参数：
		* events 事件的名称
		* data 传递的参数
		* function 回调
	* promiseOn( events )，等同于pon(). 里面绑定的是要触发的事件的名称.例子如下：

			var layout = cy.layout({ name: 'random' });
	
			layout.pon('layoutstop').then(function( event ){
			  console.log('layoutstop promise fulfilled');
			});
			
			layout.run();
	*  one（）layout开始的时候运行的一次性事件，参数如下：
		*  events 事件的名称
		*  data
		*  function（event）
	*  removeListener()等同于 off（），unbind(), unlisten()，移除对某个事件的监听
	*  emit（）等同trigge(), 主动触发某个事件，参数：
		*  events
		*  extraParams 
*  Animations 事件，绑定在某个元素上

		例如： 
			var jAni = cy.$('某个要绑定事件的元素').animation({
			  style: {
			    'background-color': 'red',
			    'width': 75
			  },
			  duration: 1000
			});
			
			jAni.play();
	* paly() 触发绑定的动画事件	
	* playing() 获取动画是否正在播放
	* 获取,设置 动画的进度的事件有：
		* ani.progress() 动画的百分比进度
		* ani.progress( progress ) 设置动画的百分比，progress 从 0 - 1
		* ani.time()获取动画进行的时间，以毫秒为单位
		* ani.time( time ) 设置动画进行的时间
		* ani.rewind() 重新开始动画
		* ani.fastforward() 快进到动画结束

				例子： 
				var jAni = cy.$('#j').animation({
				  style: {
				    'background-color': 'red',
				    'width': 75
				  },
				  duration: 1000
				});
				
				// 先把动画进度设置到50%，再开始播放
				jAni.progress(0.5).play();
		* ani.pause() 暂停动画
		* ani.stop() 暂停动画，并从队列中删除该任务
		* ani.completed()同ani.complete() 获取动画是否播放完成
		* ani.promise() 
		* ani.promsie( 动画的事件相符的名称 ) ，有 completed, complete, frame
		* ani.apply()在当前进度中应用动画，
		
			 	例子:
				var jAni = cy.$('#j').animation({
				  style: {
				    'background-color': 'red',
				    'width': 75
				  },
				  duration: 1000
				});
				
				jAni.progress(0.5).apply();
		* ani.applying() 获取动画是否当前应用
		* ani.reverse() 反转动画
		
	**等多例子参考： [http://js.cytoscape.org/#style/labels](http://js.cytoscape.org/#style/labels "animation属性和实例参考网址")**

** animate用于设置整个画布的动画，如设置fit，zoom，animation用于设置某一个元素的动画效果 **
