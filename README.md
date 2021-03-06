## 简体与繁体互相转换

### 使用方法

```
<script type="text/javascript" src="./js/language.js"></script>
```



### 使用情况一：只有一个按钮

```
new fontConversion({
    btnNum:1,//按钮数量
    elIsId: false,//绑定的按钮是否为id类型，两种类型id--true，class--false
    bindEl:{
        transBtn:'changeBtn',
    },
    useText:false,//是否使用按钮文字-简体/繁体，默认不使用false
    callBack:function(){
    //回调函数
    }
});
```

### 使用情况二：两个按钮

```
new fontConversion({
    btnNum:2,//按钮数量
    elIsId: false,//绑定的按钮是否为id类型，两种类型id--true，class--false
    bindEl:{
        toFanBtn:'fanti',//转换成繁体
        toJianBtn:'jianti',//转换成简体
    },
    useText:false,//是否使用按钮文字-简体/繁体，默认不使用false
    callBack:function(){
    //回调函数
    }
});
```

**注意：绑定的元素不需要加#或者.**



### 页面自动转换

```
new fontConversion({
    autoChange:{
		autoType: 'jian_fan',//jian_fan-简体转换繁体，fan_jian-繁体转换简体
	},
});
```



### 获取当前字体的状态

```
外部js要获取当前字体状态时使用window.curFontType()获取状态
返回以下值：
0--简体
1--繁体
```

有其他需求的可自行增加或者修改