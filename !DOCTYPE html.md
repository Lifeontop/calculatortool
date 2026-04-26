<!DOCTYPE html>

<html lang="en">

<head>

&#x20; <meta charset="UTF-8">

&#x20; <title>Simple Calculator</title>

&#x20; <style>

&#x20;   body {

&#x20;     display: flex;

&#x20;     justify-content: center;

&#x20;     align-items: center;

&#x20;     height: 100vh;

&#x20;     background: #1e1e1e;

&#x20;     font-family: Arial, sans-serif;

&#x20;   }



&#x20;   .calculator {

&#x20;     background: #2c2c2c;

&#x20;     padding: 20px;

&#x20;     border-radius: 15px;

&#x20;     box-shadow: 0 0 15px rgba(0,0,0,0.5);

&#x20;   }



&#x20;   #display {

&#x20;     width: 100%;

&#x20;     height: 60px;

&#x20;     font-size: 24px;

&#x20;     margin-bottom: 10px;

&#x20;     text-align: right;

&#x20;     padding: 10px;

&#x20;     border: none;

&#x20;     border-radius: 10px;

&#x20;     background: #000;

&#x20;     color: #0f0;

&#x20;   }



&#x20;   .buttons {

&#x20;     display: grid;

&#x20;     grid-template-columns: repeat(4, 70px);

&#x20;     gap: 10px;

&#x20;   }



&#x20;   button {

&#x20;     height: 60px;

&#x20;     font-size: 20px;

&#x20;     border: none;

&#x20;     border-radius: 10px;

&#x20;     cursor: pointer;

&#x20;     background: #444;

&#x20;     color: white;

&#x20;   }



&#x20;   button:hover {

&#x20;     background: #666;

&#x20;   }



&#x20;   .equal {

&#x20;     background: #28a745;

&#x20;   }



&#x20;   .equal:hover {

&#x20;     background: #3ddc6b;

&#x20;   }



&#x20;   .clear {

&#x20;     background: #dc3545;

&#x20;   }



&#x20;   .clear:hover {

&#x20;     background: #ff5c70;

&#x20;   }

&#x20; </style>

</head>

<body>



<div class="calculator">

&#x20; <input type="text" id="display" disabled>



&#x20; <div class="buttons">

&#x20;   <button onclick="clearDisplay()" class="clear">C</button>

&#x20;   <button onclick="append('/')">÷</button>

&#x20;   <button onclick="append('\*')">×</button>

&#x20;   <button onclick="append('-')">−</button>



&#x20;   <button onclick="append('7')">7</button>

&#x20;   <button onclick="append('8')">8</button>

&#x20;   <button onclick="append('9')">9</button>

&#x20;   <button onclick="append('+')">+</button>



&#x20;   <button onclick="append('4')">4</button>

&#x20;   <button onclick="append('5')">5</button>

&#x20;   <button onclick="append('6')">6</button>

&#x20;   <button onclick="calculate()" class="equal">=</button>



&#x20;   <button onclick="append('1')">1</button>

&#x20;   <button onclick="append('2')">2</button>

&#x20;   <button onclick="append('3')">3</button>

&#x20;   <button onclick="append('.')">.</button>



&#x20;   <button onclick="append('0')" style="grid-column: span 4;">0</button>

&#x20; </div>

</div>



<script>

&#x20; let display = document.getElementById("display");



&#x20; function append(value) {

&#x20;   display.value += value;

&#x20; }



&#x20; function clearDisplay() {

&#x20;   display.value = "";

&#x20; }



&#x20; function calculate() {

&#x20;   try {

&#x20;     display.value = eval(display.value);

&#x20;   } catch {

&#x20;     display.value = "Error";

&#x20;   }

&#x20; }

</script>



</body>

</html>

