# JS-Best-Projects

https://hackr.io/blog/javascript-projects

10 Best Javascript Projects to Build your Skills [Javascript Examples]

Introduction 
One of the most popular scripting languages, JavaScript is used in all the web applications for validation, rendering dynamic content, interactive graphics and maps, and much more. Along with HTML and CSS, JS has the power to build complete, robust web applications. Because of JS, the user can interact with a web page and see all the interesting elements on the page. As we explore the projects, we will come to know-how js helps in building interactive web pages. Before that, let us quickly go through the important features of JS:

- Used on both client-side and server-side to create interactive web content.
- Greatly improves user experience by providing dynamic functionality.
- Light-weight language having object-oriented capabilities.
- Interpreted, open and cross-platform language.
- Seamless integration with Java and HTML.

<h3>Why JavaScript Projects?</h3>
JS is the heart of any web application. Good knowledge of JavaScript can get you a range of challenging and interesting career options like developing mobile and desktop apps, building dynamic websites from scratch, UI/UX designer, or even a full stack developer. If you know the basics of JavaScript, projects are your next step to add stars to your resume. If you don’t have any prior programming experience, you can take up basic JavaScript courses and then come back to these projects. If you follow a bit of HTML & CSS, you will understand most of the Javascript projects with the source code mentioned below.

<h3>Best JavaScript Projects for Beginners</h3>
There is a lot you can do with JavaScript, but we don’t want to overwhelm you with everything yet. We have listed the top JavaScript projects that can add value to your resume as well as a career:

<h3>1. JavaScript Calculator</h3>
We will use simple HTML, CSS, and make all the components work using basic JavaScript functions. To display buttons and numbers, we will use HTML, and add some beautification to them using CSS. To make the buttons perform the respective functions we will use JavaScript. The main function is eval(), which is a global JS function that solves JS codes. The display() function will display the selected number on the calculator screen. Note that the program will work only for mouse events. Here is the complete code:

<h4>HTML</h4>

```[html]
<div class="calculator">

  <input type="text" class="calculator-screen" value="" disabled />
  
  <div class="calculator-keys">
    
    <button type="button" class="operator" value="+">+</button>
    <button type="button" class="operator" value="-">-</button>
    <button type="button" class="operator" value="*">&times;</button>
    <button type="button" class="operator" value="/">&divide;</button>

    <button type="button" value="7">7</button>
    <button type="button" value="8">8</button>
    <button type="button" value="9">9</button>


    <button type="button" value="4">4</button>
    <button type="button" value="5">5</button>
    <button type="button" value="6">6</button>


    <button type="button" value="1">1</button>
    <button type="button" value="2">2</button>
    <button type="button" value="3">3</button>


    <button type="button" value="0">0</button>
    <button type="button" class="decimal" value=".">.</button>
    <button type="button" class="all-clear" value="all-clear">AC</button>

    <button type="button" class="equal-sign operator" value="=">=</button>

  </div>
</div>
```

<h4>CSS</h4>

```css
html {
  font-size: 62.5%;
  box-sizing: border-box;
}

*, *::before, *::after {
  margin: 0;
  padding: 0;
  box-sizing: inherit;
}

.calculator {
  border: 1px solid #ccc;
  border-radius: 5px;
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  width: 400px;
}

.calculator-screen {
  width: 100%;
  font-size: 5rem;
  height: 80px;
  border: none;
  background-color: #252525;
  color: #fff;
  text-align: right;
  padding-right: 20px;
  padding-left: 10px;
}

button {
  height: 60px;
  background-color: #fff;
  border-radius: 3px;
  border: 1px solid #c4c4c4;
  background-color: transparent;
  font-size: 2rem;
  color: #333;
  background-image: linear-gradient(to bottom,transparent,transparent 50%,rgba(0,0,0,.04));
  box-shadow: inset 0 0 0 1px rgba(255,255,255,.05), inset 0 1px 0 0 rgba(255,255,255,.45), inset 0 -1px 0 0 rgba(255,255,255,.15), 0 1px 0 0 rgba(255,255,255,.15);
  text-shadow: 0 1px rgba(255,255,255,.4);
}

button:hover {
  background-color: #eaeaea;
}

.operator {
  color: #337cac;
}

.all-clear {
  background-color: #f0595f;
  border-color: #b0353a;
  color: #fff;
}

.all-clear:hover {
  background-color: #f17377;
}

.equal-sign {
  background-color: #2e86c0;
  border-color: #337cac;
  color: #fff;
  height: 100%;
  grid-area: 2 / 4 / 6 / 5;
}

.equal-sign:hover {
  background-color: #4e9ed4;
}

.calculator-keys {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  grid-gap: 20px;
  padding: 20px;
}
```

<h4>JavaScript</h4>

