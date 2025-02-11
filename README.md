Note : I did this on my sister's system(as Wipro system did not support) where she logged in her github account, that why it is showing her name( jessy getchiyal) later i changed it to my account but still her name is visible.

# calculator
It is an simple calculator for all the arithmetic operations.

## Project setup
```
npm install
```

### Compiles and hot-reloads for development
```
npm run serve
```

### Compiles and minifies for production
```
npm run build
```

### Lints and fixes files
```
npm run lint
```

### Customize configuration
See [Configuration Reference](https://cli.vuejs.org/config/).

**Code for Calculator**
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Calculator</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <div class="calculator">
        <input type="text" id="display" disabled>
        <div class="buttons">
            <button onclick="clearDisplay()">C</button>
            <button onclick="appendValue('/')">/</button>
            <button onclick="appendValue('*')">*</button>
            <button onclick="appendValue('-')">-</button>
            <button onclick="appendValue('7')">7</button>
            <button onclick="appendValue('8')">8</button>
            <button onclick="appendValue('9')">9</button>
            <button onclick="appendValue('+')">+</button>
            <button onclick="appendValue('4')">4</button>
            <button onclick="appendValue('5')">5</button>
            <button onclick="appendValue('6')">6</button>
            <button onclick="calculateResult()">=</button>
            <button onclick="appendValue('1')">1</button>
            <button onclick="appendValue('2')">2</button>
            <button onclick="appendValue('3')">3</button>
            <button onclick="appendValue('0')">0</button>
            <button onclick="appendValue('.')">.</button>
        </div>
    </div>
    <script src="script.js"></script>
</body>
</html>
<style>
  body {
    font-family: Arial, sans-serif;
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100vh;
    background-color: #f4f4f4;
}



.calculator {
    width: 250px;
    background: white;
    padding: 20px;
    border-radius: 10px;
    box-shadow: 0px 0px 10px rgba(0, 0, 0, 0.1);
}



#display {
    width: 100%;
    height: 50px;
    text-align: right;
    font-size: 1.5em;
    margin-bottom: 10px;
    padding: 5px;
}



.buttons {
    display: grid;
    grid-template-columns: repeat(4, 1fr);
    gap: 5px;
}



button {
    width: 100%;
    height: 50px;
    font-size: 1.2em;
    cursor: pointer;
    border: none;
    background: lightgray;
    border-radius: 5px;
}



button:hover {
    background: darkgray;
}



button:nth-child(4),
button:nth-child(12),
button:nth-child(16) {
    background: orange;
    color: white;
}
</style>
<script>
  function appendValue(value) {
    document.getElementById("display").value += value;
}



function clearDisplay() {
    document.getElementById("display").value = "";
}



function calculateResult() {
    try {
        document.getElementById("display").value = eval(document.getElementById("display").value);
    } catch {
        document.getElementById("display").value = "Error";
    }
}
</script>

