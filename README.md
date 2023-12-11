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
There is a lot you can do with JavaScript, but we don’t want to overwhelm you with 
everything yet. We have listed the top JavaScript projects that can add value to 
your resume as well as a career:

<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>1. JavaScript Calculator</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
We will use simple HTML, CSS, and make all the components work using basic JavaScript 
functions. To display buttons and numbers, we will use HTML, and add some beautification 
to them using CSS. To make the buttons perform the respective functions we will use 
JavaScript. 

The main function is eval(), which is a global JS function that solves JS codes. The 
display() function will display the selected number on the calculator screen. Note 
that the program will work only for mouse events. Here is the complete code:

<h4>HTML: Calculator</h4>

<details>
  <summary>HTML: Calculator</summary>

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

</details>

<h4>CSS: Calculator</h4>

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

</details>

<h4>JavaScript: Calculator</h4>

<details>
  <summary>JavaScript: Calculator</summary>

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

</details>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3><a href="https://www.sololearn.com/en/compiler-playground/WyyBylG1NvdU/#js">2. Hangman Game</a></h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->

Hangman is a well-known game, and one of our simple JS projects. You can develop it in a jiffy using JavaScript, HTML, and CSS. Note that the main functionality is defined using JS. HTML is for display, and CSS does the job of beautifying the contents. 

Many methods are defined in the JS code, so it may seem a bit complicated, but you will realize it is simple once you read the code thoroughly. You can also run the code and see the execution line by line.

<h4>HTML: Hangman</h4>

<details>
  <summary>HTML: Hangman</summary>

```[html]
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

<h4>CSS: Hangman</h4>

<details>
  <summary>CSS</summary>

```
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

<h4>JavaScript: Hangman</h4>

<details>
  <summary>JavaScript: Hangman</summary>

```js
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
        if(resY < 0) {
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
    for(a = 0; a < e.length; a++) {
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
    for(a = 0; a < word[select][0].length; a++) {
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
    for(a = 0; a < tastatur.length; a++) {
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
    for(a = 0; a < word[select][0].length; a++) {
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
<h3>3. Tic Tac Toe Game</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
JavaScript makes it easy to develop a Tic-Tac-Toe game yourself. You can look at 
the entire code here, and it explains how to build a 3x3 tic-tac-toe step by step. 
Then, you can later expand to NxN for your own practice and knowledge. The HTML 
and CSS for the project are quite simple. The author first starts with pseudocode 
and then goes on to explain each function individually.

<h4>HTML: Tic-Tac-Toe</h4>

<details>
  <summary>HTML: Tic-Tac-Toe</summary>
  
```[html]
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

<h4>CSS: Tic-Tac-Toe</h4>

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

<h4>JavaScript: Tic-Tac-Toe</h4>

<details>
  <summary>JavaScript: Tic-Tac-Toe</summary>

```js
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
    for (let i = 0; i <= 7; i++) {
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

<h3>4. Weather App</h3>
Weather apps are also popular JavaScript projects. Once you change the location name in this project, the weather display changes immediately without a page refresh. The UI is also quite sleek. 

Note that most weather apps use an API that gets the weather data. We will use the popular and most common API, OpenWeatherMap. 

Check out this Youtube video that explains the weather app code and functionality in detail. There are three files, as usual: index.html, main.js, and main.css. Although you can put all the code in a single file (HTML), it is more convenient to maintain separate files. 

<h4>HTML: Weather App</h4>

<details>
  <summary>HTML: Weather App</summary>

```[html]

```

</details>


<h4>CSS: Weather App</h4>

<details>
  <summary>CSS: Weather App</summary>

```css

```

</details>

<h4>JavaScript: Weather App</h4>

<details>
  <summary>JavaScript: Weather App</summary>

```js

```

</details>

<h3>5. Music Events</h3>
Here, we’ll introduce you to event listeners that will act on keyboard events. For example, an event will take place if the ‘S’ key is pressed. Each one will have a different code and action. 

Apart from event listeners, we will also learn how to add and play audio files. Note that we have added very basic CSS, as the focus here is on JavaScript. You will have to import your own sounds and background image for the program to work fully.

<h4>HTML: Music</h4>

<details>
  <summary>HTML</summary>

```[html]
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

<h4>CSS: Music App</h4>

<details>
  <summary>CSS</summary>

```css

```

</details>

<h4>JavaScript: Music App</h4>

<details>
  <summary>JavaScript</summary>

```js

```

</details>


<h3>6. Form Validation</h3>
Form validation is a useful aspect and used by many websites for client-side validation of user information, such as card and address details. For example, if there is a mandatory input field name, the user may type a number, leave the field blank, or type just one letter. JS can validate this information. 

The project below involves simple form validation. Of course, the project will need HTML elements as well. We have not carried out any extensive styling, only including basic elements in the HTML itself. 

Here is the complete code of a simple form with basic validations:

<h4>HTML: Form Validation</h4>

<details>
  <summary>HTML</summary>

```[html]
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
   	 <h1 align="center">USER REGISTRATION</H1>
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

<h4>CSS: Form Validation</h4>

<h4>JavaScript: Form Validation</h4>


<h3>7. Photo Details Display</h3>
Here, we will display some images on a web page. Once the user hovers over the images, more details will appear. You can download images from anywhere or use the ones you already have. 

Again, we have used basic HTML and CSS along with JS. The latter carries out most of the work. You will learn how mouse hover (over and out) events work through this project.

<h4>HTML: Photo Details Display</h4>

<details>
  <summary>HTML: Photo</summary>

```[html]
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
 #image{
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
 img{
 width: 200px;
 height: 200px;
 border-radius: 50%;
 }
 </style>
 <body>
   <div>
   <p id = "image">Hover over a sunsign image to display details.<p>
   <img alt = "Sagittarius are beautiful, loyal and passionate." src = "saggi.jpg" onmouseover = "display(this)" onmouseout = "revert()">
   <img alt = "Pisces are dreamy, helpful and love everyone!" src = "pisces.jpg" onmouseover = "display(this)" onmouseout = "revert()">
   <img alt = "Leo are strong and fearless. They aim for and achieve a lot!" src = "leo.jpg" onmouseover = "display(this)" onmouseout = "revert()">
   <img alt = "Scorpions are friends for life. They are trustworthy and truthful." src = "scorpio.jpg" onmouseover = "display(this)" onmouseout = "revert()">
   </div>
 </body>
</html>
```

</details>

To make this project more complex, try this slideshow project from W3Schools. You can change the onClick events to onmousehover and onmouseout events, in which case, the images will change once the user hovers over the images.

<h4>CSS: Photo App</h4>

<details>
  <summary>CSS</summary>

```css

```

</details>

<h4>JavaScript: Photo App</h4>

<details>
  <summary>JavaScript</summary>

```js

```

</details>

<h3>8. Build an Interactive Landing Page</h3>
This project involves building a dynamic landing page that stores your name and text written in local storage, and shows you an appropriate image and greeting message based on the day's time. This YouTube video will help you learn about this project’s JS components.

https://www.youtube.com/watch?v=fSTQzlprGLI


<h4>HTML</h4>
<h4>CSS</h4>
<h4>JavaScript</h4>


<h3>9. Single Page Application</h3>
Here, the page won’t reload upon navigating the side links, but the content will change. Again, we will use eventListeners to change the view from one link to another. Check out the code and explanation on this YouTube video.

https://www.youtube.com/watch?v=6BozpmSjk-Y

<h4>HTML</h4>
<h4>CSS</h4>
<h4>JavaScript</h4>
