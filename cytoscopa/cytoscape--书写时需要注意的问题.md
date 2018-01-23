**在初始化的时候可以把所有的样式都写在style中，包括node，edge原本的样式和选中之后的样式，对于一些其他的样式可以通过动态添加class类的形式对元素单独定义**

可以参考如下代码：
	
	style: [{
		selector: 'node.green', //定义node中带有green类node
		style: {
			'background-color': 'green' //具体定制green所特有的样式
		}
	}]
	
	// 在触发某个事件的时候动态的给某个元素添加class类
	cy.nodes().on('grab', function(event) {
		event.target.addClass('green') // 添加class，移除的时候使用 removeClass('class名')
	})


