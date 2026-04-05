<!DOCTYPE html>
<html>
<head>
    <title>Electrónica Fácil</title>
    <style>
        body{
            font-family: Arial;
            text-align: center;
            background-color: #0f172a;
            color: white;
        }
        h1{
            color: #38bdf8;
        }
        .box{
            background: #1e293b;
            padding: 20px;
            border-radius: 10px;
            width: 300px;
            margin: auto;
        }
        input{
            padding: 5px;
            margin: 5px;
        }
        button{
            padding: 10px;
            background: #38bdf8;
            border: none;
            color: black;
            cursor: pointer;
        }
    </style>
</head>

<body>

<h1>🔌 Aprende Electrónica y Arduino</h1>

<div class="box">
    <h2>Calculadora Ley de Ohm</h2>

    Voltaje (V): <br>
    <input id="V"><br>

    Resistencia (Ω): <br>
    <input id="R"><br>

    <button onclick="calc()">Calcular</button>

    <p id="res"></p>
</div>

<script>
function calc(){
    let V = document.getElementById("V").value;
    let R = document.getElementById("R").value;

    if(R == 0){
        document.getElementById("res").innerHTML = "Error: R no puede ser 0";
    } else {
        let I = V / R;
        document.getElementById("res").innerHTML = "Corriente = " + I + " A";
    }
}
</script>

</body>
</html>
