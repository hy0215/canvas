<!DOCTYPE html>
<html>
<head>
	<meta charset ="utf-8"/>
	<title></title>
	<script type="text/javascript" src = "js/jquery-1.11.2.js"></script>
	<style type="text/css">
	*{
		padding:0;
		margin:0;
	}
	#outer{
		width:96%;
		height:200px;
		margin:0 auto;
		border:1px solid skyblue;
		display: flex;/*c3新属性 : 弹性盒模型*/
	}
	.inner{
		width:100px;
		height:100px;
		text-align: center;
		line-height:100px;
		font-size:32px;
		background-color: pink; 
		margin:auto;
		color:yellowgreen;
		animation:move 1s infinite normal;
	}
	@keyframes move{
		form{
			transform: rotate(0deg);
			}
			to{
				transform :rotate(360deg);
				border-radius: 50%;
			}
	}
	</style>
</head>
<body>
	<div id="outer">
		<div class="inner">1</div>
		<div class="inner">2</div>
		<div class="inner" id="third">3</div>
		<div class="inner">4</div>
		<div class="inner"><a href="">5</a></div>
		<div class="inner">6</div>
		<div class="inner"></div>
		<div class="inner">8</div>
		<div class="inner">9</div>
		<div class="inner">10</div>
	</div>
	<input type="text"/>
	<input type="text"/>

</body>
<script type="text/javascript">
//API 框架说明书：说明框架为你提供什么功能。提供哪些接口 ，接口如何使用。
	//实现可折叠菜单
	// $("h3").on("click",function(){$(this).siblings("li").show(300).end().closest("ul").siblings("ul").children("li").hide(300)});//链式语句
//选择器的使用 $(selector)表示选择器
   console.log($("#outer"));
   //jquery对象与dom对象不相同
   console.log($("#outer") === document.getElementById('outer'));//--->false
   //dom对象在页面中唯一的，多次选中返回的是同一dom节点
   console.log(document.getElementById('outer') ==document.getElementById('outer'));//--->true

   //每次使用选择器选中返回的jqurey对象返回的都是不相同的，所以，如果要多次操作相同的dom对象，建议使用变量持有jquery对象，而不是每次都选取
   console.log($("#outer") ===$("#outer"));//--->false


</script>
</html>
