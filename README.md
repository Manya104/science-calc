# science-calc
for performing mathematical nd science calc
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Scientific Calculator</title>
    <style>
        .calculator {
            width: 300px;
            margin: 0 auto;
            text-align: center;
        }

        #display {
            width: 100%;
            padding: 10px;
            margin-bottom: 10px;
            font-size: 20px;
        }

        .buttons button {
            width: 50px;
            height: 50px;
            margin: 5px;
            font-size: 18px;
        }

        .buttons {
            display: grid;
            grid-template-columns: repeat(4, 1fr);
            gap: 5px;
        }
    </style>
</head>
<body>
    <div class="calculator">
        <input type="text" id="display" readonly>
        <div class="buttons">
            <button onclick="clearDisplay()">C</button>
            <button onclick="appendToDisplay('7')">7</button>
            <button onclick="appendToDisplay('8')">8</button>
            <button onclick="appendToDisplay('9')">9</button>
            <button onclick="appendToDisplay('/')">/</button>
            <button onclick="appendToDisplay('sin(')">sin</button>
            <button onclick="appendToDisplay('cos(')">cos</button>
            <button onclick="appendToDisplay('tan(')">tan</button>
            <button onclick="appendToDisplay('sqrt(')">sqrt</button>
            <button onclick="appendToDisplay('4')">4</button>
            <button onclick="appendToDisplay('5')">5</button>
            <button onclick="appendToDisplay('6')">6</button>
            <button onclick="appendToDisplay('*')">*</button>
            <button onclick="appendToDisplay('^')">^</button>
            <button onclick="appendToDisplay('(')">(</button>
            <button onclick="appendToDisplay(')')">)</button>
            <button onclick="appendToDisplay('log(')">log</button>
            <button onclick="appendToDisplay('1')">1</button>
            <button onclick="appendToDisplay('2')">2</button>
            <button onclick="appendToDisplay('3')">3</button>
            <button onclick="appendToDisplay('-')">-</button>
            <button onclick="appendToDisplay('exp(')">exp</button>
            <button onclick="appendToDisplay('pi')">π</button>
            <button onclick="appendToDisplay('0')">0</button>
            <button onclick="appendToDisplay('.')">.</button>
            <button onclick="appendToDisplay('+')">+</button>
            <button onclick="calculate()">=</button>
        </div>
    </div>
    <script>
        function appendToDisplay(value) {
            document.getElementById('display').value += value;
        }

        function clearDisplay() {
            document.getElementById('display').value = '';
        }

        function calculate() {
            let expression = document.getElementById('display').value;
            try {
                let result = eval(expression);
                document.getElementById('display').value = result;
            } catch (error) {
                alert('Invalid expression');
            }
        }
    </script>
</body>
</html>

