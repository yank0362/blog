## Jquery AJAX 的全局事件
- AjaxStart()和AjaxStop()的使用
*在jquery 1.8之后的版本，全局事件是作用在$(document)对象上的
```javascript
$().ready(function () {		
			$(document).ajaxStart(function(){
				
				$("#loading").show();//在ajax请求开始的时候，显示友好提示，提高用户体验
			});
			
			$("input:button").click(function(){
				$.ajax({
					"type":"POST",
					"url":"2.php",
					"data":$("#form1").serialize(),
					"dataType":"json",
					"success":function(data){
						console.log(data);
					},
					
				});


			$(document).ajaxStop(function(){
				
				$("#loading").hide();//当ajax请求结束时，隐藏提示
			});
			});
			//$.ajaxPrefilter(function (options){options.global = true;});
		});

```
## Ajax其它全局事件
方法名称 | 说明
------------ | -------------
ajaxComplete(callback) | Ajax请求完成时执行回调函数
ajaxError(callback) | Ajax请求发生错误时执行回调函数，捕捉到的错误可作为最后一个参数传递
ajaxSend(callback) | Ajax请求发送前执行回调函数
ajaxSuccess(callback) | Ajax请求成功时执行回调函数
