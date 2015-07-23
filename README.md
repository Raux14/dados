
<!DOCTYPE html>
<html>
<head>
	<title></title>
<style type="text/css">

ul{
	margin: 0;
}
li{
	display: inline;
	margin-right: 10px;
}
img{
	width: 100px;
	height: 100px;
}

</style>

<script type="text/javascript">
/* numero aleatorio
var valor;
for(var i = 1; i<=30; ++i){
	valor = Math.floor(1 + Math.random() * 6);
	document.write(valor);
}
*/
// imagenes aleatorias

var imagenDado1;
var imagenDado2;
var imagenDado3;
var imagenDado4;

function iniciar(){
	var boton = document.getElementById("botonTirar");
	boton.addEventListener("click", tirarDados, false);
	imagenDado1 = document.getElementById("dado1");
	imagenDado2 = document.getElementById("dado2");
	imagenDado3 = document.getElementById("dado3");
	imagenDado4 = document.getElementById("dado4");
}

function tirarDados(){
	establecerImagen(imagenDado1);
	establecerImagen(imagenDado2);
	establecerImagen(imagenDado3);
	establecerImagen(imagenDado4);
}

function establecerImagen(imgDado){
	var valorDado = Math.floor(1 + Math.random() * 6);
	imgDado.setAttribute("src", "dado" + valorDado + ".jpg");
	imgDado.setAttribute("alt", "imagen de un dado con " + valorDado + " punto(s)");
}
window.addEventListener("load", iniciar, false);

</script>
</head>
<body>

<form action = "#">
	<input id="botonTirar" type="button" value="Tirar dados"  >
</form>


<ol>
	<li><img id="dado1" src="dado1.jpg" alt="imagen en blanco"></li>
	<li><img id="dado2" src="dado2.jpg" alt="imagen en blanco"></li>
	<!--<li><img id="dado3" src="dado3.jpg" alt="imagen en blanco"></li> -->
	<!--<li><img id="dado4" src="dado4.jpg" alt="imagen en blanco"></li> -->
</ol>
</ol>

</body>
</html>
