# Ex04 Simple Calculator built with React Project
## Date:23-03-2025

## AIM
A simple calculator built with React to perform basic arithmetic operations (addition, subtraction, multiplication, and division). The project aims to demonstrate React component usage, state management, and handling user inputs dynamically.
## ALGORITHM
Set Up the React Application

Initialize a React app using npx create-react-app calculator-app.

Navigate into the project folder and start the development server with npm start.

Create a Calculator Component

Inside the src folder, create a new file Calculator.js.

Import React and set up the calculator structure with display and buttons.

Manage State and Functions

Use useState to manage user input.

Create functions for handling button clicks, performing calculations, and clearing input.

Render Buttons Dynamically

Create buttons for numbers, operators, and actions (C, =, etc.).

Assign onClick event handlers to buttons to update input or trigger calculations.

Style the Calculator (Optional)

Create a Calculator.css file and add styles for layout, display, and buttons.

Import the CSS file in Calculator.js.

Integrate the Component in App.js

Import and render the Calculator component in App.js.

Test the Application

Run npm start and test functionalities like addition, subtraction, multiplication, division, and clearing input.
## PROGRAM
App.Css
```
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body {
  font-family: Arial, sans-serif;
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
  background: linear-gradient(135deg, #3498db, #8e44ad);
}

.container {
  width: 300px;
}

.calculator {
  background-color: white;
  padding: 20px;
  border-radius: 10px;
  box-shadow: 0 4px 10px rgba(0, 0, 0, 0.2);
}

.display input {
  width: 100%;
  height: 60px;
  font-size: 24px;
  text-align: right;
  margin-bottom: 10px;
  padding: 5px;
  border: none;
  border-radius: 5px;
  background-color: rgb(240, 240, 240);
}

.buttons {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  gap: 10px;
}

button {
  height: 60px;
  font-size: 20px;
  background-color: rgb(91, 91, 151);
  color: white;
  border: none;
  border-radius: 10px;
  cursor: pointer;
}

button:hover {
  background-color: rgb(137, 22, 245);
}

button:active {
  background-color: rgb(100, 100, 200);
}

button:nth-child(16) {
  background-color: rgb(220, 53, 69); /* Red for 'C' */
}
```
App.js
```
import React, { useState } from 'react';
import './App.css';

function App() {
  const [input, setInput] = useState('');

  const handleClick = (value) => {
    setInput(input + value);
  };

  const clearInput = () => {
    setInput('');
  };

  const calculateResult = () => {
    try {
      setInput(eval(input));
    } catch {
      setInput('Error');
    }
  };

  return (
    <div className="container">
      <div className="calculator">
        <form className="display">
          <input type="text" value={input} readOnly />
        </form>

        <div className="buttons">
          <button onClick={() => handleClick('1')}>1</button>
          <button onClick={() => handleClick('2')}>2</button>
          <button onClick={() => handleClick('3')}>3</button>
          <button onClick={() => handleClick('+')}>+</button>

          <button onClick={() => handleClick('4')}>4</button>
          <button onClick={() => handleClick('5')}>5</button>
          <button onClick={() => handleClick('6')}>6</button>
          <button onClick={() => handleClick('-')}>-</button>

          <button onClick={() => handleClick('7')}>7</button>
          <button onClick={() => handleClick('8')}>8</button>
          <button onClick={() => handleClick('9')}>9</button>
          <button onClick={() => handleClick('*')}>*</button>

          <button onClick={() => handleClick('0')}>0</button>
          <button onClick={clearInput}>C</button>
          <button onClick={calculateResult}>=</button>
          <button onClick={() => handleClick('/')}>/</button>
        </div>
      </div>
    </div>
  );
}

export default App;
```
index.js
```
import React, { useState } from 'react';
import './App.css';

function App() {
  const [input, setInput] = useState('');

  const handleClick = (value) => {
    setInput(input + value);
  };

  const clearInput = () => {
    setInput('');
  };

  const calculateResult = () => {
    try {
      setInput(eval(input));
    } catch {
      setInput('Error');
    }
  };

  return (
    <div className="container">
      <div className="calculator">
        <form className="display">
          <input type="text" value={input} readOnly />
        </form>

        <div className="buttons">
          <button onClick={() => handleClick('1')}>1</button>
          <button onClick={() => handleClick('2')}>2</button>
          <button onClick={() => handleClick('3')}>3</button>
          <button onClick={() => handleClick('+')}>+</button>

          <button onClick={() => handleClick('4')}>4</button>
          <button onClick={() => handleClick('5')}>5</button>
          <button onClick={() => handleClick('6')}>6</button>
          <button onClick={() => handleClick('-')}>-</button>

          <button onClick={() => handleClick('7')}>7</button>
          <button onClick={() => handleClick('8')}>8</button>
          <button onClick={() => handleClick('9')}>9</button>
          <button onClick={() => handleClick('*')}>*</button>

          <button onClick={() => handleClick('0')}>0</button>
          <button onClick={clearInput}>C</button>
          <button onClick={calculateResult}>=</button>
          <button onClick={() => handleClick('/')}>/</button>
        </div>
      </div>
    </div>
  );
}

export default App;
```


## OUTPUT
![image](https://github.com/user-attachments/assets/47aefa1a-a60d-4ee1-bd2e-41a999565f03)


## RESULT
The program for creating Simple Calculator built with React Project is executed successfully.
