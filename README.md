# demo
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>简易时钟</title>
</head>
<body>
	<p>在页面显示一个时钟</p>
	<p id="demo"></p>
	<button id="e" onclick="star()" >开始计时</button>
	<button id="b" onclick="stop()" disabled="true">停止计时</button>
	<script>			

			function myTimer(){
				var d=new Date();/*获取当前时间*/
				var t=d.toLocaleTimeString();/*时间部分转换为字符串，并返回结果*/
				document.getElementById("demo").innerHTML=t;// 时间赋值给id为demo的标签并打印
				s=setTimeout('myTimer()',1000);
				
			}

			function star(){
				myTimer();
				document.getElementById("e").disabled=true;
				document.getElementById("b").disabled=false;
			}

			function stop(){
				clearTimeout(s);
				document.getElementById("e").disabled=false;
				document.getElementById("b").disabled=true;
			}
	</script>
</body>
</html>
