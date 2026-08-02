<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h1><a href="https://hackr.io/blog/javascript-projects">JS-Best-Projects</a></h1>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h2>13+ Best Javascript Projects to Build your Skills [Javascript Examples]</h2>
<blockquote>
  <h3><a href="#ch1">1. Calculator</a></h3>
  <h3><a href="#ch2">2. Hangman Game</a></h3>
  <h3><a href="#ch3">3. Tic-Tac-Toe Game</a></h3>
  <h3><a href="#ch3b">3b. Again, Tic-Tac-Toe Game</a></h3>
  <h3><a href="#ch4">4. Weather App</a></h3>
  <h3><a href="#ch5">5. Music Events</a></h3>
  <h3><a href="#ch5b">5b. Drums</a></h3>
  <h3><a href="#ch6">6. Form Validation</a></h3>
  <h3><a href="#ch7">7. Photo Details Display</a></h3>
  <h3><a href="#ch8">8. Build an Interactive Landing Page</a></h3>
  <h3><a href="#ch9">9. Single Page Application</a></h3>
  <h3><a href="#ch10">10. To-Do List</a></h3>
  <h3><a href="#ch11">11. JS Rock, Paper, Scissors Game</a></h3>
  <h3><a href="#ch12">12. JS Countdown Timer</a></h3>
  <h3><a href="#ch13">13. Animated Business Card</a></h3>
  <h3><a href="#ch14">14. Interactive Photo Gallery</a></h3>
  <h3><a href="#ch15">15. 10 Best Computer Science Projects To Hone Your Skills</a></h3>
  <h3><a href="#ch16">16. Text to Speech Converter</a></h3>
  <h3><a href="#ch17">17. JavaScript Map Reference</a></h3>
</blockquote>

<h3>Introduction</h3>
<p>One of the most popular scripting languages, JavaScript is used in all the web applications for validation, 
rendering dynamic content, interactive graphics and maps, and much more. Along with HTML and CSS, JS has 
the power to build complete, robust web applications. Because of JS, the user can interact with a web 
page and see all the interesting elements on the page. As we explore the projects, we will come to know-
how js helps in building interactive web pages. Before that, let us quickly go through the important 
features of JS:</p>

- Used on both client-side and server-side to create interactive web content.
- Greatly improves user experience by providing dynamic functionality.
- Light-weight language having object-oriented capabilities.
- Interpreted, open and cross-platform language.
- Seamless integration with Java and HTML.

<h3>Why JavaScript Projects?</h3>
JS is the heart of any web application. Good knowledge of JavaScript can get you a range of challenging 
and interesting career options like developing mobile and desktop apps, building dynamic websites from 
scratch, UI/UX designer, or even a full stack developer. If you know the basics of JavaScript, projects 
are your next step to add stars to your resume. If you don’t have any prior programming experience, you 
can take up basic JavaScript courses and then come back to these projects. If you follow a bit of HTML 
& CSS, you will understand most of the Javascript projects with the source code mentioned below.

<h3>Best JavaScript Projects for Beginners</h3>
<p>There is a lot you can do with JavaScript, but we don’t want to overwhelm you with everything yet. We 
have listed the top JavaScript projects that can add value to your resume as well as a career:</p>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3 id="ch1">1. JavaScript Calculator</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<p>We will use simple HTML, CSS, and make all the components work using basic JavaScript 
functions. To display buttons and numbers, we will use HTML, and add some beautification 
to them using CSS. To make the buttons perform the respective functions we will use 
JavaScript.</p>

<p>The main function is eval(), which is a global JS function that solves JS codes. The 
display() function will display the selected number on the calculator screen. Note 
that the program will work only for mouse events. Here is the complete code:</p>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>HTML: Calculator</h4>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->

<details>
  <summary>HTML: Calculator</summary>

```html
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

</details>

<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>CSS: Calculator</h4>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->

<details>
  <summary>CSS: Calculator</summary>

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
  background-image: linear-gradient(to bottom,transparent,
    transparent 50%,rgba(0,0,0,.04));
  box-shadow: inset 0 0 0 1px rgba(255,255,255,.05), 
    inset 0 1px 0 0 rgba(255,255,255,.45), 
  inset 0 -1px 0 0 rgba(255,255,255,.15), 
  0 1px 0 0 rgba(255,255,255,.15);
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

</details>

<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>JavaScript: Calculator</h4>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->

<details>
  <summary>JavaScript: Calculator</summary>

```javascript
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

</details>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3 id="ch2">2. <a href="https://www.sololearn.com/en/compiler-playground/WyyBylG1NvdU/#js">Hangman Game</a></h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<p>Hangman is a well-known game, and one of our simple JS projects. You can develop it in a jiffy 
using JavaScript, HTML, and CSS. Note that the main functionality is defined using JS. HTML is 
for display, and CSS does the job of beautifying the contents.</p>

<p>Many methods are defined in the JS code, so it may seem a bit complicated, but you will realize 
it is simple once you read the code thoroughly. You can also run the code and see the execution 
line by line.</p>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>HTML: Hangman</h4>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->

<details>
  <summary>HTML: Hangman</summary>

```html
<!DOCTYPE html>
<html t="0x31" i="YA-9517" v="1.60">
  <head>
    <title>Hangman (Game)</title>
  </head>
  <body>
    <div id="home">
      <div class="title">Hangman</div>
      <div class="button anim" onclick="startGame()">Play</div>
      <div class="foother">Coded by Thomas Hj</div>
    </div>
    <div id="result" class="h">
      <div class="title" id="rT"></div>
      <div class="body" id="rM"></div>
      <div class="button anim" onclick="startGame()">Try Again?</div>
    </div>
    <div id="pGame">
      <div id="letter"></div>
      <div id="game">
        <div class="player">
          <div class="playerModel">
            <div class="head" data="false" id="g4"></div>
            <div class="body" data="false" l="false" r="false" id="g5"></div>
            <div class="foot" data="false" l="false" r="false" id="g6"></div>
          </div>
        </div>
        <div class="stang3" data="false" id="g3"></div>
        <div class="stang2" data="false" id="g2"></div>
        <div class="stang" data="false" id="g1"></div>
        <div class="ground" data="false" id="g0"></div>
        <div class="hintButton" data="false" id="hintButton" onclick="hint()">?</div>
      </div>
      <div id="tastatur">
        <div id="moveKeybord"><div class="marg"></div></div>
        <div id="keybord"></div>
      </div>
      <div class="hint" id="hint">
        <div class="title">Hint<div class="exit" onclick="hintExit()">X</div></div>
        <div class="body" id="hintText"></div>
      </div>
    </div>
  </body>
</html>
```

</details>

<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>CSS: Hangman</h4>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<details>
  <summary>CSS</summary>

