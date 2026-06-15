<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Ultimate Gym Guide</title>

<style>
*{
margin:0;
padding:0;
box-sizing:border-box;
font-family:Arial, sans-serif;
}

body{
background:#0d1117;
color:white;
line-height:1.6;
}

header{
background:linear-gradient(135deg,#ff4b2b,#ff416c);
padding:20px;
text-align:center;
}

header h1{
font-size:3rem;
}

nav{
background:#161b22;
padding:15px;
text-align:center;
position:sticky;
top:0;
}

nav a{
color:white;
text-decoration:none;
margin:15px;
font-weight:bold;
}

.hero{
height:80vh;
display:flex;
justify-content:center;
align-items:center;
text-align:center;
padding:20px;
background:linear-gradient(rgba(0,0,0,.6),rgba(0,0,0,.6)),
url('https://images.unsplash.com/photo-1517836357463-d25dfeac3438');
background-size:cover;
background-position:center;
}

.hero h2{
font-size:3rem;
}

section{
padding:60px 20px;
max-width:1200px;
margin:auto;
}

.card-container{
display:grid;
grid-template-columns:repeat(auto-fit,minmax(250px,1fr));
gap:20px;
}

.card{
background:#161b22;
padding:20px;
border-radius:15px;
transition:.3s;
}

.card:hover{
transform:translateY(-10px);
}

.card h3{
color:#ff416c;
margin-bottom:10px;
}

table{
width:100%;
border-collapse:collapse;
margin-top:20px;
}

table th,table td{
border:1px solid #444;
padding:10px;
text-align:center;
}

table th{
background:#ff416c;
}

.calculator{
background:#161b22;
padding:30px;
border-radius:15px;
max-width:500px;
margin:auto;
}

input{
width:100%;
padding:12px;
margin:10px 0;
border:none;
border-radius:8px;
}

button{
background:#ff416c;
color:white;
border:none;
padding:12px 20px;
border-radius:8px;
cursor:pointer;
}

button:hover{
background:#ff4b2b;
}

#result{
margin-top:20px;
font-size:20px;
}

footer{
background:#161b22;
padding:20px;
text-align:center;
margin-top:50px;
}
</style>
</head>
<body>

<header>
<h1>💪 Ultimate Gym Guide</h1>
<p>Build Muscle | Lose Fat | Stay Healthy</p>
</header>

<nav>
<a href="#about">About</a>
<a href="#workout">Workout</a>
<a href="#diet">Diet</a>
<a href="#bmi">BMI</a>
<a href="#tips">Tips</a>
</nav>

<div class="hero">
<div>
<h2>Transform Your Body Naturally</h2>
<p>Learn everything about fitness, workouts and nutrition.</p>
</div>
</div>

<section id="about">
<h2>🏋 About Gym</h2>
<p>
Gym helps improve strength, stamina, flexibility and overall health.
Regular exercise reduces stress and keeps the body fit.
</p>
</section>

<section id="workout">
<h2>🔥 Workout Plans</h2>

<div class="card-container">

<div class="card">
<h3>Chest Day</h3>
<p>
Bench Press - 4 Sets<br>
Incline Press - 4 Sets<br>
Push Ups - 3 Sets
</p>
</div>

<div class="card">
<h3>Back Day</h3>
<p>
Pull Ups - 4 Sets<br>
Lat Pulldown - 4 Sets<br>
Deadlift - 4 Sets
</p>
</div>

<div class="card">
<h3>Leg Day</h3>
<p>
Squats - 4 Sets<br>
Leg Press - 4 Sets<br>
Lunges - 3 Sets
</p>
</div>

<div class="card">
<h3>Shoulder Day</h3>
<p>
Shoulder Press - 4 Sets<br>
Lateral Raise - 3 Sets<br>
Front Raise - 3 Sets
</p>
</div>

</div>
</section>

<section id="diet">
<h2>🥗 Healthy Diet Plan</h2>

<table>
<tr>
<th>Meal</th>
<th>Food</th>
</tr>

<tr>
<td>Breakfast</td>
<td>Oats, Eggs, Banana</td>
</tr>

<tr>
<td>Lunch</td>
<td>Rice, Chicken, Vegetables</td>
</tr>

<tr>
<td>Evening</td>
<td>Fruit & Nuts</td>
</tr>

<tr>
<td>Dinner</td>
<td>Paneer/Fish + Salad</td>
</tr>

</table>
</section>

<section id="bmi">
<h2>📊 BMI Calculator</h2>

<div class="calculator">

<input type="number" id="weight" placeholder="Weight (kg)">
<input type="number" id="height" placeholder="Height (cm)">

<button onclick="calculateBMI()">Calculate BMI</button>

<div id="result"></div>

</div>
</section>

<section id="tips">
<h2>⭐ Fitness Tips</h2>

<div class="card-container">

<div class="card">
<h3>Drink Water</h3>
<p>Drink 3-4 liters of water daily.</p>
</div>

<div class="card">
<h3>Sleep</h3>
<p>Sleep 7-9 hours every night.</p>
</div>

<div class="card">
<h3>Protein</h3>
<p>Eat protein-rich foods regularly.</p>
</div>

<div class="card">
<h3>Consistency</h3>
<p>Workout regularly and stay disciplined.</p>
</div>

</div>
</section>

<footer>
<h3>Ultimate Gym Guide © 2026</h3>
<p>Stay Strong • Stay Healthy • Stay Motivated</p>
</footer>

<script>
function calculateBMI(){

let weight =
document.getElementById("weight").value;

let height =
document.getElementById("height").value/100;

let bmi =
(weight/(height*height)).toFixed(1);

let status="";

if(bmi<18.5){
status="Underweight";
}
else if(bmi<25){
status="Normal";
}
else if(bmi<30){
status="Overweight";
}
else{
status="Obese";
}

document.getElementById("result").innerHTML=
"Your BMI: "+bmi+"<br>Status: "+status;
}
</script>

</body>
</html>
