# Calculator-app
_______________________________________________

<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Calculator</title>
  <style>
    body { display: flex; justify-content: center; align-items: center; height: 100vh; background: #eee; font-family: sans-serif; }
    .calculator { background: #fff; padding: 20px; border-radius: 10px; box-shadow: 0 5px 15px rgba(0,0,0,0.2); }
    input { width: 100%; font-size: 24px; padding: 10px; margin-bottom: 10px; }
    button { width: 22%; font-size: 20px; padding: 10px; margin: 5px; }
  </style>
</head>
<body>
  <div class="calculator">
    <input type="text" id="result" readonly>
    <br>
    <button onclick="append('1')">1</button>
    <button onclick="append('2')">2</button>
    <button onclick="append('3')">3</button>
    <button onclick="append('+')">+</button><br>
    <button onclick="append('4')">4</button>
    <button onclick="append('5')">5</button>
    <button onclick="append('6')">6</button>
    <button onclick="append('-')">-</button><br>
    <button onclick="append('7')">7</button>
    <button onclick="append('8')">8</button>
    <button onclick="append('9')">9</button>
    <button onclick="append('*')">*</button><br>
    <button onclick="append('0')">0</button>
    <button onclick="clearResult()">C</button>
    <button onclick="calculate()">=</button>
    <button onclick="append('/')">/</button>
  </div>

  <script>
    function append(char) {
      document.getElementById('result').value += char;
    }

    function clearResult() {
      document.getElementById('result').value = '';
    }

    function calculate() {
      try {
        document.getElementById('result').value = eval(document.getElementById('result').value);
      } catch {
        alert("Invalid Expression");
      }
    }
  </script>
</body>
</html>