```css
body {
    background-color: #eee;
    margin: 0;
}

#home {
  background: linear-gradient(#eee, #aaa);
  background: -webkit-linear-gradient(top, #eee, #aaa);
  background: -ms-linear-gradient(top, #eee, #aaa);
  background: -moz-linear-gradient(top, #eee, #aaa);
  background: -o-linear-gradient(top, #eee, #aaa);
  bottom: 0;
  left: 0;
  position: absolute;
  right: 0;
  top: 0;
  z-index: 99;
}

#home .title {
  font-size: 48px;
  font-weight: bold;
  margin-top: 15%;
  text-align: center;
}

#home .button {
  background: #afa;
  background: linear-gradient(#afa, #6f6);
  background: -webkit-linear-gradient(top, #afa, #6f6);
  background: -ms-linear-gradient(top, #afa, #6f6);
  background: -moz-linear-gradient(top, #afa, #6f6);
  background: -o-linear-gradient(top, #afa, #6f6);
  border-radius: 2px;
  box-shadow: 0 0 0 5px #090;
  display: table;
  font-weight: bold;
  padding: 10px 20px;
  margin: 20% auto;
}

#home .foother {
  bottom: 20px;
  font-size: 12px;
  font-style: italic;
  position: absolute;
  right: 20px;
}

.h {
    display: none;
}

#result {
  background: #700;
  background: linear-gradient(rgba(125, 0, 0, 0.9) 20%, rgba(0, 0, 0, 0.7) 80%);
  background: -webkit-linear-gradient(top, rgba(125, 0, 0, 0.9) 20%, rgba(0, 0, 0, 0.7) 80%);
  background: -ms-linear-gradient(top, rgba(125, 0, 0, 0.9) 20%, rgba(0, 0, 0, 0.7) 80%);
  background: -moz-linear-gradient(top, rgba(125, 0, 0, 0.9) 20%, rgba(0, 0, 0, 0.7) 80%);
  background: -o-linear-gradient(top, rgba(125, 0, 0, 0.9) 20%, rgba(0, 0, 0, 0.7) 80%);
  bottom: 0;
  left: 0;
  position: absolute;
  right: 0;
  top: 0;
  z-index: 100;
}

#result[data="true"] {
  background: #070;
  background: linear-gradient(rgba(0, 125, 0, 0.9) 20%, rgba(0, 0, 0, 0.7) 80%);
  background: -webkit-linear-gradient(top, rgba(0, 125, 0, 0.9) 20%, rgba(0, 0, 0, 0.7) 80%);
  background: -ms-linear-gradient(top, rgba(0, 125, 0, 0.9) 20%, rgba(0, 0, 0, 0.7) 80%);
  background: -moz-linear-gradient(top, rgba(0, 125, 0, 0.9) 20%, rgba(0, 0, 0, 0.7) 80%);
  background: -o-linear-gradient(top, rgba(0, 125, 0, 0.9) 20%, rgba(0, 0, 0, 0.7) 80%);
}

#result .title {
  color: #eee;
  font-size: 48px;
  margin-top: 15%;
  text-align: center;
  text-shadow: 1px 1px 0 #000;
}

#result .body {
  color: #fff;
  margin-top: 30px;
  text-align: center;
  text-shadow: 1px 1px 0 #000;
}

#result .button {
  background:#afa;
  background: linear-gradient(#afa, #6f6);
  background: -webkit-linear-gradient(top, #afa, #6f6);
  background: -ms-linear-gradient(top, #afa, #6f6);
  background: -moz-linear-gradient(top, #afa, #6f6);
  background: -o-linear-gradient(top, #afa, #6f6);
  border-radius: 2px;
  box-shadow: 0 0 0 5px #090;
  display: table;
  font-weight: bold;
  padding: 10px 20px;
  margin: 40px auto;
  margin-bottom: 0;
}

#letter {
  font-size: 22px;
  height: 30px;
  margin: 20px;
  text-align: center;
}

.l {
  box-shadow: 0 3px 0 -1px #555;
  display: inline-block;
  margin: 1px;
  height: 20px;
  text-transform: uppercase;
  width: 20px;
}

.ls {
  box-shadow: 0 0 0 0 #555;
  width: 10px;
}

#game {
  height: 250px;
  margin: auto;
  position: relative;
  width: 220px;
}

#game .player {
  left: 53px;
  position: absolute;
  top: 90px;
  height: 130px;
  width: 75px;
}

.player .playerModel {
  height: 100%;
  position: relative;
  width: 100%;
}

.playerModel .head {
  border-radius: 50%;
  box-shadow: 0 0 0 2px #000 inset;
  height: 35px;
  margin: auto;
  width: 35px;
}

.playerModel .head[data="false"] {
  display: none;
}

.playerModel .body {
  background-color: #000;
  height: 45px;
  margin: auto;
  width: 2px;
}

.playerModel .body[data="false"] {
  display: none;
}

.playerModel .body:before, .playerModel .body:after {
  background-color: #000;
  content: "";
  display: inline-block;
  height: 30px;
  position: absolute;
  width: 2px;
}

.playerModel .body[l="false"]:before, .playerModel .body[r="false"]:after {
  display: none;
}

.playerModel .body:before {
  left: 27px;
  transform: rotate(45deg);
  -webkit-transform: rotate(45deg);
}

.playerModel .body:after {
  right: 26px;
  transform: rotate(-45deg);
  -webkit-transform: rotate(-45deg);
}

.playerModel .foot {
  background-color: #000;
  height: 3px;
  margin: auto;
  width: 2px;
}

.playerModel .foot[data="false"] {
  display: none;
}

.playerModel .foot:before, .playerModel .foot:after {
  background-color: #000;
  content: "";
  display: inline-block;
  height: 40px;
  position: absolute;
  width: 2px;
}

.playerModel .foot[l="false"]:before, .playerModel .foot[r="false"]:after {
  display: none;
}

.playerModel .foot:before {
  left: 30px;
  transform: rotate(20deg);
  -webkit-transform: rotate(20deg);
}

.playerModel .foot:after {
  right: 29px;
  transform: rotate(-20deg);
  -webkit-transform: rotate(-20deg);
}

#game .stang3 {
  background-color: #000;
  height: 20px;
  left: 90px;
  position: absolute;
  top: 70px;
  width: 2px;
}

#game .stang3[data="false"] {
  display: none;
}

#game .stang2 {
    background-color: #000;
    border-radius: 5px 0 0 5px;
    bottom: 180px;
    height: 5px;
    position: absolute;
    right: 45px;
    width: 95px;
}

#game .stang2:before {
    background-color: #000;
    content: "";
    left: 50px;
    height: 5px;
    position: absolute;
    top: 17px;
    transform: rotate(45deg);
    -webkit-transform: rotate(45deg);
    width: 50px;
}

#game .stang2[data="false"] {
    display: none;
}

#game .stang {
    background-color: #000;
    bottom: 0;
    height: 180px;
    margin: auto;
    position: absolute;
    right: 45px;
    width: 5px;
}

#game .stang[data="false"] {
    display: none;
}

#game .ground {
    background-color: #000;
    border-radius: 5px;
    bottom: 0;
    left: 0;
    height: 5px;
    margin: auto;
    position: absolute;
    right: 0;
    width: 220px;
}

#game .ground[data="false"] {
    display: none;
}

#game .hintButton {
    background: #ccc;
    background: linear-gradient(transparent, rgba(0, 0, 0, 0.1));
    background: -webkit-linear-gradient(top, transparent, rgba(0, 0, 0, 0.1));
    background: -ms-linear-gradient(top, transparent, rgba(0, 0, 0, 0.1));
    background: -moz-linear-gradient(top, transparent, rgba(0, 0, 0, 0.1));
    background: -o-linear-gradient(top, transparent, rgba(0, 0, 0, 0.1));
    border-radius: 8%;
    box-shadow: 1px 1px 3px #999;
    font-weight: bold;
    padding: 5px 10px;
    position: absolute;
    right: 5px;
    top: 5px;
}

#game .hintButton[data="false"] {
    display: none;
}

#tastatur {
    background-color: rgba(238, 238, 238, 0.9);
    bottom: 0;
    left: 0;
    margin: auto;
    margin-bottom: 20px;
    max-width: 500px;
    padding: 0 15px;
    position: absolute;
    right: 0;
    text-align: center;
}

#moveKeybord {
    padding: 15px;
}

.marg {
    border-bottom: solid 2px #ccc;
}

#hint {
    border-radius: 2px;
    box-shadow: 1px 1px 4px #888;
    display: none;
    left: 0;
    margin: auto;
    margin-top: 75px;
    position: absolute;
    right: 0;
    top: 0;
    width: 250px;
}

#hint .title {
    background: #fff;
    background: linear-gradient(#fff, #bbb);
    background: -webkit-linear-gradient(top, #fff, #bbb);
    background: -ms-linear-gradient(top, #fff, #bbb);
    background: -moz-linear-gradient(top, #fff, #bbb);
    background: -o-linear-gradient(top, #fff, #bbb);
    border-bottom: solid 1px #555;
    border-radius: 2px 2px 0 0;
    font-weight: bold;
    padding: 5px 10px;
    position: relative;
}

#hint .title .exit {
    background-color: #f55;
    border-radius: 50%;
    box-shadow: 1px 1px 4px #888;
    font-weight: bold;
    padding: 8px 12px;
    position: absolute;
    right: -15px;
    top: -15px;
}

#hint .body {
    background-color: #ddd;
    border-radius: 0 0 2px 2px;
    padding: 10px;
}

.b {
    background: #eee;
    background: linear-gradient(#fff, #eee);
    background: -webkit-linear-gradient(top, #fff, #eee);
    background: -ms-linear-gradient(top, #fff, #eee);
    background: -moz-linear-gradient(top, #fff, #eee);
    background: -o-linear-gradient(top, #fff, #eee);
    box-shadow: 1px 1px 1px 0 #ccc;
    display: inline-block;
    margin: 2px;
    padding: 8px;
    text-align: center;
    width: 25px;
}

.b[data="false"], .b[data="true"] {
    color: #555;
    font-weight: bold;
}

.b[data="true"] {
    background: #9f9;
}

.b[data="false"] {
    background: #aaa;
}

.anim {
    animation: button 3s infinite;
    -webkit-animation: button 3s infinite;
}

@keyframes button {
    0%, 50%, 90% {
        transform: rotate(0deg);
        -webkit-transform: rotate(0deg);
    }
    60% {
        transform: rotate(5deg) scale(1);
        -webkit-transform: rotate(5deg) scale(1);
    }
    70% {
        transform: rotate(-5deg) scale(0.97);
        -webkit-transform: rotate(-5deg) scale(0.97);
    }
    80% {
        transform: rotate(5deg) scale(1.05);
        -webkit-transform: rotate(5deg) scale(1.05);
    }
}

@-webkit-keyframes button {
    0%, 50%, 90% {
        transform: rotate(0deg);
        -webkit-transform: rotate(0deg);
    }
    60% {
        transform: rotate(5deg) scale(1);
        -webkit-transform: rotate(5deg) scale(1);
    }
    70% {
        transform: rotate(-5deg) scale(0.97);
        -webkit-transform: rotate(-5deg) scale(0.97);
    }
    80% {
        transform: rotate(5deg) scale(1.05);
        -webkit-transform: rotate(5deg) scale(1.05);
    }
}
```

</details>

<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>JavaScript: Hangman</h4>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<details>
  <summary>JavaScript: Hangman</summary>

