<script>
	window.isd = 0;

function go(){
	var i = document.forms["in"]["in1"].value
		if (window.isd == 1){	document.getElementById("if").src = `https://s-api.kellanb.repl.co/?search=${i}&dark=2`;
		document.getElementById("if").style.display = "block"
}
else
{	document.getElementById("if").src = 
	
	`https://s-api.kellanb.repl.co/?search=${i}`;
		document.getElementById("if").style.display = "block"
}		
document.getElementsByClassName("noif")[0].style.display = "none"
document.getElementById("foot").style.display = "none"
}
function dark(){
if(window.isd==0)
{document.querySelector(":root").style.color = "white"
document.querySelector(":root").style.backgroundColor = "black"
window.isd = 1;

}
else if(window.isd==1){
document.querySelector(":root").style.color = "black"
document.querySelector(":root").style.backgroundColor = "white"
window.isd = 0;
}

}

</script>
<main>
<div class="noif">
	<h1>super search!</h1>
	<br>
	<p> press search. Please don't press enter</p>
	<form name="in">
		<input name="in1" placeholder="search the web!" id="in1" > 
	</form>
	<br>
	<button on:click={go} id="b1">search! </button>
</div>
<iframe style="display:none" id="if"> </iframe>	
<footer id="foot"> 
<p>Made by <a href="http://bmsc.ga/" target="_blank">Butler Math and Science Club</a></p>
<button on:click={dark}>toggle dark</button>


</footer>
</main>
<style>
	:root{
		--se :  "🔎"
	}
main{
		display:block; 

	text-align:center;
}
iframe{
    position: fixed;
    top: 0px;
    bottom: 0px;
    right: 0px;
    width: 100%;
    border: none;
    margin: 0;
    padding: 0;
    overflow: hidden;
    z-index: 999999;
    height: 100%;
}
#b1:hover{
	color:white;
	background-color:black;

}
#in1:focus{
		color:white;
	background-color:black;

}
footer {
   position:absolute;
   bottom:50px;
   width:100%;
   height:60px;
}
#in1{  width: 50%;
height:30px;border-radius: 25px;padding:12px 20px
}
#b1{
	width:90px;
	height:40px;
}
#b1::after{
	content: var(--se)
}
</style>
