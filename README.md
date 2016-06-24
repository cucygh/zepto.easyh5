# zepto.easyh5

[![issues](https://img.shields.io/github/issues/webzhongwang/zepto.easyh5.svg)](https://github.com/webzhongwang/zepto.easyh5/issues) [![forks](https://img.shields.io/github/forks/webzhongwang/zepto.easyh5.svg)](https://github.com/webzhongwang/zepto.easyh5/network) [![stars](https://img.shields.io/github/stars/webzhongwang/zepto.easyh5.svg)](https://github.com/webzhongwang/zepto.easyh5/stargazers)

快速构建html5移动应用

## 功能介绍
实现移动端的单页全屏滚动，参数自定义，预定义移动端开发常用的CSS3动画。

## 依赖包

[Zepto](https://cdnjs.cloudflare.com/ajax/libs/zepto/1.1.6/zepto.min.js)

## 在线演示

[在线演示](http://webzhongwang.github.io/zepto.easyh5/)

## 安装

###### 项目克隆
	git clone git@github.com:webzhongwang/zepto.easyh5.git
###### npm安装
	npm install zepto.easyh5 --save-dev

## 快速上手

#### 全屏滚动
###### HTML

	<div id="easyh5" class="easyh5">
		<section class="easyh5-page">Page 1</section>
		<section class="easyh5-page">Page 2</section>
		<section class="easyh5-page">Page 3</section>
		<section class="easyh5-page">Page 4</section>
	</div>

##### JS
	
	$('#easyh5').easyh5();

##### 参数

	//默认参数
    var defaults = {
        start: 0,           // 初始化时显示第几屏 默认从0开始
        duration: 300,      // 滚动到下一屏所需的时间，单位（毫秒），默认300毫秒
        loop: true,         // 是否可循环激动，默认是true
        auto: false,        // 是否自动滚屏
        dir: 'top',         // 自动滚屏的方向，只有auto值为true时有效，取值:top|bottom
        autoDuration: 5,    // 自动滚屏的时间间隔，只有auto值为true时有效，单位（秒）
        showPageNum: true,  // 是否显示当前页是第几页，从第一页开始计数
        pageNumPlace: 'right-bottom',   // 显示页码的位置，只有当showPageNum为true时有效，取值:left-top|left-bottom|right-top|right-bottom
        audio: false,       // 是否添加背景音乐，目前暂不支持safari浏览器和极少部份android平台上的游览器
        showAudio: true,    // 是否显示背景音乐图标，只有当audio为true时生效
        audioSrc: 'http://webzhongwang.github.io/zepto.easyh5/files/bg1.mp3',  // 背景音乐地址，只有当audio为true时生效
        volume: 0.8,        // 控制背景音乐声音大小，取值[0,1.0]，默认0.8
        width: 320,         // 设置内容区域宽度 默认320px
        height: 480,        // 设置内容区域高度 默认480px
        persent: 0.15       // 滑动屏幕的临界值时触发换页 默认是屏幕高度的15%
    };

#### 动画设置
	
	<div id="easyh5" class="easyh5">
	    <section class="easyh5-page s1">
	    	<h1 class="a" anim-class="bounceInRight animated" delay="0.4">title</h1>
	    	<div class="b" anim-class="slideInUp animated" delay>content</div>
	    	<p class="c " anim-class="fadeIn animated" delay="0.8" duration="2.5">footer</p>
	    </section>
	    <section class="easyh5-page s2">
	    	<h1 class="a " anim-class="bounceInRight animated" delay="0.3">2title</h1>
	    	<p class="c" anim-class="bounceInLeft animated" delay="0.7">2footer</p>
	    </section>
	</div>
	
delay用于设置动画延迟执行的时长，单位（秒），无需延迟执行动画的元素也一定要加上空的delay属性；duration用于设置动画时长，单位（秒）；anim-class代表动画类名

#### 关于Animate.css

项目集成了[Animate.css](https://daneden.github.io/animate.css/)，这里要感谢Animate.css的作者 [Daniel Eden](https://github.com/daneden/) 提供优秀的CSS3动画。所有动画都需加上基础的动画设置类“animated”。

* bounce
* flash
* pulse
* rubberBand
* shake
* headShake
* swing
* tada
* wobble
* jello
* bounceIn
* bounceInDown
* bounceInLeft
* bounceInRight
* bounceInUp
* bounceOut
* bounceOutDown
* bounceOutLeft
* bounceOutRight
* bounceOutUp
* fadeIn
* fadeInDown
* fadeInDownBig
* fadeInLeft
* fadeInLeftBig
* fadeInRight
* fadeInRightBig
* fadeInUp
* fadeInUpBig
* fadeOut
* fadeOutDown
* fadeOutDownBig
* fadeOutLeft
* fadeOutLeftBig
* fadeOutRight
* fadeOutRightBig
* fadeOutUp
* fadeOutUpBig
* flipInX
* flipInY
* flipOutX
* flipOutY
* lightSpeedIn
* lightSpeedOut
* rotateIn
* rotateInDownLeft
* rotateInDownRight
* rotateInUpLeft
* rotateInUpRight
* rotateOut
* rotateOutDownLeft
* rotateOutDownRight
* rotateOutUpLeft
* rotateOutUpRight
* hinge
* rollIn
* rollOut
* zoomIn
* zoomInDown
* zoomInLeft
* zoomInRight
* zoomInUp
* zoomOut
* zoomOutDown
* zoomOutLeft
* zoomOutRight
* zoomOutUp
* slideInDown
* slideInLeft
* slideInRight
* slideInUp
* slideOutDown
* slideOutLeft
* slideOutRight
* slideOutUp




