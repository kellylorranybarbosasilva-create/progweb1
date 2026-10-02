<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Aprovação</title>
</head>
<body>
    
     <h1>Confira status de Aprovação</h1>
    <p>Digite o nome do(a) estudante e sua média:

    </p>
<form>
    <label for="n4">Nome:</label>
        <input id="n4"
        type="text">
        <br><br>

        <label for="n5">Média:</label>
        <input id="n5"
        type="number"
        min="0" max="10" step="0.1">
        <br><br>

 <button type="button"
    onclick="StatusFinal()">
        Status Final
    </button>

    </form>



    <h3>Resultado</h3>
    <p>
       <span id="nomeEstudante">-</span> está
       <span id="resultado">-</span> 
    </p>


<script src="../js/Aprovação.js"></script>


</body>
</html>

function verAprovacao() {
  let nome = 
document.getElementById("nome").value;

  let media = 
Number(document.getElementById("media").value);

   let resultado;

   if (media>=7.0) {
    resultado = "Aprovado(a)!"
   }
   else {
    resultado = "Reprovado!"
   }

document.getElementById("nomeEstudante").textContent = nome;
document.getElementById("resultado").textContent = resultado
