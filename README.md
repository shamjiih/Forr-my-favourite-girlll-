<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>Happy New Year 🤍</title>
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<style>
body{
  margin:0;
  height:100vh;
  display:flex;
  justify-content:center;
  align-items:center;
  background: linear-gradient(135deg, #fdfbfb, #ebedee);
  font-family: 'Segoe UI', sans-serif;
  color:#444;
}

.card{
  background: rgba(255,255,255,0.95);
  padding:45px 35px;
  border-radius:22px;
  max-width:440px;
  text-align:center;
  box-shadow: 0 20px 40px rgba(0,0,0,0.12);
  animation: fadeIn 2s ease;
}

h1{
  font-weight:500;
  margin-top:0;
}

p{
  font-size:16px;
  line-height:1.9;
  margin-bottom:18px;
}

button{
  margin-top:25px;
  padding:12px 34px;
  border:none;
  border-radius:30px;
  background:#c8b6a6;
  color:#fff;
  font-size:15px;
  cursor:pointer;
}

button:hover{
  background:#b7a795;
}

@keyframes fadeIn{
  from{opacity:0;}
  to{opacity:1;}
}
</style>
</head>

<body>

<div class="card" id="card">
  <h1>Happy New Year 🎉</h1>
  <p>
    A brand new year is here,<br>
    and with it, fresh moments, soft mornings,<br>
    and new reasons to smile.
  </p>
  <button onclick="next()">Continue</button>
</div>

<script>
const messages = [
  "I hope this year brings you calm days and light hearts.",
  "More laughter, more peace, and moments that feel right.",
  "May you find happiness in small things and comfort in big dreams.",
  "Leave behind what was heavy, and carry forward what matters.",
  "This year, choose yourself a little more.",
  "And remember — you deserve good things.",
  "Wishing you a beautiful, gentle year ahead 🤍"
];

let i = 0;

function next(){
  const card = document.getElementById("card");
  card.innerHTML = "<p>"+messages[i]+"</p>";
  if(i < messages.length - 1){
    card.innerHTML += "<button onclick='next()'>Continue</button>";
  }
  i++;
}
</script>

</body>
</html>
