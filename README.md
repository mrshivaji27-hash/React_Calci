# Ex04 Simple Calculator - React Project
## Date: 16/03/2024

## AIM
To  develop a Simple Calculator using React.js with clean and responsive design, ensuring a smooth user experience across different screen sizes.

## ALGORITHM
### STEP 1
Create a React App.

### STEP 2
Open a terminal and run:
  <ul><li>npx create-react-app simple-calculator</li>
  <li>cd simple-calculator</li>
  <li>npm start</li></ul>

### STEP 3
Inside the src/ folder, create a new file Calculator.js and define the basic structure.

### STEP 4
Plan the UI: Display screen, number buttons (0-9), operators (+, -, *, /), clear (C), and equal (=).

### STEP 5
Create a new file Calculator.css in src/ and add the styling.

### STEP 6
Open src/App.js and modify it.

### STEP 7
Start the development server.
  npm start

### STEP 8
Open http://localhost:3000/ in the browser.

### STEP 9
Test the calculator by entering numbers and operations.

### STEP 10
Fix styling issues and refine content placement.

### STEP 11
Deploy the website.

### STEP 12
Upload to GitHub Pages for free hosting.

## PROGRAM
# Main.jsx
```
import React from "react";
import ReactDOM from "react-dom/client";
import App from "./App.jsx";
import "./index.css";

ReactDOM.createRoot(document.getElementById("root")).render(
  <React.StrictMode>
    <App />
  </React.StrictMode>
);
```
# index.css
```
body{
  background:#222;
  font-family: Arial;
  display:flex;
  justify-content:center;
  align-items:center;
  height:100vh;
}

.calculator{
  background:#333;
  padding:20px;
  border-radius:10px;
  width:260px;
  text-align:center;
}

h1{
  color:white;
}

.display{
  width:100%;
  height:40px;
  font-size:20px;
  margin-bottom:15px;
  text-align:right;
  padding:5px;
}

.buttons{
  display:grid;
  grid-template-columns: repeat(4,1fr);
  gap:10px;
}

button{
  padding:15px;
  font-size:18px;
  border:none;
  border-radius:5px;
  cursor:pointer;
  background:#555;
  color:white;
}

button:hover{
  background:#777;
}

.zero{
  grid-column: span 2;
}
```
# app.jsx
```
import { useState } from "react";

function App() {

  const [display, setDisplay] = useState("");

  const press = (value) => {
    setDisplay(display + value);
  };

  const clear = () => {
    setDisplay("");
  };

  const calculate = () => {
    try {
      setDisplay(eval(display).toString());
    } catch {
      setDisplay("Error");
    }
  };

  return (
    <div className="calculator">

      <input className="display" value={display} readOnly />

      <div className="buttons">

        <button onClick={clear}>C</button>
        <button onClick={() => press("/")}>/</button>
        <button onClick={() => press("*")}>*</button>
        <button onClick={() => press("-")}>-</button>

        <button onClick={() => press("7")}>7</button>
        <button onClick={() => press("8")}>8</button>
        <button onClick={() => press("9")}>9</button>
        <button onClick={() => press("+")}>+</button>

        <button onClick={() => press("4")}>4</button>
        <button onClick={() => press("5")}>5</button>
        <button onClick={() => press("6")}>6</button>

        <button onClick={() => press("1")}>1</button>
        <button onClick={() => press("2")}>2</button>
        <button onClick={() => press("3")}>3</button>

        <button onClick={() => press("0")}>0</button>
        <button onClick={() => press(".")}>.</button>
        <button onClick={calculate}>=</button>

      </div>
    </div>
  );
}

export default App;
```

## OUTPUT

<img width="154" height="243" alt="Screenshot 2026-03-17 135949" src="https://github.com/user-attachments/assets/1e587ae9-2b37-4e07-9bd0-1cbd35209b67" />

<img width="150" height="199" alt="Screenshot 2026-03-17 140624" src="https://github.com/user-attachments/assets/3e100404-f3f7-44dd-8383-46578574132a" />


## RESULT
The program for developing a simple calculator in React.js is executed successfully.
