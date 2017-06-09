### JQuery闭包写法
```javascript
;(function($){
  //将jQuery对象传入到函数内部，$作为形参，所以，内部可以使用$代表jQuery
  var foo;
  var bar=function(){
  
  }
  $.BAR=bar;
})(jQuery);
```
### JQuery扩展对象方法$.extend()
1.使用$.extend()初始化参数options
```javascript
   function foo(options){
       options=$.extend({
          "name":"bar",
          "length":5,
          "dataType":"xml"//默认参数
       },options);//传入参数，合并替换
   
   }
   
   foo({"name","damon"});//替换
   foo();//默认
```
2.使用$.extend()扩展jQuery全局函数
```javascript
  ;(function($){
    $.extend({
      "ltrim":function(text){
           return (text||"").replace(/^\s+/g,"");
      },
      "rtrim":function(text){
           return (text||"").replace(/\s+$/g,"");
      }
    
    });
  
  })(jQuery);

  $.ltrim("      test    ");

```
3.使用$.extend()扩展String原型链方法
```
   $.extend(String.prototype,{
      "isInterger":function(){
          return (new RegExp(/^\d+$/).test(this));
      }
   });
   
   $("input").val().isInterger();
```
### Jquery插件写法$.fn.extend()使用
- 命名规则 jquery.插件名.js
- 闭包当中写插件代码
```
   ;(function($){
      $.fn.extend({
        "color":function(value){
          return this.css("color",value);//支持链式操作，这里的this不是dom对象而是jQuery对象，所以不用再次封装
        }
      })
   })(jQuery);
   $("div").color("red");//插件的方法，实际上也是插在了jQuery对象的原型链接上
```
