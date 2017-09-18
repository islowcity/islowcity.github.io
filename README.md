<%@ page language="java" contentType="text/html; charset=UTF-8"
    pageEncoding="UTF-8"%>
<!DOCTYPE html PUBLIC "-//W3C//DTD HTML 4.01 Transitional//EN" "http://www.w3.org/TR/html4/loose.dtd">
<html>
<head>
<meta http-equiv="Content-Type" content="text/html; charset=UTF-8">

<script src="js/jquery-3.2.1.js"></script>

<title>Insert title here</title>
</head>
<body>
		<div>
		<input type="text" id="a" name="a"/> <input type="text" id="b" name="b"/>
		<button id="btn">提交</button>
		
		
		</div>


  <script>
	$("#btn").click(
		function(){	 
			$.post("Myfile.jsp",{
				a : $("#a").val(),
				b : $("#b").val()
		},
		function(data){
			document.getElementById("txt").innerHTML=data;
			alert(data);
		})
	});


</script>  

<!-- 
<script >
	$("#btn").click(function(){
		
		var res=showres();
		alert(res);
		
		
	});
	
	
	
	function showres(){
		var res="";
		$.ajax({
			type:"POST",
			url:"Myfile.jsp",
			data:{
				a:$("#a").val,
				b:$("#b").val
			},
			success:function(data){
				res=data;
			},
			async:true
			
		});
		
		return res;
		
	}





</script>







 -->




</body>
</html>