```javascript
/*
 * > Coded By Thomas Hj
 * > 31102016
 * 
 * > #31
 */

// Word selection
// New word = ["Word name", "Hint"]
var word = [["Hangman", "That game you are playing right now."], ["Thomas Hj", "About the creator of this game."], ["HTML", "Markup language for creating Web pages."], ["CSS", "Wep page styles"], ["PHP", "A very popular server scripting language."], ["JavaScript", "Make web-page dynamic without reload the web page."], ["Java", "Run 15 billion devices.\nA program can be run in Windows, Linux and Mac"], ["SoloLearn", "A company that everyone can code for fun and share."], ["Love", "What is ?\nBaby don't hurt me\nDon't hurt me\nNo more"], ["Document", "A lot of text in the a file."], ["Playground", "There school kids go to."], ["Run", "Usain bolt."], ["Code", "var hw = 'Hello World';"], ["Samsung", "A company create Phone, Tv, Monitor, SDD, Memory chip..."], ["Super Mario", "A very popular game in Nintendo 64 that have red hat."], ["Star", "Super Mario like to get."], ["Clock", "14:12 or 14pm"], ["Binary Clock", "A clock that only use 0 or 1."], ["Sword", "Link from Zelda have on the hand."], ["Girl", "Not boy but ?"], ["Boy", "Not girl but ?"], ["Female", "Other name as girl."], ["Male", "Other name as boy."], ["Smartphone", "Something you've always on you."]]

// Game keyboard
var tastatur = "ABCDEFGHIJKLMNOPQRSTUVWXYZ"

// Game memory
var select = 0
var wordLeft = []
var fail = 0

// Web-page onload
window.onload = function() {
    gId("moveKeybord").addEventListener('touchmove', function(e) {
        wH = window.innerHeight
        tY = e.touches[0].clientY
        eL = gId("tastatur")
        resY = wH - tY - eL.offsetHeight
        if(resY &lt; 0) {
            resY = 0
        } else if(resY > wH / 2) {
            resY = wH / 2
        }
        eL.style.bottom = resY + "px"
    }, false)
    createTastur()
}

// Start game
function startGame() {
    gId("home").className = "h"
    gId("result").className = "h"
    newGame()
}

// New game
function newGame() {
    clearTastatur()
    clearPlayer()
    createWord()
}

// Clear keyboard
function clearTastatur() {
    var e = document.getElementsByClassName("b")
    for(a = 0; a &lt; e.length; a++) {
        e[a].setAttribute("data", "")
    }
}

// Clear player
function clearPlayer() {
    fail = 0
    wordLeft = []
    gId("g0").setAttribute("data", "false")
    gId("g1").setAttribute("data", "false")
    gId("g2").setAttribute("data", "false")
    gId("g3").setAttribute("data", "false")
    gId("g4").setAttribute("data", "false")
    gId("g5").setAttribute("data", "false")
    gId("g5").setAttribute("r", "false")
    gId("g5").setAttribute("l", "false")
    gId("g6").setAttribute("data", "false")
    gId("g6").setAttribute("l", "false")
    gId("g6").setAttribute("r", "false")
    gId("hintButton").setAttribute("data", "false")
    gId("hint").style.display = "none"
}

// Get new word
function createWord() {
  var d = gId("letter")
  d.innerHTML = ""
  select = Math.floor(Math.random() * word.length)
  for(a = 0; a &lt; word[select][0].length; a++) {
    var x = word[select][0][a].toUpperCase()
    var b = document.createElement("span")
    b.className = "l" + (x == " " ? " ls" : "")
    b.innerHTML = "&nbsp"
    b.id = "l" + a;
    d.appendChild(b)
    if(x != " ") {
      if(wordLeft.indexOf(x) == -1) {
        wordLeft.push(x)
      }
    }
  }
}

// Create keyboard
function createTastur() {
  var tas = gId("keybord")
  tas.innerHTML = ""
  for(a = 0; a &lt; tastatur.length; a++) {
    var b = document.createElement("span")
    b.className = "b"
    b.innerText = tastatur[a]
    b.setAttribute("data", "")
    b.onclick = function() {
      bTas(this)
    }
      tas.appendChild(b)
  }
}

// Game check, If show next error / game end
function bTas(a) {
    if(a.getAttribute("data") == "") {
        var x = isExist(a.innerText)
        a.setAttribute("data", x)
        if(x) {
            if(wordLeft.length == 0) {
                gameEnd(true)
            }
        } else {
            showNextFail()
        }
    }
}

// If letter "X" exist
function isExist(e) {
    e = e.toUpperCase()
    var x = wordLeft.indexOf(e)
    if(x != -1) {
        wordLeft.splice(x, 1)
        typeWord(e)
        return true
    }
    return false
}

// Show next fail drawing
function showNextFail() {
    fail++
    switch(fail) {
        case 1:
            gId("g0").setAttribute("data", "true")
            break;
        
        case 2:
            gId("g1").setAttribute("data", "true")
            break;
        
        case 3:
            gId("g2").setAttribute("data", "true")
            break;
        
        case 4:
            gId("g3").setAttribute("data", "true")
            gId("hintButton").setAttribute("data", "true")
            break;
        
        case 5:
            gId("g4").setAttribute("data", "true")
            break;
        
        case 6:
            gId("g5").setAttribute("data", "true")
            break;
        
        case 7:
            gId("g5").setAttribute("l", "true")
            break;
        
        case 8:
            gId("g5").setAttribute("r", "true")
            break;
        
        case 9:
            gId("g6").setAttribute("data", "true")
            gId("g6").setAttribute("l", "true")
            break;
        
        case 10:
            gId("g6").setAttribute("r", "true")
            gameEnd(false)
            break;
    }
}

function typeWord(e) {
    for(a = 0; a &lt; word[select][0].length; a++) {
        if(word[select][0][a].toUpperCase() == e) {
            gId("l" + a).innerText = e
        }
    }
}

// Game result
function gameEnd(e) {
    var d = gId("result")
    d.setAttribute("data", e)
    if(e) {
        gId("rT").innerText = "You Win!"
        gId("rM").innerHTML = "Congratulations, you found the word!<br/><br/>Good Job!"
    } else {
        gId("rT").innerText = "You Lose!"
        gId("rM").innerHTML = "The word was <br/><br/>\"" + word[select][0].toUpperCase() + "\"<br/><br/>Better luck next time."
    }
    d.className = ""
}

// Show hint
function hint() {
    gId("hintText").innerText = word[select][1]
    gId("hint").style.display = "block"
}

// Exit hint
function hintExit() {
    gId("hint").style.display = "none"
}

// Get HTML ID element by name
function gId(a) {
    return document.getElementById(a)
}
```

</details>

<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3 id="ch3">3. Tic Tac Toe Game</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<p>JavaScript makes it easy to develop a Tic-Tac-Toe game yourself. You can look at the entire code 
here, and it explains how to build a 3x3 tic-tac-toe step by step. Then, you can later expand to 
NxN for your own practice and knowledge. The HTML and CSS for the project are quite simple. The 
author first starts with pseudocode and then goes on to explain each function individually.</p>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>HTML: Tic-Tac-Toe</h4>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<details>
  <summary>HTML: Tic-Tac-Toe</summary>
  
```html
<!doctype html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport"
    content="width=device-width, user-scalable=no, initial-scale=1.0, maximum-scale=1.0, minimum-scale=1.0">
  <meta http-equiv="X-UA-Compatible" content="ie=edge">
  <title>Tic Tac Toe</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>
  <section>
    <h1 class="game--title">Tic Tac Toe</h1>
    <div class="game--container">
      <div data-cell-index="0" class="cell"></div>
      <div data-cell-index="1" class="cell"></div>
      <div data-cell-index="2" class="cell"></div>
      <div data-cell-index="3" class="cell"></div>
      <div data-cell-index="4" class="cell"></div>
      <div data-cell-index="5" class="cell"></div>
      <div data-cell-index="6" class="cell"></div>
      <div data-cell-index="7" class="cell"></div>
      <div data-cell-index="8" class="cell"></div>
    </div>
    <h2 class="game--status"></h2>
    <button class="game--restart">Restart Game</button>
  </section>
<script src="script.js"></script>
</body>
</html>
```

</details>

<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>CSS: Tic-Tac-Toe</h4>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->

<details>
  <summary>CSS: Tic-Tac-Toe</summary>
  
```css
body {
    font-family: "Arial", sans-serif;
}
section {
    text-align: center;
}
.game--container {
    display: grid;
    grid-template-columns: repeat(3, auto);
    width: 306px;
    margin: 50px auto;
}
.cell {
    font-family: "Permanent Marker", cursive;
    width: 100px;
    height: 100px;
    box-shadow: 0 0 0 1px #333333;
    border: 1px solid #333333;
    cursor: pointer;
    line-height: 100px;
    font-size: 60px;
}
```

</details>

<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>JavaScript: Tic-Tac-Toe</h4>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->

<details>
  <summary>JavaScript: Tic-Tac-Toe</summary>

```javascript
const statusDisplay = document.querySelector('.game--status');

let gameActive = true;
let currentPlayer = "X";
let gameState = ["", "", "", "", "", "", "", "", ""];

const winningMessage = () => `Player ${currentPlayer} has won!`;
const drawMessage = () => `Game ended in a draw!`;
const currentPlayerTurn = () => `It's ${currentPlayer}'s turn`;

statusDisplay.innerHTML = currentPlayerTurn();

const winningConditions = [
    [0, 1, 2],
    [3, 4, 5],
    [6, 7, 8],
    [0, 3, 6],
    [1, 4, 7],
    [2, 5, 8],
    [0, 4, 8],
    [2, 4, 6]
];

function handleCellPlayed(clickedCell, clickedCellIndex) {
    gameState[clickedCellIndex] = currentPlayer;
    clickedCell.innerHTML = currentPlayer;
}

function handlePlayerChange() {
    currentPlayer = currentPlayer === "X" ? "O" : "X";
    statusDisplay.innerHTML = currentPlayerTurn();
}

function handleResultValidation() {
  let roundWon = false;
  for (let i = 0; i &lt;= 7; i++) {
    const winCondition = winningConditions[i];
    let a = gameState[winCondition[0]];
    let b = gameState[winCondition[1]];
    let c = gameState[winCondition[2]];
    if (a === '' || b === '' || c === '') {
      continue;
    }
    if (a === b && b === c) {
      roundWon = true;
      break
    }
  }

  if (roundWon) {
    statusDisplay.innerHTML = winningMessage();
    gameActive = false;
    return;
  }

  let roundDraw = !gameState.includes("");
  if (roundDraw) {
    statusDisplay.innerHTML = drawMessage();
    gameActive = false;
    return;
  }
  handlePlayerChange();
}

function handleCellClick(clickedCellEvent) {
  const clickedCell = clickedCellEvent.target;
  const clickedCellIndex = parseInt(clickedCell.getAttribute('data-cell-index'));

  if (gameState[clickedCellIndex] !== "" || !gameActive) {
    return;
  }

  handleCellPlayed(clickedCell, clickedCellIndex);
  handleResultValidation();
}

function handleRestartGame() {
  gameActive = true;
  currentPlayer = "X";
  gameState = ["", "", "", "", "", "", "", "", ""];
  statusDisplay.innerHTML = currentPlayerTurn();
  document.querySelectorAll('.cell').forEach(cell => cell.innerHTML = "");
}

document.querySelectorAll('.cell').forEach(cell => cell.addEventListener('click', handleCellClick));
document.querySelector('.game--restart').addEventListener('click', handleRestartGame);
```

</details>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3 id="ch3b">3b. Another Tic-Tac-Toe</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<details>
  <summary>HTML: 2nd Tic-Tac-Toe</summary>

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Tic-Tac-Toe Game</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>
  <div id="tic-tac-toe-board">
    <div class="row">
      <div class="cell" id="cell-1"></div>
      <div class="cell" id="cell-2"></div>
      <div class="cell" id="cell-3"></div>
    </div>
    <div class="row">
      <div class="cell" id="cell-4"></div>
      <div class="cell" id="cell-5"></div>
      <div class="cell" id="cell-6"></div>
    </div>
    <div class="row">
      <div class="cell" id="cell-7"></div>
      <div class="cell" id="cell-8"></div>
      <div class="cell" id="cell-9"></div>
    </div>
  </div>
  <div id="gameMessage" class="game-message"></div>
  <button id="resetButton">Reset Game</button>  
  <script src="script.js"></script>
</body>
</html>
```

</details>

<details>
  <summary>CSS: 2nd Tic-Tac-Toe</summary>

```css
body {
  font-family: 'Arial', sans-serif;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  height: 100vh;
  margin: 0;
  background: linear-gradient(to right, #74ebd5, #ACB6E5);
  color: #333;
}

#tic-tac-toe-board {
  display: grid;
  grid-template-columns: repeat(3, 100px);
  grid-template-rows: repeat(3, 100px);
  gap: 10px;
}

.cell {
  background-color: #fff;
  border: 2px solid #333;
  display: flex;
  justify-content: center;
  align-items: center;
  font-size: 2rem;
  cursor: pointer;
  transition: background-color 0.3s ease;
  width: 100px;
  height: 100px;
}

.cell:hover {
  background-color: #e3e3e3;
}

.game-message {
  text-align: center;
  margin-top: 20px;
  font-size: 20px;
  color: #333;
}

