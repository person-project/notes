###Ele - Data###

* ele.data() 可以获取ele元素的所有数据
* ele.data({ show: '修改数据' }) 可以添加或者修改ele的数据，但是id，source, target, parent 是不能修改的	
	
		可以参考如下例子：
	
		var j = cy.$('#j');

		j.data('weight', 60);
		
		j.data({
		  name: 'Jerry Jerry Dingleberry',
		  height: 176
		});
		先根据id获取这个元素，之后可以设置/获取这个元素绑定的数据
* ele.removeData() 移除ele上的所有的可变数据
* ele.removeData(属性名称) 移除ele上的某个可变属性的值
* ele.id() 获取元素的id值
* ele.json() 获取元素相关的一个josn格式的信息
* ele.json( eleJosn ) 设置元素的可变的属性
* ele.group() 获取元素的组， 例如点击线段的时候回弹出edges
* ele.isNode() / ele.idEdge() / edge.isLoop() 线是否是循环 / edge.isSimple()
* node.position()等同modelPosition(),point() 获取node的位置信息，格式： {x:656.7852593996914，y:216.56541151876414}
* node.position( 参数 ) 获取某个维度的值
* node.position( key, value ) 设置某个维度的值
* node.position({key: value, key: value}) 设置多个维度的值
* nodes.positions(function(node, i) {}) 可以设置多个点的位置
* 