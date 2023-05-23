# skilwill
// დავალება პირველი
// #####
// #####

HTML
<button id="myButton">Click Me</button>
<div id="myDiv">Working</div> -->
    
Js

 const myButton = document.getElementById(`myButton`);
 const myDiv = document.getElementById(`myDiv`);

 myButton.addEventListener("click", function () {
  myDiv.style.display = `none`;
 });
 
 // დავალება მეორე
// #####
// #####
 Js
 
 const div = document.createElement("div");
 div.id = "card";
 const h2 = document.createElement("h2");
 h2.textContent = "Gandalf";
 const a = document.createElement("a");
 a.href = "#";
 a.textContent = "Go to profile";
 div.appendChild(h2);
 div.appendChild(a);
 document.body.append(div);
 console.log(div);
 
  // დავალება მესამე
// #####
// #####
HTMl


<div>
      <h1 class="first">The capital of Georgia?</h1>
      <button class="tbilisi">Tbilisi</button>
      <button class="gori">gori</button>
      <button class="kutaisi">kutaisi</button>
      <button class="batumi">Batumi</button>
 </div> 
    
   JS
   
   const tbilisiBtn = document.querySelector(`.tbilisi`);
const goriBtn = document.querySelector(`.gori`);
const kutaisiBtn = document.querySelector(`.kutaisi`);
const batumiBtn = document.querySelector(`.batumi`);
tbilisiBtn.addEventListener("click", function () {
  tbilisiBtn.style.color = `green`;
  goriBtn.style.color = `red`;
  kutaisiBtn.style.color = `red`;
  batumiBtn.style.color = `red`;
 });
 goriBtn.addEventListener("click", function () {
   goriBtn.style.color = `red`;
 });
 kutaisiBtn.addEventListener("click", function () {
  kutaisiBtn.style.color = `red`;
 });
batumiBtn.addEventListener("click", function () {
   batumiBtn.style.color = `red`;});
   
   ##
// ბონუს დავალება
// ##

HTML
<h1>Score: <span id="score">0</span></h1>
 <button id="correctBtn">True</button>
 <button id="incorrectBtn">False</button>
 
 JS
 let score = 0;
 const scoreElement = document.getElementById("score");
 const correctBtn = document.getElementById("correctBtn");
 const incorrectBtn = document.getElementById("incorrectBtn");

 correctBtn.addEventListener("click", function () {
   score += 1;
   scoreElement.textContent = score;
 });
 

   
   
   
   
   
   
   
   
   
   
   
   
   
   
   
   
   
   
   
   
   
   
    
    