```js
const calculator = {
  displayValue: '0',
  firstOperand: null,
  waitingForSecondOperand: false,
  operator: null,
};

function inputDigit(digit) {
  const { displayValue, waitingForSecondOperand } = calculator;

  if (waitingForSecondOperand === true) {
    calculator.displayValue = digit;
    calculator.waitingForSecondOperand = false;
  } else {
    calculator.displayValue = displayValue === '0' ? digit : displayValue + digit;
  }
}

function inputDecimal(dot) {
  if (calculator.waitingForSecondOperand === true) {
  	calculator.displayValue = "0."
    calculator.waitingForSecondOperand = false;
    return
  }

  if (!calculator.displayValue.includes(dot)) {
    calculator.displayValue += dot;
  }
}

function handleOperator(nextOperator) {
  const { firstOperand, displayValue, operator } = calculator
  const inputValue = parseFloat(displayValue);
  
  if (operator && calculator.waitingForSecondOperand)  {
    calculator.operator = nextOperator;
    return;
  }


  if (firstOperand == null && !isNaN(inputValue)) {
    calculator.firstOperand = inputValue;
  } else if (operator) {
    const result = calculate(firstOperand, inputValue, operator);

    calculator.displayValue = `${parseFloat(result.toFixed(7))}`;
    calculator.firstOperand = result;
  }

  calculator.waitingForSecondOperand = true;
  calculator.operator = nextOperator;
}

function calculate(firstOperand, secondOperand, operator) {
  if (operator === '+') {
    return firstOperand + secondOperand;
  } else if (operator === '-') {
    return firstOperand - secondOperand;
  } else if (operator === '*') {
    return firstOperand * secondOperand;
  } else if (operator === '/') {
    return firstOperand / secondOperand;
  }

  return secondOperand;
}

function resetCalculator() {
  calculator.displayValue = '0';
  calculator.firstOperand = null;
  calculator.waitingForSecondOperand = false;
  calculator.operator = null;
}

function updateDisplay() {
  const display = document.querySelector('.calculator-screen');
  display.value = calculator.displayValue;
}

updateDisplay();

const keys = document.querySelector('.calculator-keys');
keys.addEventListener('click', event => {
  const { target } = event;
  const { value } = target;
  if (!target.matches('button')) {
    return;
  }

  switch (value) {
    case '+':
    case '-':
    case '*':
    case '/':
    case '=':
      handleOperator(value);
      break;
    case '.':
      inputDecimal(value);
      break;
    case 'all-clear':
      resetCalculator();
      break;
    default:
      if (Number.isInteger(parseFloat(value))) {
        inputDigit(value);
      }
  }

  updateDisplay();
});
```

<h3>2. Hangman Game</h3>

Hangman is a well-known game, and one of our simple JS projects. You can develop it in a jiffy using JavaScript, HTML, and CSS. Note that the main functionality is defined using JS. HTML is for display, and CSS does the job of beautifying the contents. 

Many methods are defined in the JS code, so it may seem a bit complicated, but you will realize it is simple once you read the code thoroughly. You can also run the code and see the execution line by line.

<h4>HTML</h4>
<h4>CSS</h4>
<h4>JavaScript</h4>

<h3>3. Tic Tac Toe Game</h3>
JavaScript makes it easy to develop a Tic-Tac-Toe game yourself. You can look at the entire code here, and it explains how to build a 3x3 tic-tac-toe step by step. Then, you can later expand to NxN for your own practice and knowledge. The HTML and CSS for the project are quite simple. The author first starts with pseudocode and then goes on to explain each function individually.

<h4>HTML</h4>
<h4>CSS</h4>
<h4>JavaScript</h4>

<h3>4. Weather App</h3>
Weather apps are also popular JavaScript projects. Once you change the location name in this project, the weather display changes immediately without a page refresh. The UI is also quite sleek. 

Note that most weather apps use an API that gets the weather data. We will use the popular and most common API, OpenWeatherMap. 

Check out this Youtube video that explains the weather app code and functionality in detail. There are three files, as usual: index.html, main.js, and main.css. Although you can put all the code in a single file (HTML), it is more convenient to maintain separate files. 

<h4>HTML</h4>
<h4>CSS</h4>
<h4>JavaScript</h4>

<h3>5. </h3>

<h4>HTML</h4>
<h4>CSS</h4>
<h4>JavaScript</h4>


<h3>6. </h3>

<h4>HTML</h4>
<h4>CSS</h4>
<h4>JavaScript</h4>


<h3>7. </h3>

<h4>HTML</h4>
<h4>CSS</h4>
<h4>JavaScript</h4>


<h3>8. </h3>

<h4>HTML</h4>
<h4>CSS</h4>
<h4>JavaScript</h4>


<h3>9. </h3>

<h4>HTML</h4>
<h4>CSS</h4>
<h4>JavaScript</h4>
