# Dialog

组件说明


        设计思路:业务组件，特有的动画效果，继承了KISSY Overlay组件


## 配置

包含[Overlay](http://docs.kissyui.com/1.2/docs/html/api/component/overlay/overlay.html#config-attributes-detail)的所有配置

* `start` {Object}
	
	起始点样式

	如：
	
        {
            left: 600,
            top: 100,
            opacity: 0
        }

* `end` {Object}

	终点样式
	
	如：
    
        {
	        left: 100,
	        top: 100,
	        opacity: 1
	    }

* `tmpl` {String}
	
	模板字符串，在dialog加载完成后会调用brix的Pagelet，初始化弹窗中的内容

* `data` {Object}
	
	数据源，和tmpl组合使用
	


## 方法

包含[Overlay](http://docs.kissyui.com/1.2/docs/html/api/component/overlay/overlay.html#methods-detail)的所有方法


## 事件

包含[Overlay](http://docs.kissyui.com/1.2/docs/html/api/component/overlay/overlay.html#events-detail)的所有事件	

## 代码示例
		
```javascript
KISSY.use("brix/gallery/dialog/", function(S, Dialog) {
    var config = {
        data:dropdown_data,
        tmpl:S.one("#tmpl_dropdown").html(),
        start:{
            left:100,
            top:600,
            opacity:0
        },
        end:{
            left:100,
            top:100,
            opacity:1
        },
        width:300,
        duration:0.3
    }
    var dialog = new Dialog(config);
    dialog.on('hide',function(){alert('hide')});
    dialog.on('show',function(){alert('show')});
    dialog.show();

    S.one('#aaa').on('click',function(){
        dialog.show();
    });
    S.one('#bbb').on('click',function(){
        dialog.hide();
    });
});
```