#resetButton {
  padding: 10px 20px;
  font-size: 1rem;
  color: #fff;
  background-color: #333;
  border: none;
  cursor: pointer;
  border-radius: 5px;
  transition: background-color 0.3s ease;
}

#resetButton:hover {
  background-color: #555;
}
```

</details>

<details>
  <summary>JavaScript: 2nd Tic-Tac-Toe</summary>

```javascript
let currentPlayer = 'X'; // Player X always starts
let gameBoard = ['', '', '', '', '', '', '', '', '']; // 3x3 game board
let gameActive = true;

function handlePlayerTurn(clickedCellIndex) {
  if (gameBoard[clickedCellIndex] !== '' || !gameActive) {
      return;
  }
  gameBoard[clickedCellIndex] = currentPlayer;
  checkForWinOrDraw();
  currentPlayer = currentPlayer === 'X' ? 'O' : 'X';
}

function cellClicked(clickedCellEvent) {
  const clickedCell = clickedCellEvent.target;
  const clickedCellIndex = parseInt(clickedCell.id.replace('cell-', '')) - 1;
  if (gameBoard[clickedCellIndex] !== '' || !gameActive) {
      return;
  }
  handlePlayerTurn(clickedCellIndex);
  updateUI();
}

const cells = document.querySelectorAll('.cell');

cells.forEach(cell => {
  cell.addEventListener('click', cellClicked, false);
});

function updateUI() {
  for (let i = 0; i &lt; cells.length; i++) {
      cells[i].innerText = gameBoard[i];
  }
}

function announceWinner(player) {
  const messageElement = document.getElementById('gameMessage');
  messageElement.innerText = `Player ${player} Wins!`;
}

function announceDraw() {
  const messageElement = document.getElementById('gameMessage');
  messageElement.innerText = 'Game Draw!';
}

const winConditions = [
  [0, 1, 2], // Top row
  [3, 4, 5], // Middle row
  [6, 7, 8], // Bottom row
  [0, 3, 6], // Left column
  [1, 4, 7], // Middle column
  [2, 5, 8], // Right column
  [0, 4, 8], // Left-to-right diagonal
  [2, 4, 6]  // Right-to-left diagonal
];

function checkForWinOrDraw() {
  let roundWon = false;

  for (let i = 0; i &lt; winConditions.length; i++) {
    const [a, b, c] = winConditions[i];
    if (gameBoard[a] && gameBoard[a] === gameBoard[b] && gameBoard[a] === gameBoard[c]) {
      roundWon = true;
      break;
    }
  }

  if (roundWon) {
    announceWinner(currentPlayer);
    gameActive = false;
    return;
  }

  let roundDraw = !gameBoard.includes('');
  if (roundDraw) {
    announceDraw();
    gameActive = false;
    return;
  }
}

function resetGame() {
  gameBoard = ['', '', '', '', '', '', '', '', ''];
  gameActive = true;
  currentPlayer = 'X';
  cells.forEach(cell => {
      cell.innerText = '';
  });
  document.getElementById('gameMessage').innerText = '';
}

const resetButton = document.getElementById('resetButton');
resetButton.addEventListener('click', resetGame, false);
```

</details>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3 id="ch4">4. Weather App</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<p>Weather apps are also popular JavaScript projects. Once you change the location name in this project, 
the weather display changes immediately without a page refresh. The UI is also quite sleek.</p>

<p>Note that most weather apps use an API that gets the weather data. We will use the popular and most 
common API, OpenWeatherMap.</p>

<p>Check out this Youtube video that explains the weather app code and functionality in detail. There 
are three files, as usual: index.html, main.js, and main.css. Although you can put all the code in 
a single file (HTML), it is more convenient to maintain separate files.</p>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>HTML: Weather App</h4>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->

<details>
  <summary>HTML: Weather App</summary>

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <meta http-equiv="X-UA-Compatible" content="ie=edge">
  <title>Weather app</title>
  <link rel="stylesheet" href="main.css" />
</head>
<body>
  <div class="app-wrap">
    <header>
      <input type="text" autocomplete="off" class="search-box" placeholder="Search for a city..." />
    </header>
    <main>
      <section class="location">
        <div class="city">Northampton, GB</div>
        <div class="date">Thursday 10 January 2020</div>
      </section>
      <div class="current">
        <div class="temp">15<span>°c</span></div>
        <div class="weather">Sunny</div>
        <div class="hi-low">13°c / 16°c</div>
      </div>
    </main>
  </div>
  <script src="main.js"></script>
</body>
</html>
```

</details>

<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>CSS: Weather App</h4>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->

<details>
  <summary>CSS: Weather App</summary>

```css
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body {
  font-family: 'montserrat', sans-serif;
  background-image: url('bg.jpg');
  background-size: cover;
  background-position: top center;
}

.app-wrap {
  display: flex;
  flex-direction: column;
  min-height: 100vh;
  background-image: linear-gradient(to bottom, rgba(0, 0, 0, 0.3), rgba(0, 0, 0, 0.6));
}

header {
  display: flex;
  justify-content: center;
  align-items: center;
  padding: 50px 15px 15px;
}

header input {
  width: 100%;
  max-width: 280px;
  padding: 10px 15px;
  border: none;
  outline: none;
  background-color: rgba(255, 255, 255, 0.3);
  border-radius: 16px 0px 16px 0px;
  border-bottom: 3px solid #DF8E00;
  
  color: #313131;
  font-size: 20px;
  font-weight: 300;
  transition: 0.2s ease-out;
}

header input:focus {
  background-color: rgba(255, 255, 255, 0.6);
}

main {
  flex: 1 1 100%;
  padding: 25px 25px 50px;
  display: flex;
  flex-direction: column;
  align-items: center;
  text-align: center;
}

.location .city {
  color: #FFF;
  font-size: 32px;
  font-weight: 500;
  margin-bottom: 5px;
}

.location .date {
  color: #FFF;
  font-size: 16px;
}

.current .temp {
  color: #FFF;
  font-size: 102px;
  font-weight: 900;
  margin: 30px 0px;
  text-shadow: 2px 10px rgba(0, 0, 0, 0.6);
}

.current .temp span {
  font-weight: 500;
}

.current .weather {
  color: #FFF;
  font-size: 32px;
  font-weight: 700;
  font-style: italic;
  margin-bottom: 15px;
  text-shadow: 0px 3px rgba(0, 0, 0, 0.4);
}

.current .hi-low {
  color: #FFF;
  font-size: 24px;
  font-weight: 500;
  text-shadow: 0px 4px rgba(0, 0, 0, 0.4);
}
```

</details>

<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>JavaScript: Weather App</h4>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->

<details>
  <summary>JavaScript: Weather App</summary>

```javascript
const api = {
  key: "afaf9f8d48cff6cafd32e23220bcfdbf",
  base: "https://api.openweathermap.org/data/2.5/"
}

const searchbox = document.querySelector('.search-box');
searchbox.addEventListener('keypress', setQuery);

function setQuery(evt) {
  if (evt.keyCode == 13) {
    getResults(searchbox.value);
  }
}

function getResults (query) {
  fetch(`${api.base}weather?q=${query}&units=metric&APPID=${api.key}`)
    .then(weather => {
      return weather.json();
    }).then(displayResults);
}

function displayResults (weather) {
  let city = document.querySelector('.location .city');
  city.innerText = `${weather.name}, ${weather.sys.country}`;

  let now = new Date();
  let date = document.querySelector('.location .date');
  date.innerText = dateBuilder(now);

  let temp = document.querySelector('.current .temp');
  temp.innerHTML = `${Math.round(weather.main.temp)}<span>°c</span>`;

  let weather_el = document.querySelector('.current .weather');
  weather_el.innerText = weather.weather[0].main;

  let hilow = document.querySelector('.hi-low');
  hilow.innerText = `${Math.round(weather.main.temp_min)}°c / ${Math.round(weather.main.temp_max)}°c`;
}

function dateBuilder (d) {
  let months = ["January", "February", "March", "April", "May", "June", "July", "August", "September", "October", "November", "December"];
  let days = ["Sunday", "Monday", "Tuesday", "Wednesday", "Thursday", "Friday", "Saturday"];

  let day = days[d.getDay()];
  let date = d.getDate();
  let month = months[d.getMonth()];
  let year = d.getFullYear();

  return `${day} ${date} ${month} ${year}`;
}
```

</details>

<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3 id="ch5">5. Music Events</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<p>Here, we’ll introduce you to event listeners that will act on keyboard events. For example, an event 
will take place if the ‘S’ key is pressed. Each one will have a different code and action.</p>

<p>Apart from event listeners, we will also learn how to add and play audio files. Note that we have added 
very basic CSS, as the focus here is on JavaScript. You will have to import your own sounds and 
background image for the program to work fully.</p>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>HTML: Music</h4>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->

<details>
  <summary>HTML</summary>

```html
<html>
<head>
 <meta charset="UTF-8">
 <meta name="viewport" content="width=device-width, initial-scale=1">
 <title>KeyBoard Music</title>
</head>
<body>
 <div class="keys">
   <div data-key="65" class="key">
     <kbd>A</kbd>
   </div>
   <div data-key="83" class="key">
     <kbd>S</kbd>
   </div>
   <div data-key="68" class="key">
     <kbd>D</kbd>
   </div>
   <div data-key="70" class="key">
     <kbd>F</kbd>
   </div>
   <div data-key="71" class="key">
     <kbd>G</kbd>
   </div>
   <div data-key="72" class="key">
     <kbd>H</kbd>
   </div>
   <div data-key="74" class="key">
     <kbd>J</kbd>
   </div>
   <div data-key="75" class="key">
     <kbd>K</kbd>
   </div>
   <div data-key="76" class="key">
     <kbd>L</kbd>
   </div>
 </div>
 <audio data-key="65" src="sounds/clap.wav"></audio>
 <audio data-key="83" src="sounds/chord.wav"></audio>
 <audio data-key="68" src="sounds/ride.wav"></audio>
 <audio data-key="70" src="sounds/openhat.wav"></audio>
 <audio data-key="71" src="sounds/tink.wav"></audio>
 <audio data-key="72" src="sounds/kick.wav"></audio>
 <audio data-key="74" src="sounds/swipe.wav"></audio>
 <audio data-key="75" src="sounds/tom.wav"></audio>
 <audio data-key="76" src="sounds/boom.wav"></audio>
</body>
<script>
function removeTransition(event) {
  if (event.propertyName !== 'transform') return
  event.target.classList.remove('playing')
}
function playSound(event) {
  const audio = document.querySelector(`audio[data-key="${event.keyCode}"]`)
  const key = document.querySelector(`div[data-key="${event.keyCode}"]`)
  if (!audio) return
  key.classList.add('playing')
  audio.currentTime = 0
  audio.play()
}
const keys = Array.from(document.querySelectorAll('.key'))
  keys.forEach((key) => key.addEventListener('transitionend', removeTransition))
  window.addEventListener('keydown', playSound)
</script>
<style>
html {
  font-size: 12px;
  background: url('drums.jpg') top center;
  background-size: 80%;
}
.keys {
  display: flex;
  flex: 1;
  align-items: top;
  justify-content: center;
}
.key {
  border: 0.4rem solid blue;
  border-radius: 0.5rem;
  margin: 1rem;
  font-size: 2rem;
  padding: 1rem 0.5rem;
  transition: all 0.01s ease;
  width: 5rem;
  text-align: center;
  color: black;
  text-shadow: 0 0 0.5rem yellow;
}
</style>
</html>
```

