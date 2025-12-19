<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>For You</title>
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<style>
body{
  margin:0;
  background:#f6f4f1;
  font-family: Georgia, serif;
  display:flex;
  justify-content:center;
  align-items:center;
  height:100vh;
  color:#444;
}
.card{
  max-width:600px;
  padding:40px 25px;
  text-align:center;
  animation:fade 1.5s ease;
}
button{
  margin-top:30px;
  padding:10px 28px;
  border:none;
  background:#d8b4a0;
  color:#fff;
  font-size:16px;
  border-radius:25px;
}
@keyframes fade{
  from{opacity:0;}
  to{opacity:1;}
}
</style>
</head>

<body>
<div class="card" id="card">
  <p>Hey…</p>
  <p>You don’t have to smile.</p>
  <p>I just wanted you to know I’m here.</p>
  <button onclick="next()">Continue</button>
</div>

<script>
const text=[
 "I don’t know what you’re feeling right now.",
 "You don’t have to explain anything.",
 "Take your time.",
 "Bad days don’t change how special you are.",
 "I’m not here to fix things.",
 "Just to stay.",
 "Whenever you feel ready…",
 "I’m just one message away 🤍"
];
let i=0;
function next(){
 const c=document.getElementById("card");
 c.innerHTML="<p>"+text[i]+"</p>";
 if(i<text.length-1){
  c.innerHTML+="<button onclick='next()'>Continue</button>";
 }
 i++;
}
</script>
</body>
</html>
