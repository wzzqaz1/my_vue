
<!DOCTYPE html>
<html>
	<head>
		<meta charset="UTF-8">
		<title></title>
		
		<script>
		function t1(){
             return pwdcheck()&& namecheck();
		}
		 function pwdcheck(){
			var pwd = document.getElementById("pwd")
			var pwdValue = pwd.value
		  if(pwdspan.length<6){
			var pwdspan=document.getElementById("pwdspan")
			pwdspan.innerHTML="密码不可少于6位"
			pwdspan.style="color:red"
		}else
			var pwdspan=document.getElementById("pwdspan")
			pwdspan.innerHTML="ok"
			pwdspan.style="color:green"	
		}
		function namecheck(){
			  var name = document.getElementById("name")
			  var nameValue = name.value
			if(nameValue.length<6){
			  var namespan=document.getElementById("namespan")
			  namespan.innerHTML="用户名不可少于6位"
			  namespan.style="color:red"
			}else{
				 var namespan=document.getElementById("namespan")
			     namespan.innerHTML="ok"
			     namespan.style="color:green"
			}
			
		}

			</script>
	</head>	
    <body> 
    	<form action="c.html" onsubmit="return t1()">
    	用户名：<input type="text" onblur="namecheck()" id="name"><span id="namespan"></span> <br />
    	密码：<input type="password" onblur="pwdcheck()" id="pwd"><span id="pwdspan"></span>  <br />
           <input type="submit" value="登录" /> 
	      </form>
	</body>
</html>
