# Kwicks

组件说明


        设计思路:类似Switchable组件，用来内容展示


## 配置

包含[Brick](/etaoux/brix/tree/master/docs/brick.md)的所有配置

* `isVertical` {Boolen}
	
	切换方向，是否纵向，默认false（横向）

* `sticky` {Boolen}
	
	是否始终激活一个，默认false

* `activeIndex` {Number}
	
	默认激活的位置，只有当sticky为true时有效，默认为0

* `triggerType` {String}
	
	切换事件类型，默认mouseenter

* `activeCls` {String}
	
	激活样式，默认active

* `spacing` {Number}
	
	两个视图间距，默认0

* `easing` {String}
	
	动画效果，默认easeNone

* `duration` {Number} 单位s
	
	动画持续时间，默认0.3

* `max` {Number} 
	
	当个视图最大宽高度

		根据视图总大小和样式定义的默认大小，重新计算最小值，max的优先与min

* `min` {Number} 
	
	当个视图最大宽高度

		会根据视图总大小和样式定义的默认大小，重新计算最大值

* `autoplay` {Boolen} 
	
	是否自动播放

* `interval` {Number} 单位ms
	
	自动播放时间间隔	


## 方法


* `switchTo(i)`

    切换到某个视图

    * @param  {Number} i 要切换的项


* `start()`

    开始自动切换

* `stop()`

    停止自动切换


## 事件

	

## 代码示例
		
```javascript
KISSY.use("brix/gallery/kwicks/", function(S, Kwicks) {
    var kwicks1 = new Kwicks({
        el:'#ulkwicks1',//这里可以直接指定el，也可以是tmpl
        max : 205,
        spacing : 5,
        autoplay:true
    });
});
```