</details>

<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>CSS: Music App</h4>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->

<details>
  <summary>CSS</summary>

```css

```

</details>

<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>JavaScript: Music App</h4>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->

<details>
  <summary>JavaScript</summary>

```javascript

```

</details>

<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3 id="ch5b">5b. Drums</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>HTML: Drums</h4>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->

<details>
  <summary>HTML</summary>

```
<!DOCTYPE html>
<html>

<head>
  <title>Drum Kit</title>
  <link rel="stylesheet" href="styles.css"> 
</head>

<body>
  <h1 id="title">The Drum Kit</h1>
  <div class="set">
    <button class="w drum">w</button>
    <button class="a drum">a</button>
    <button class="s drum">s</button>
    <button class="d drum">d</button>
    <button class="j drum">j</button>
    <button class="k drum">k</button>
    <button class="l drum">l</button>
  </div>

<script src="index.js"></script> 

<footer>
</footer>
</body>
</html>
```

</details>

<details>
  <summary>JS</summary>

```
var numberOfDrumButtons = document.querySelectorAll(".drum").length;

for (var i = 0; i < numberOfDrumButtons; i++) {
  document.querySelectorAll(".drum")[i].addEventListener("click", function() {
    var buttonInnerHTML = this.innerHTML;
    makeSound(buttonInnerHTML);
    buttonAnimation(buttonInnerHTML);
  });
}

document.addEventListener("keypress", function(event) {
  makeSound(event.key);
  buttonAnimation(event.key);
});

function makeSound(key) {
  switch (key) {
    case "w":
      var tom1 = new Audio("sounds/tom-1.mp3");
      tom1.play();
      break;
    case "a":
      var tom2 = new Audio("sounds/tom-2.mp3");
      tom2.play();
      break;
    case "s":
      var tom3 = new Audio('sounds/tom-3.mp3');
      tom3.play();
      break;
    case "d":
      var tom4 = new Audio('sounds/tom-4.mp3');
      tom4.play();
      break;
    case "j":
      var snare = new Audio('sounds/snare.mp3');
      snare.play();
      break;
    case "k":
      var crash = new Audio('sounds/crash.mp3');
      crash.play();
      break;
    case "l":
      var kick = new Audio('sounds/kick-bass.mp3');
      kick.play();
      break;
    default: console.log(key);
  }
}

function buttonAnimation(currentKey) {
  var activeButton = document.querySelector("." + currentKey);
  activeButton.classList.add("pressed");
  setTimeout(function() {
    activeButton.classList.remove("pressed");
  }, 100);
}
```

</details>

<details>
  <summary>CSS</summary>

```
body {
  text-align: center;
  background-color: #a06060;
}

h1 {
  font-size: 5rem;
  color: #DBEDF3;
  font-family: cursive;
  text-shadow: 3px 0 #DA0463;

}

.w {
  background-image: url("images/tom1.png");
}

.a {
  background-image: url("images/tom2.png");
}

.s {
  background-image: url("images/tom3.png");
}

.d {
  background-image: url("images/tom4.png");
}

.j {
  background-image: url("images/snare.png");
}

.k {
  background-image: url("images/crash.png");
}

.l {
  background-image: url("images/kick.png");
}

.set {
  margin: 10% auto;
}

.pressed {
  box-shadow: 0 3px 4px 0 #DBEDF3;
  opacity: 0.5;
}

.drum {
  outline: none;
  border: 10px solid #404B69;
  font-size: 5rem;
  font-family: 'Arvo', cursive;
  line-height: 2;
  font-weight: 900;
  color: #DA0463;
  text-shadow: 3px 0 #DBEDF3;
  border-radius: 15px;
  display: inline-block;
  width: 150px;
  height: 150px;
  text-align: center;
  margin: 10px;
  background-color: white;
}
```

</details>

<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3 id="ch6">6. Form Validation</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<p>Form validation is a useful aspect and used by many websites for client-side validation of user information, 
such as card and address details. For example, if there is a mandatory input field name, the user may type 
a number, leave the field blank, or type just one letter. JS can validate this information.</p>

<p>The project below involves simple form validation. Of course, the project will need HTML elements as well. 
We have not carried out any extensive styling, only including basic elements in the HTML itself.</p>

<p>Here is the complete code of a simple form with basic validations:</p>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>HTML: Form Validation</h4>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->

<details>
  <summary>HTML</summary>

```html
<html>
  <head>
     <title>Form Validation</title>
        <script type = "text/javascript">
        function validate() {
        var text;
           if( document.myForm.name.value == "" ) {
             text = "Name cannot be empty";
              document.getElementById("demo").innerHTML = text;
              document.myForm.name.focus() ;
              return false;
           }
           if( document.myForm.email.value == "" ) {
             text = "E-mail cannot be empty";
              document.getElementById("demo").innerHTML = text;
              document.myForm.email.focus() ;
              return false;
           }
      var emailID = document.myForm.email.value;
      atposn = emailID.indexOf("@");
      dotposn = emailID.lastIndexOf(".");
      if (atposn < 1 || ( dotposn - atposn < 2 )) {
      text = "Please enter valid email ID";
      document.getElementById("demo").innerHTML = text;
      document.myForm.email.focus() ;
      return false;
    }
           if( document.myForm.phone.value == "" || isNaN( document.myForm.phone.value ) ||
              document.myForm.phone.value.length != 10 ) {
              text = "Please enter a valid 10-digit phone number";
              document.getElementById("demo").innerHTML = text;
              document.myForm.phone.focus() ;
              return false;
           }
           if( document.myForm.subject.value == "0" ) {
              text = "Please provide your area of expertise";
              document.getElementById("demo").innerHTML = text;
              return false;
           }
           return( true );
        }
     </script>
  </head>
  <body>
     <form action = "" name = "myForm" onsubmit = "return(validate());">
       <h1 align="center">USER REGISTRATION</h1>
       <table align="center" cellspacing = "3" cellpadding = "3" border = "3">
           <tr>
              <td align = "right">Name</td>
              <td><input type = "text" name = "name" /></td>
           </tr>
           <tr>
              <td align = "right">E-mail</td>
              <td><input type = "text" name = "email" /></td>
           </tr>
           <tr>
              <td align = "right">Phone Number</td>
              <td><input type = "text" name = "phone" /></td>
           </tr>
           <tr>
              <td align = "right">Subject</td>
              <td>
                 <select name = "subject">
                    <option value = "0" selected>Select</option>
                    <option value = "1">HTML</option>
                    <option value = "2">JavaScript</option>
                    <option value = "3">CSS</option>
                    <option value = "4">JSP</option>
                 </select>
              </td>
           </tr>
        </table>
        <p id="demo" style="color:red; text-align:center"></p>
     <div style="text-align:center"><input type = "submit" value = "Submit" /></div>
     </form>
  </body>
</html>
```

</details>

<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>CSS: Form Validation</h4>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->

<h4>JavaScript: Form Validation</h4>

<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3 id="ch7">7. Photo Details Display</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<p>Here, we will display some images on a web page. Once the user hovers over the images, more details 
will appear. You can download images from anywhere or use the ones you already have.</p>

<p>Again, we have used basic HTML and CSS along with JS. The latter carries out most of the work. You 
will learn how mouse hover (over and out) events work through this project.</p>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>HTML: Photo Details Display</h4>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->

<details>
  <summary>HTML: Photo</summary>

```html
<!DOCTYPE html>
<html>
  <head>
    <title>My Sun Sign Infos</title>
  </head>
  <script>
  function display(element){
    document.getElementById('image').innerHTML = element.alt;
  }
  function revert(){
    document.getElementById('image').innerHTML = "Hover over a sunsign image to display details.";
  }
</script>
<style>
#image {
  width: 650px;
  height: 70px;
  border:5px solid pink;
  background-color: black;
  background-repeat: no-repeat;
  color:white;
  background-size: 100%;
  font-family: Didot;
  font-size: 150%;
  line-height: 60px;
  text-align: center;
}
img {
  width: 200px;
  height: 200px;
  border-radius: 50%;
}
</style>
<body>
  <div>
  <p id = "image">Hover over a sunsign image to display details.<p>
  <img alt = "Sagittarius are beautiful, loyal and passionate." 
    src = "saggi.jpg" onmouseover = "display(this)" onmouseout = "revert()">
  <img alt = "Pisces are dreamy, helpful and love everyone!" 
    src = "pisces.jpg" onmouseover = "display(this)" onmouseout = "revert()">
  <img alt = "Leo are strong and fearless. They aim for and achieve a lot!" 
    src = "leo.jpg" onmouseover = "display(this)" onmouseout = "revert()">
  <img alt = "Scorpions are friends for life. They are trustworthy and truthful." 
    src = "scorpio.jpg" onmouseover = "display(this)" onmouseout = "revert()">
  </div>
</body>
</html>
```

</details>

<p>To make this project more complex, try this slideshow project from W3Schools. You can change the 
onClick events to onmousehover and onmouseout events, in which case, the images will change once 
the user hovers over the images.</p>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>CSS: Photo App</h4>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->

<details>
  <summary>CSS</summary>

