# skilwill
// დავალება პირველი
// #####
// #####
html

<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Document</title>
    <link rel="stylesheet" href="style.css" />
  </head>
  <body>
    <button id="myButton">Open Modal</button>

    <div id="myModal" class="modal">
      <div class="modal-content">
        <span class="close">&times;</span>
        <h2>Modal Title</h2>
        <p>This is the modal content.</p>
      </div>
    </div>
  </body>

  <script src="./index.js"></script>
</html>

css

.modal {
  display: none;
  position: fixed;
  z-index: 999;
  left: 0;
  top: 0;
  width: 100%;
  height: 100%;
  overflow: auto;
  background-color: rgba(0, 0, 0, 0.5);
}

.modal-content {
  background-color: #fefefe;
  margin: 15% auto;
  padding: 20px;
  border: 1px solid #888;
  width: 80%;
}

.close {
  color: #aaa;
  float: right;
  font-size: 28px;
  font-weight: bold;
  cursor: pointer;
}

.close:hover,
.close:focus {
  color: black;
  text-decoration: none;
  cursor: pointer;
}

js

const button = document.getElementById("myButton");

const modal = document.getElementById("myModal");

const closeBtn = document.getElementsByClassName("close")[0];

button.addEventListener("click", function () {
  modal.style.display = "block";
});

closeBtn.addEventListener("click", function () {
  modal.style.display = "none";
});

window.addEventListener("click", function (event) {
  if (event.target == modal) {
    modal.style.display = "none";
  }
});

 
 // დავალება მეორე
// #####
// #####
 
html

<input id="colorInput" type="text" placeholder="Enter a color">
<button onclick="changeBackgroundColor()">Change Background Color</button>

 js
 
function changeBackgroundColor() {
  const colorInput = document.getElementById("colorInput");
  const color = colorInput.value.toLowerCase();

  const validColors = ["red", "blue", "green", "black", "white"];

  if (validColors.includes(color)) {
    document.body.style.backgroundColor = color;
  } else {
    alert("Invalid color entered!");
  }
}

 
  // დავალება მესამე
// #####
// #####
HTMl

  <!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Document</title>
    <link rel="stylesheet" href="./style.css" />
  </head>
  <body>
    <input
      type="text"
      id="numbersInput"
      placeholder="Enter numbers separated by ':'"
    />
    <button id="averageButton">Average</button>
    <p id="result"></p>

    <script src="./index.js"></script>
  </body>
</html>

 Js 
// Get the input element
const numbersInput = document.getElementById("numbersInput");

// Get the button element
const averageButton = document.getElementById("averageButton");

// Get the result element
const result = document.getElementById("result");

// Add event listener to the button
averageButton.addEventListener("click", function () {
  const numbers = numbersInput.value.split(":");
  let sum = 0;

  // Calculate the sum of the numbers
  for (var i = 0; i < numbers.length; i++) {
    sum += parseInt(numbers[i]);
  }

  // Calculate the average
  const average = sum / numbers.length;

  // Display the result
  result.textContent = "Average: " + average.toFixed(2);
});

   
   
   
   
   
   
   
   
   
   
   
   
   
   
   
   
   
   
   
   
   
    
    
