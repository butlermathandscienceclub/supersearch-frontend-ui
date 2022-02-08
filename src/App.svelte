<script>
function go(){
	var i = document.forms["in"]["in1"].value
	document.getElementById("if").src = `https://s-api.kellanb.repl.co/?search=${i}`;
		document.getElementById("if").style.display = "block"

		
document.getElementsByClassName("noif")[0].style.display = "none"
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
	<button on:click={go} id="b1">search!</button>
</div>
<iframe style="display:none" id="if"> </iframe>	
<footer>
<p>Made by <a href="http://bmsc.ga/" target="_blank">Butler Math and Science Club</a></p>
</footer>
</main>
<style>
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
   bottom:0;
   width:100%;
   height:60px;
}
</style>