```css
header {
  background-color: #f8f9fa;
  padding: 20px;
  text-align: center;
  border-bottom: 1px solid #ccc;
  font-family: 'Roboto', sans-serif;
}
header h1 {
  font-size: 24px;
  color: #333;
}
header p {
  font-size: 16px;
  color: #666;
}

#gallery {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(200px, 1fr));
  gap: 10px;
  padding: 20px;
  font-family: 'Roboto', sans-serif;
}
.photo {
  position: relative;
}
.photo img {
  width: 100%;
  height: auto;
  display: block;
}
.photo .caption {
  position: absolute;
  bottom: 0;
  background: rgba(0, 0, 0, 0.5);
  color: #fff;
  width: 100%;
  text-align: center;
  padding: 5px 0;
}

nav button {
  background-color: #fff;
  border: 1px solid #ddd;
  padding: 10px 20px;
  margin: 10px;
  cursor: pointer;
  transition: background-color 0.3s;
  font-family: 'Roboto', sans-serif;
}
nav button:hover {
  background-color: #eee;
}

.modal {
  display: none;
  position: fixed;
  z-index: 1000;
  left: 0;
  top: 0;
  width: 100%;
  height: 100%;
  overflow: auto;
  background-color: rgb(0,0,0,0.9);
  font-family: 'Roboto', sans-serif;
}
.modal-content {
  margin: auto;
  display: block;
  width: 80%;
  max-width: 700px;
}
.close {
  position: absolute;
  top: 15px;
  right: 35px;
  color: #f1f1f1;
  font-size: 40px;
  font-weight: bold;
  cursor: pointer;
}
.close:hover,
.close:focus {
  color: #bbb;
  text-decoration: none;
  cursor: pointer;
}
#caption {
  color: #ccc;
  font-size: 16px;
  padding: 15px 20px;
  text-align: center;
  width: 100%;
}

@media (max-width: 600px) {
  #gallery {
    grid-template-columns: repeat(auto-fill, minmax(150px, 1fr));
  }
}
```

</details>

<h4>JavaScript: Photo App</h4>

<details>
  <summary>JavaScript</summary>

```javascript
function filterGallery(category) {
  const photos = document.querySelectorAll('.photo');
  photos.forEach(photo => {
    const isVisible = category === 'all' || photo.classList.contains(category);
    photo.style.display = isVisible ? '' : 'none';
  });
}

document.querySelectorAll('.photo img').forEach(img => {
  img.addEventListener('click', function() {
    const modal = document.getElementById('myModal');
    const modalImg = document.getElementById('img01');
    const captionText = document.getElementById('caption');
    modal.style.display = 'block';
    modalImg.src = this.src;
    captionText.innerHTML = this.nextElementSibling.innerHTML;
  });
});

const closeButton = document.querySelector('.close');
closeButton.onclick = function() {
  const modal = document.getElementById('myModal');
  modal.style.display = 'none';
}

document.addEventListener('keydown', function(event) {
  if (event.key === 'Escape') {
    const modal = document.getElementById('myModal');
    if (modal.style.display === 'block') {
      modal.style.display = 'none';
    }
  }
});
```

</details>

<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3 id="ch8">8. Build an Interactive Landing Page</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<p>This project involves building a dynamic landing page that stores your name and text written in local 
storage, and shows you an appropriate image and greeting message based on the day's time. This YouTube 
video will help you learn about this project’s JS components.</p>

https://www.youtube.com/watch?v=fSTQzlprGLI

<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>HTML</h4>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<details>
  <summary>HTML</summary>

</details>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>CSS</h4>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<details>
  <summary>CSS</summary>

</details>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>JavaScript</h4>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<details>
  <summary>JavaScript</summary>

</details>

<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3 id="ch9">9. Single Page Application</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<p>Here, the page won’t reload upon navigating the side links, but the content will change. Again, we will 
use eventListeners to change the view from one link to another. Check out the code and explanation on 
this YouTube video.</p>

https://www.youtube.com/watch?v=6BozpmSjk-Y

<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>HTML</h4>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<details>
  <summary>HTML</summary>

</details>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>CSS</h4>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<details>
  <summary>CSS</summary>

</details>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>JavaScript</h4>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<details>
  <summary>JavaScript</summary>

</details>

<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3 id="ch10">10. JavaScript To-Do List</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<p>In this JavaScript project, you'll build a To-Do List app, a practical and highly useful application 
that is a staple in many people's daily productivity routines.</p>

<p>This project is not just about creating a functional tool; it’s also a brilliant demonstration of 
how JavaScript can be used to enhance the interactivity and responsiveness of web pages.</p>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>HTML</h4>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<details>
  <summary>HTML</summary>

```
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>To-Do List App</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>
  <div id="todo-app">
    <h1>My To-Do List</h1>
    <form id="todo-form">
      <input type="text" id="todo-input" placeholder="Add a new task...">
      <button type="submit">Add Task</button>
    </form>
    <ul id="todo-list">
      <!-- Tasks will be added here -->
    </ul>
  </div>
  <script src="script.js"></script>
</body>
</html>
```

</details>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>CSS</h4>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<details>
  <summary>CSS</summary>

```
body {
  font-family: 'Arial', sans-serif;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  height: 100vh;
  margin: 0;
  background: linear-gradient(to right, #6DD5FA, #FF758C);
  color: #333;
}

#todo-app {
  width: 80%;
  max-width: 400px;
  margin: 0 auto;
  padding: 20px;
  background-color: #fff;
  border-radius: 10px;
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
}

#todo-form input[type="text"] {
  width: 70%;
  padding: 10px;
  border: 2px solid #ddd;
  border-radius: 4px;
  margin-right: 10px;
}

#todo-form button {
  padding: 10px 20px;
  background-color: #5F9EA0;
  color: white;
  border: none;
  border-radius: 4px;
  cursor: pointer;
  transition: background-color 0.3s;
}

#todo-form button:hover {
  background-color: #4682B4;
}

#todo-list {
  list-style: none;
  padding: 0;
}

#todo-list li {
  background-color: #f9f9f9;
  margin-top: 10px;
  padding: 10px;
  border-radius: 4px;
  display: flex;
  justify-content: space-between;
  align-items: center;
}
```

</details>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>JavaScript</h4>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<details>
  <summary>JavaScript</summary>
  
```
const todoForm = document.getElementById('todo-form');
const todoInput = document.getElementById('todo-input');
const todoList = document.getElementById('todo-list');

todoForm.addEventListener('submit', function(event) {
  event.preventDefault();
  const newTask = todoInput.value;

  if (newTask === '') {
      alert('Please enter a task!');
      return;
  }
  todoInput.value = '';
  addTask(newTask);
});

function addTask(task) {
  const listItem = document.createElement('li');
  const taskText = document.createElement('span');
  taskText.textContent = task;
  listItem.appendChild(taskText);

  const checkBox = document.createElement('input');
  checkBox.setAttribute('type', 'checkbox');
  listItem.appendChild(checkBox);

  const deleteButton = document.createElement('button');
  deleteButton.textContent = 'Delete';
  listItem.appendChild(deleteButton);

  todoList.appendChild(listItem);

  const editButton = document.createElement('button');
  editButton.textContent = 'Edit';
  listItem.appendChild(editButton);

  checkBox.addEventListener('change', function() {
      if (this.checked) {
          taskText.style.textDecoration = 'line-through';
      } else {
          taskText.style.textDecoration = 'none';
      }
  });
 
  deleteButton.addEventListener('click', function() {
      todoList.removeChild(listItem);
  });

  editButton.addEventListener('click', function() {
      const isEditing = listItem.classList.contains('editing');
 
      if (isEditing) {
         
          taskText.textContent = this.previousSibling.value;
          listItem.classList.remove('editing');
          editButton.textContent = 'Edit';
      } else {
         
          const input = document.createElement('input');
          input.type = 'text';
          input.value = taskText.textContent;
          listItem.insertBefore(input, taskText);
          listItem.removeChild(taskText);
          listItem.classList.add('editing');
          editButton.textContent = 'Save';
      }
  });

  saveTasksToLocalStorage();
}

function saveTasksToLocalStorage() {
  const tasks = [];
  document.querySelectorAll('#todo-list li').forEach(task => {
      const taskText = task.querySelector('span').textContent;
      const isCompleted = task.classList.contains('completed');
      tasks.push({ text: taskText, completed: isCompleted });
  });
  localStorage.setItem('tasks', JSON.stringify(tasks));
}

document.addEventListener('DOMContentLoaded', function() {
  const savedTasks = JSON.parse(localStorage.getItem('tasks')) || [];
  savedTasks.forEach(task => {
      addTask(task.text);
  });
});
```

</details>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3 id="ch11">11. JavaScript Rock, Paper, Scissors Game</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<p>In this JavaScript project, you'll create the timeless classic Rock Paper Scissors game. It really 
needs no introduction, but this is an engaging and interactive application that brings a classic 
game to your web browser.</p>

<p>But this JavaScript project goes beyond merely replicating a well-known game; it's also a fantastic 
showcase of JavaScript's power to create dynamic and responsive web experiences.</p>

<p>It's also a solid portfolio piece, particularly if you want to highlight your web development 
prowess by using core programming principles in a context that's both enjoyable and easy to 
understand.</p>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>HTML</h4>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<details>
  <summary>HTML</summary>

```
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Rock-Paper-Scissors Game</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>
  <div id="rps-game">
      <h1>Rock-Paper-Scissors</h1>
      <div id="choices">
          <button id="rock">Rock</button>
          <button id="paper">Paper</button>
          <button id="scissors">Scissors</button>
      </div>
      <div id="result">
          <!-- Result will be displayed here -->
      </div>
      <div id="game-info">
          <div id="round">Round: 1 of 5</div>
          <div id="scoreboard">
              <div id="player-score">Player Score: 0</div>
              <div id="computer-score">Computer Score: 0</div>
          </div>
      </div>
  </div>
  <script src="script.js"></script>
</body>
</html>
```

</details>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>CSS</h4>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<details>
  <summary>CSS</summary>

```
body {
  font-family: 'Arial', sans-serif;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  height: 100vh;
  margin: 0;
  background: linear-gradient(to right, #56AB2F, #A8E063);
  color: #333;
}

#rps-game {
  width: 80%;
  max-width: 600px;
  margin: 0 auto;
  padding: 20px;
  background-color: #fff;
  border-radius: 10px;
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
  text-align: center; /* Center the game content */
}

#choices button {
  padding: 15px 25px;
  background-color: #4CAF50;
  color: white;
  border: none;
  border-radius: 5px;
  cursor: pointer;
  font-size: 18px;
  margin: 10px;
  transition: background-color 0.3s;
}

#choices button:hover {
  background-color: #0056b3;
}

#result {
  margin-top: 20px;
  font-size: 24px;
  font-weight: bold;
}

#scoreboard {
  margin-top: 20px;
  font-size: 20px;
}

#player-score, #computer-score {
  margin: 10px;
}

#game-info {
  text-align: center;
  margin-bottom: 20px;
}

#round {
  font-size: 20px;
  margin: 10px 0;
}
```

