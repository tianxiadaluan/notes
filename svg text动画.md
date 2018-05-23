## 创建一个SVG标签 ##
    <svg id="svgForStroke" width="1280" height="938" xmlns="http://www.w3.org/2000/svg">
		<defs>
			<path d="m40.5,71.5c1,0 2,0 3,0c1,0 4.01498,-0.24437 6,0c4.09221,0.50378 7,1 10,1c6,0 9,0 13,0c2,0 3,0 7,0c1,0 3,0 4,0c2,0 3,0 7,0c2,0 4,0 7,0c1,0 4.82375,-0.48626 7,-1c1.9465,-0.4595 4.69344,-0.4588 6,-1c2.77164,-1.14805 4,-1 5,-1c1,0 2,0 3,0c1,0 2,0 3,0c1,0 2,0 3,0c1,0 2,0 4,0c1,0 2,0 4,0c1,0 1.69344,-0.4588 3,-1c0.92387,-0.38268 2,0 3,0c1,0 2,0 3,0c1,0 2,0 3,0l2,0" id="svg_section5" fill-opacity="null" stroke-opacity="null" stroke-width="1.5" stroke="#000" fill="none"/>
		</defs>
		<text x="0" y="0" style="stroke: #000000;" id="s555">
			<textPath xlink:href="#svg_section5" startOffset="-100%">M&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;O&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;M&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;O&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;M&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;O&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;M&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;O</textPath>
		</text>
	</svg>

> 这里是一个svg标签，包含了文字以及路径 各个参数属性自己查资料 这里只用到 startOffset 这个属性 这个属性表示着 路径文字的 起点

> path路径生成 例如：https://c.runoob.com/more/svgeditor/

## Javascript ##
    (function(){
		var ii = -100;
		timer = setInterval(function () {
			if(ii > 100){
				ii = -100;
			}else{
				ii += 1;
			}
			document.querySelector("#s555 textPath").setAttribute('startOffset', ii+'%');
		}, 50);
	})();

> 这里要用setAttribute获取startOffset的值，不要用jquery的attr 或者 prop ，不知道为什么获取不到，原因待查证