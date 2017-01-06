# PCalendar
原生js实现日历组件
##实现功能
1、选取日期返回标准`date`对象；<br>
2、通过下拉列表和前后按钮切换年、月；<br>
3、自定义获得`date`后的回调方法；<br>
4、自定义`date`格式化方法；<br>
5、可选择显示方式:默认显示日历or默认隐藏、点击显示的选择日期组件；<br>
##使用
###配置格式
```
 config: {
   target: document.getElementById("container"),
   date:new Date(),
   type:"show",//or "hide"
   format:function(date){
     return nDate;//after format
   },
   callback:function(date){
   }
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
    type:"hide",//默认隐藏,点击显示
    format:function(date){
      return date.getFullYear()+"-"+~~(date.getMonth()+1)+"-"+date.getDate();;//YYYY-MM-DD
    },
    callback:function(date,format){
      console.log("标准格式:"+date);
      console.log("format:"+format);
    }
});
```

##待完善
1、选取时间段（暂时没有想到好的交互方式）；<br>
2、调用第三方api，获取节气、节日等信息；<br>
3、日程表、闹钟等扩展功能；<br>