</details>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>JavaScript</h4>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<details>
  <summary>JavaScript</summary>
  
```
const rockButton = document.getElementById('rock');
const paperButton = document.getElementById('paper');
const scissorsButton = document.getElementById('scissors');
const resultDisplay = document.getElementById('result');

rockButton.addEventListener('click', () => playRound('rock'));
paperButton.addEventListener('click', () => playRound('paper'));
scissorsButton.addEventListener('click', () => playRound('scissors'));

let playerScore = 0;
let computerScore = 0;
const playerScoreDisplay = document.getElementById('player-score');
const computerScoreDisplay = document.getElementById('computer-score');

let currentRound = 1;
const totalRounds = 5; // You can adjust this number based on how long you want the game to be
const roundDisplay = document.getElementById('round');

function playRound(playerChoice) {
    if (currentRound <= totalRounds) {

        roundDisplay.textContent = `Round: ${currentRound} of ${totalRounds}`;
        currentRound++;
        console.log(currentRound)

        const choices = ['rock', 'paper', 'scissors'];
        const computerChoice = choices[Math.floor(Math.random() * choices.length)];

        if (playerChoice === computerChoice) {
            resultDisplay.textContent = 'It\'s a draw!';
        } else if (
            (playerChoice === 'rock' && computerChoice === 'scissors') ||
            (playerChoice === 'paper' && computerChoice === 'rock') ||
            (playerChoice === 'scissors' && computerChoice === 'paper')
        ) {
            resultDisplay.textContent = 'You win!';
            playerScore++;
        } else {
            resultDisplay.textContent = 'Computer wins!';
            computerScore++;
        }

        playerScoreDisplay.textContent = `Player Score: ${playerScore}`;
        computerScoreDisplay.textContent = `Computer Score: ${computerScore}`;

    }
    
    if (currentRound > totalRounds) {
        concludeGame();
    }
}

function concludeGame() {
    const gameContainer = document.getElementById('rps-game');
    const choices = document.getElementById('choices');
    const gameInfo = document.getElementById('game-info');
    const roundRes = document.getElementById('result');
    if (choices) {
        choices.style.display = 'none';
    }

    if (gameInfo) {
        gameInfo.style.display = 'none';
    }

    if (roundRes) {
        roundRes.style.display = 'none';
    }

    const gameConclusion = document.createElement('div');
    gameConclusion.setAttribute('id', 'game-conclusion');

    let finalMessage = '';
    if (playerScore > computerScore) {
        finalMessage = 'Congratulations, you won the game!';
    } else if (playerScore < computerScore) {
        finalMessage = 'Game over, the computer wins!';
    } else {
        finalMessage = 'The game ends in a draw!';
    }

    gameConclusion.innerHTML = `
        <h2>Game Over</h2>
        <p>${finalMessage}</p>
        <p>Final Score - You: ${playerScore} | Computer: ${computerScore}</p>
        <button id="restart-btn">Restart Game</button>
    `;

    gameContainer.appendChild(gameConclusion);
    document.getElementById('restart-btn').addEventListener('click', restartGame);
}

function restartGame() {
    playerScore = 0;
    computerScore = 0;
    currentRound = 1;

    playerScoreDisplay.textContent = 'Player Score: 0';
    computerScoreDisplay.textContent = 'Computer Score: 0';
    roundDisplay.textContent = `Round: 1 of ${totalRounds}`;

    const choices = document.getElementById('choices');
    const gameInfo = document.getElementById('game-info');
    const roundRes = document.getElementById('result');
    if (choices) {
        choices.style.display = '';
    }

    if (gameInfo) {
        gameInfo.style.display = '';
    }

    if (roundRes) {
        roundRes.style.display = '';
    }

    const gameConclusion = document.getElementById('game-conclusion');
    if (gameConclusion) {
        gameConclusion.remove();
    }

    document.getElementById('choices').style.display = '';
    resultDisplay.textContent = 'Choose your weapon!';
}
```

</details>

<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3 id="ch12">12. JavaScript Countdown Timer</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->

<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>HTML</h4>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<details>
  <summary>HTML</summary>

```
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Countdown Timer</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>
  <div id="countdown">
      <p id="timer">
          <span id="days"></span>
          <span class="timer-unit">Days</span>
          <span id="hours"></span>
          <span class="timer-unit">Hours</span>
          <span id="minutes"></span>
          <span class="timer-unit">Minutes</span>
          <span id="seconds"></span>
          <span class="timer-unit">Seconds</span>
      </p>
  </div>
  <script src="script.js"></script>
</body>
</html>
```

</details>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>CSS</h4>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<details>
  <summary>CSS</summary>

```
body {
  font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
  margin: 0;
  background: linear-gradient(135deg, #6dd5ed, #2193b0);
  color: white;
}

#countdown {
  background: rgba(0, 0, 0, 0.7);
  padding: 40px 60px;
  border-radius: 15px;
  box-shadow: 0 10px 25px rgba(0, 0, 0, 0.3);
  text-align: center;
}

#timer {
  font-size: 3rem;
  letter-spacing: 3px;
}

.timer-unit {
  font-size: 1.2rem;
  text-transform: uppercase;
  letter-spacing: 2px;
  margin-top: 10px;
  display: inline;
}
```

</details>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>JavaScript</h4>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<details>
  <summary>JavaScript</summary>
  
```
const targetDate = new Date('YYYY-MM-DDTHH:MM:SS'); // Set your target

function updateCountdown() {
  const currentTime = new Date();
  const difference = targetDate - currentTime;

  const days = Math.floor(difference / (1000 * 60 * 60 * 24));
  const hours = Math.floor((difference % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));
  const minutes = Math.floor((difference % (1000 * 60 * 60)) / (1000 * 60));
  const seconds = Math.floor((difference % (1000 * 60)) / 1000);

  document.getElementById("days").innerText = days;
  document.getElementById("hours").innerText = hours;
  document.getElementById("minutes").innerText = minutes;
  document.getElementById("seconds").innerText = seconds;

  if (difference < 0) {
      clearInterval(interval);
      document.getElementById("timer").innerText = "The event has started!";
  }
}

const interval = setInterval(updateCountdown, 1000);
```

</details>

