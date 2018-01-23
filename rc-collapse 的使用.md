# rc-collapse 的使用
在引入 Collapse和Panel的同时要把，css的样式文件引入 

Collapse属性：
		* activeKey: 当前活跃的Panel
		* defaultActiveKey： 默认在第一次打开页面的时候打开的Panel
		* accordion： 百叶窗效果，默认是false，设置为true的话每次只能打开一个Panel，当打开其他的面板的时候其他打开的Panel默认关闭，设置为false可以同时打开多个Panel
		* onChange：当点击的时候出发的事件，接受key(当前点击的Panel的key值)
Panel属性：
		* header：panel显示的内容  