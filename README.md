# PCalendar
原生js实现日历组件
##实现功能
1、选取日期返回标准`date`对象；<br>
2、通过下拉列表和前后按钮切换年、月；<br>
3、自定义获得`date`后的回调方法；<br>

##使用
###配置格式
```
 config: {
 	target: document.getElementById("container"),
 	date:new Date(),
 	callback:function(date){}
 }
 ```
###示例
```
var container = document.getElementById("container");
```
```
var cal = new PCalendar({
    target:container,
    date:new Date(),
    callback:function(date){
      //blabla
    }
});
```

##待完善
1、选取时间段（暂时没有想到好的交互方式）；<br>
2、调用第三方api，获取节气、节日等信息；<br>
3、日程表、闹钟等扩展功能；<br>
