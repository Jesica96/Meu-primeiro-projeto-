# Meu-primeiro-projeto-
Uma calculatora simples 

<!DOCTYPE html>
<html LANG="pt--br">

<head>
  <meta charset="UTF-8">
  <meta http-equiv="X-UA-Compatible" content="ie=edge">
  <meta name="viewport" content="initial-scale=1">
  <title> calculadora simples</title>
  <link rel="stylesheet" href="style.css">
  <script src="calculadora.js">
  </script>
</head>

<body>
  <div class="fundo">
    <h1> Jésica </h1>
    <div class="Calculadora">
      <h2>Calculadora</h2>
      <p id="resultado"></p>
      <table>
        <tr>
          <td> <button class="botao" onclick="clean() ">C</button></td>
          <td><button class="botao" onclick="back() ">
              <</td>

          <td> <button class="botao" onclick="insert('/')"> / </button></td>
          <td> <button class="botao" onclick="insert('*')">*</button></td>
        </tr>
        <td><button class="botao" onclick="insert('1')">1</button></td>
        <td><button class="botao" onclick="insert('2')">2</button></td>
        <td><button class="botao" onclick="insert('3')">3</button></td>
        <td><button class="botao" onclick="insert('-')">-</button></td>
        </tr>
        <tr>
          <td><button class="botao" onclick="insert('4')">4</button></td>
          <td><button class="botao" onclick="insert('5')">5</button></td>
          <td><button class="botao" onclick="insert('6')">6</button></td>
          <td><button class="botao" onclick="insert('+')">+</button></td>
        </tr>
        <tr>
          <td><button class="botao" onclick="insert('7')">7</button></td>
          <td><button class="botao" onclick="insert('8')">8</button></td>
          <td><button class="botao" onclick="insert('9')">9</button></td>
          <td rowspan="2"><button class="botao" style="height 100px;" onclick="Calcular() ">=</button></td>
        </tr>
        <tr>
          <td colspan="2"><button class="botao" style="width:106px;" onclick="insert('0') ">0</button></td>
          <td><button class="botao" onclick="insert('.')">.</button></td>
        </tr>
      </table>
    </div>
  </div>

</body>

</html>






* {
  margin: 0;
  padding: 0;
}
.fundo {
  background-image: linear-gradient (25deg, rgb(125, 77, 186) .rgb(79, 45, 162));
  height: 100vh;
  color: white;
  font-family: arial, helvetica, sans serife;
  text-aling: right;
}
.Calculadora {
  position: absolute;
  background-color: rgba(0, 0, 0, 0.9);
  top: 50%;
  left: 50%;
  tranform: translate(-50%, -50%);
  border-radius: 13px;
}
.botao {
  width: 50px;
  height: 50px;
  font-size: 25px;
  cursor: pointer;
  margin: 3px;
  background-color: rgb(32, 32, 32);
  border: none;
  color: white;
}
.botao:hover {
  width: 207px;
  background-color: white;
  height: 30px;
  margin: 6px;
  font-size: 26px;
  color: black;
  text-align: right;
  padding: 5px;
}




function insert (num)
{
    var numero = document.getElementById('resultado').innerHTML;
    document.getElementById('resultado').innerHTML = numero + num;
}
function clean()
{
    document.getElementById('resultado').innerHTML = "";
}
function back()
{
    var resultado = document.getElementById('resultado').innerHTML;
    document.getElementById('resultado').innerHTML = resultado.substring(0, resultado.length -1);
}
function calcular()
{
    var resultado = document.getElementById('resultado').innerHTML;
    if(resultado)
    {
        document.getElementById('resultado').innerHTML = eval(resultado);
    }
    else
    {
        document.getElementById('resultado').innerHTML = "Nada..."
    }
}
