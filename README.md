# Laboratorio_1
Trata sobre una calculadora que define tu edad solo poniendo tu año de nacimiento, 
para acerlo se utilizaron los codigos correspòndiente al HTML CSS y JavaScript
En el codigo HTML encontramos
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="estilos.css">
    <title>Práctica 1</title>
</head>
<body>
    <h1>Calcula tu nacimiento:</h1>
<div id="contenedor">
    <input type="text" id="entrada" placeholder="Ingresa tu edad">
    <button id="agregar">Calcular</button>
    <h2 id="respuesta"></h2>
</div>
<ul id="lista">
</ul>
    <script src="app.js"></script>
</body>
</html>

En el codigo CSS encontramos

body{
    background-color: #e8e8e8;
    font-family: Arial, sans-serif;
    margin: 0;
    padding: 20px;
}
h1{
    text-align: center;
    color: rgb(12, 0, 246);
}
#contenedor{
    text-align: center;
}
input{
    padding: 10px;
    font-size: 16px;
}
button{
    padding: 10px;
    cursor: pointer;
}

En el javascript encontramos 

const edad = document.getElementById("entrada");
const boton= document.getElementById("agregar");
const respuesta = document.getElementById("respuesta");

function mensaje(){
    //alert("Hicistes click en el boton");
    const nac = 2023-parseInt(edad.value);
    //alert("Nacistes en: " + nac);

    respuesta.innerHTML = "Tu fecha de nacimiento es: " + nac;
    edad.value="";
}
edad.addEventListener("keydown",(event)=>{
    if (event.key==="Enter"){
        mensaje();
    }
});
boton.addEventListener("click", mensaje);