<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3 id="ch13">13. Animated Business Card</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
[Animated Business Card](https://hackr.io/blog/how-to-create-a-html-animated-business-card)

</details>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>HTML</h4>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<details>
  <summary>HTML</summary>


```
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Alex Carter - Business Card</title>
  <link href="https://fonts.googleapis.com/css2?family=Roboto:wght@400;700&display=swap" rel="stylesheet">
  <link rel="stylesheet" href="styles.css">
</head>
<body>
  <div id="businessCard">
      <img src="alex-carter.jpg" alt="Alex Carter" class="profile-photo">
      <!-- <a href="https://www.freepik.com/free-photo/young-male-posing-isolated-against-blank-studio-wall_10110817.htm#query=male%20headshot&position=1&from_view=keyword&track=ais&uuid=43edf3b5-1fff-4353-a9d7-bbe75f59e87b">Image by wayhomestudio</a> on Freepik -->
      <h1>Alex Carter</h1>
      <p>Junior Web Developer</p>
      <p>Email: <a href="mailto:alex.carter.dev@example.com">alex.carter.dev@example.com</a></p>
      <div id="socialLinks">
          <p>LinkedIn: <a href="https://www.linkedin.com/in/alex-carter-dev" target="_blank">alex-carter-dev</a></p>
      </div>
      <div id="bio">
          <h2>About Me</h2>
          <p>I recently graduated from MIT with a degree in Computer Science, specializing in web development. I am passionate about building responsive and user-friendly websites and applications.</p>
      </div>
  </div>
</body>
</html>
```

</details>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>CSS</h4>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<details>
  <summary>CSS</summary>

```
body {
  font-family: 'Roboto', sans-serif;
  background-color: #f4f4f4;
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
  margin: 0;
}

#businessCard {
  box-shadow: 0 0 20px rgba(0, 0, 0, 0.1);
  background-color: white;
  padding: 20px;
  width: 350px;
  text-align: center;
  border-radius: 10px;
}

.profile-photo {
  width: 100px;
  height: auto;
  border-radius: 50%;
  margin: 20px 0;
  transition: transform 0.3s ease-in-out;
}

h1 {
  color: #333;
  font-size: 24px;
}

p {
  color: #666;
  font-size: 16px;
}

a {
  color: #1a0dab;
  text-decoration: none;
}

a:hover {
  text-decoration: underline;
}

.profile-photo:hover {
  transform: scale(1.1);
}

@media only screen and (max-width: 600px) {
  #businessCard {
      width: 90%;
      padding: 10px;
  }
}
```

</details>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3 id="ch14">14. Interactive Photo Gallery</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->

<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>HTML</h4>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<details>
  <summary>HTML</summary>


```
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Interactive Photo Gallery</title>
  <link rel="stylesheet" href="styles.css">
  <link href="https://fonts.googleapis.com/css2?family=Roboto:wght@400;700&display=swap" rel="stylesheet">
  <script src="script.js" defer></script>
</head>
<body>
  <header>
      <h1>My Photo Gallery</h1>
      <p>Explore my collection of high-quality images ranging from landscapes to portraits.</p>
    </header>
    <nav>
      <button class="filter" onclick="filterGallery('all')">All</button>
      <button class="filter" onclick="filterGallery('landscapes')">Landscapes</button>
      <button class="filter" onclick="filterGallery('portraits')">Portraits</button>
      <!-- Add more filters as needed -->
    </nav>
  <section id="gallery">
    <div class="photo">
      <img src="other_1.jpg" alt="Hot Air Balloon">
      <p class="caption">Hot Air Balloon</p>
    </div>
    <div class="photo">
      <img src="other_2.jpg" alt="Carpenter In Front Of House">
      <p class="caption">Carpenter In Front Of House</p>
    </div>
    <div class="photo">
      <img src="other_3.jpg" alt="Surfer Catching Air">
      <p class="caption">Surfer Catching Air</p>
    </div>
    <div class="photo landscapes">
      <img src="landscape_1.jpg" alt="Lake With Mountains">
      <p class="caption">Lake With Mountains</p>
    </div>
    <div class="photo landscapes">
      <img src="landscape_2.jpg" alt="Cabin On The Lake">
      <p class="caption">Cabin On The Lake</p>
    </div>
    <div class="photo landscapes">
      <img src="landscape_3.jpg" alt="Dramatic Hillside">
      <p class="caption">Dramatic Hillside</p>
    </div>
    <div class="photo portraits">
      <img src="portrait_1.jpg" alt="Dramatic Female Portrait">
      <p class="caption">Dramatic Female Portrait</p>
    </div>
    <div class="photo portraits">
      <img src="portrait_2.jpg" alt="Woman With Balloons">
      <p class="caption">Woman With Balloons</p>
    </div>
    <div class="photo portraits">
      <img src="portrait_3.jpg" alt="Woman With Binary Projection">
      <p class="caption">Woman With Binary Projection</p>
    </div>
  </section>
  <div id="myModal" class="modal">
    <span class="close">&times;</span>
    <img class="modal-content" id="img01">
    <div id="caption"></div>
  </div>  
</body>
</html>
```

</details>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>CSS</h4>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<details>
  <summary>CSS</summary>

```
header {
  background-color: #f8f9fa;
  padding: 20px;
  text-align: center;
  border-bottom: 1px solid #ccc;
  font-family: 'Roboto', sans-serif;
}
header h1 {
  font-size: 24px;
  color: #333;
}
header p {
  font-size: 16px;
  color: #666;
}

#gallery {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(200px, 1fr));
  gap: 10px;
  padding: 20px;
  font-family: 'Roboto', sans-serif;
}
.photo {
  position: relative;
}
.photo img {
  width: 100%;
  height: auto;
  display: block;
}
.photo .caption {
  position: absolute;
  bottom: 0;
  background: rgba(0, 0, 0, 0.5);
  color: #fff;
  width: 100%;
  text-align: center;
  padding: 5px 0;
}

nav button {
  background-color: #fff;
  border: 1px solid #ddd;
  padding: 10px 20px;
  margin: 10px;
  cursor: pointer;
  transition: background-color 0.3s;
  font-family: 'Roboto', sans-serif;
}
nav button:hover {
  background-color: #eee;
}

.modal {
  display: none;
  position: fixed;
  z-index: 1000;
  left: 0;
  top: 0;
  width: 100%;
  height: 100%;
  overflow: auto;
  background-color: rgb(0,0,0,0.9);
  font-family: 'Roboto', sans-serif;
}
.modal-content {
  margin: auto;
  display: block;
  width: 80%;
  max-width: 700px;
}
.close {
  position: absolute;
  top: 15px;
  right: 35px;
  color: #f1f1f1;
  font-size: 40px;
  font-weight: bold;
  cursor: pointer;
}
.close:hover,
.close:focus {
  color: #bbb;
  text-decoration: none;
  cursor: pointer;
}
#caption {
  color: #ccc;
  font-size: 16px;
  padding: 15px 20px;
  text-align: center;
  width: 100%;
}

@media (max-width: 600px) {
  #gallery {
      grid-template-columns: repeat(auto-fill, minmax(150px, 1fr));
  }
}
```

</details>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>JS</h4>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<details>
  <summary>JS</summary>

```
function filterGallery(category) {
  const photos = document.querySelectorAll('.photo');
  photos.forEach(photo => {
    const isVisible = category === 'all' || photo.classList.contains(category);
    photo.style.display = isVisible ? '' : 'none';
  });
}

document.querySelectorAll('.photo img').forEach(img => {
  img.addEventListener('click', function() {
    const modal = document.getElementById('myModal');
    const modalImg = document.getElementById('img01');
    const captionText = document.getElementById('caption');
    modal.style.display = 'block';
    modalImg.src = this.src;
    captionText.innerHTML = this.nextElementSibling.innerHTML;
  });
});

const closeButton = document.querySelector('.close');
closeButton.onclick = function() {
  const modal = document.getElementById('myModal');
  modal.style.display = 'none';
}

document.addEventListener('keydown', function(event) {
  if (event.key === 'Escape') {
    const modal = document.getElementById('myModal');
    if (modal.style.display === 'block') {
      modal.style.display = 'none';
    }
  }
});
```

</details>

<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3 id="ch15">15. 10 Best Computer Science Projects To Hone Your Skills</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->

<a href="https://hackr.io/blog/best-computer-science-projects?source=k8mepg2dMy">here</a>

<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3 id="ch16">16. Text to Speech Converter</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<p></p>
<details>
  <summary>HTML</summary>

```
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content=
        "width=device-width, initial-scale=1.0">
    <title>Text to Speech Converter</title>
    <link rel="stylesheet" href="style.css">
</head>

<body>
    <div class="container">
        <div class="app-container">
            <div class="headings-container">
                <h1>Text to Speech Converter</h1>
                <h3>Enter Text and Convert into Speech</h3>
            </div>

            <div class="interaction-container">
                <textarea id="textToConvert" 
                    placeholder="Enter text to convert into speech..." 
                    id="" cols="35" rows="10" 
                    class="text-control"></textarea>

                <p class="error-para"></p>

                <button class="btn" id="convertBtn">
                    Play Converted Sound
                </button>
            </div>
        </div>
    </div>

    <script src="script.js"></script>
</body>

</html>
```

</details>
<details>
  <summary>CSS</summary>

```
@import url('https://fonts.googleapis.com/css2?family=Poppins&display=swap');

body {
    padding: 0;
    margin: 0;
    box-sizing: border-box;
    font-family: "Poppins", sans-serif;
}

.container {
    height: 100vh;
    width: 100%;
    display: flex;
    align-items: center;
    justify-content: center;
    background-image: linear-gradient(90deg, #161578, #b81055);
}

.app-container {
    display: flex;
    align-items: center;
    justify-content: center;
    flex-direction: column;
    text-align: center;
    color: #fff;
}

.headings-container {
    padding: 0 1rem;
}

.interaction-container {
    display: flex;
    align-items: normal;
    justify-content: center;
    flex-direction: column;
    text-align: center;
    padding: 0 1rem;
}

.text-control {
    padding: 0.5rem;
    margin: 2rem 0;
    background-color: #3f464a52;
    color: #fff;
    border: 1px solid #fff;
    border-radius: 10px;
}

.text-control:focus-visible {
    outline: none;
}

.error-para {
    color: red;
}

.btn {
    padding: 0.8rem;
    background-image: linear-gradient(90deg, #F4244C, #F57D4E);
    border: 1px solid transparent;
    border-radius: 10px;
    color: #fff;
    cursor: pointer;
    transition: all 0.25s;
}

.btn:hover {
    padding: 1rem;
}
```

</details>
<details>
  <summary>JS</summary>

```
const text = document.getElementById("textToConvert");
const convertBtn = document.getElementById("convertBtn");

convertBtn.addEventListener('click', function () {
    const speechSynth = window.speechSynthesis;
    const enteredText = text.value;
    const error = document.querySelector('.error-para');

    if (!speechSynth.speaking &&
        !enteredText.trim().length) {
        error.textContent = `Nothing to Convert! 
        Enter text in the text area.`
    }
    
    if (!speechSynth.speaking && enteredText.trim().length) {
        error.textContent = "";
        const newUtter =
            new SpeechSynthesisUtterance(enteredText);
        speechSynth.speak(newUtter);
        convertBtn.textContent = "Sound is Playing..."
    }
    
    setTimeout(() => {
        convertBtn.textContent = "Play Converted Sound"
    }, 5000);
});
```

</details>

<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3 id="ch17">17. JavaScript Map Reference</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<p>JavaScript Map is a collection of elements where each element is stored as a key, value pair. 
Map objects can hold both objects and primitive values as either key or value. When we iterate over 
the map object it returns the key, and value pair in the same order as inserted.</p>

You can create a JavaScript Map by:

  - Passing an Array to new Map()
  - Create a Map and use Map.set()

<h4>Passing an Array to new Map()</h4>
<p>Example: In this example, an array of key-value pairs is passed to the Map constructor to create 
a Map. Each sub-array [key, value] represents a key-value pair.</p>

```
// Create a Map by passing an Array of key-value pairs to the Map constructor
const arrayMap = new Map([
    ['key1', 'value1'],
    ['key2', 'value2'],
    ['key3', 'value3']
]);

// Accessing values in the Map
console.log(arrayMap.get('key1'));  // Output: "value1"
console.log(arrayMap.get('key2'));  // Output: "value2"
console.log(arrayMap.get('key3'));  // Output: "value3"
```

<h4>Create a Map and use Map.set()</h4>
<p>Example: In this example, an empty Map is created, and then key-value pairs are added using the 
Map.set() method. This approach is useful when you want to dynamically build a Map during runtime.</p>

```
// Create an empty Map and use Map.set() to add key-value pairs
const setMap = new Map();

// Adding key-value pairs using Map.set()
setMap.set('name', 'John');
setMap.set('age', 25);
setMap.set('city', 'New York');

// Accessing values in the Map
console.log(setMap.get('name'));  // Output: "John"
console.log(setMap.get('age'));   // Output: 25
console.log(setMap.get('city'));  // Output: "New York"
```

<p>The complete list of JavaScript Map is listed below:</p>

<p><b>JavaScript Map Constructor:</b> In JavaScript, a constructor gets called when an object is 
created using the new keyword.</p>

| Constructor |        Description  |
|-------------|---------------------|
| Map()	| Create Map objects in JavaScript. |

<p><b>JavaScript Map Properties:</b> A JavaScript property is a member of an object that associates a key with a value.</p>

  - Instance Properties: An instance property is a property that has a new copy for every new instance of the class.

| Instance Properties |  Description |
----------------------|-------------------------------------------------------------
| constructor | It is used to return the constructor function of Map. |
| size	      |  Return the number of keys, and value pairs stored in a map. |

<p><b>JavaScript Map Methods:</b> JavaScript methods are actions that can be performed on objects.</p>

<p><b>Instance Methods:</b> If the method is called on the instance of a Map then it is called an instance method of Map.</p>

| Static Methods | Description |
|----------------|-------------------------------------------------------------------------------|
| clear( )	     | Removal of all the elements from a map and making it empty. |
| delete()	     | Delete the specified element among all the elements which are present in the map. |
| entries( )	 | Returning an iterator object which contains all the [key, value] pairs of each element of the map. |
| forEach()	     | The map with the given function executes the given function over each key-value pair. |
| get( )	     | Returning a specific element among all the elements which are present in a map. |
| has( )	     | Check whether an element with a specified key exists in a map or not. |
| keys()	     | The keys from a given map object return the iterator object of keys. |
| set()	         | Add key-value pairs to a Map object. |
| values()	     | Return a new Iterator object that contains the value of each element present in Map. |

<details>
  <summary>HTML</summary>
  
</details>
