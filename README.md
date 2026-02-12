<!DOCTYPE html>
<html>
<head>
<meta charset="UTF-8">
<title>Валентинка 💖</title>

<style>
body{
  text-align:center;
  font-family:Arial;
  background:linear-gradient(to bottom, #ffe6f0, #ffccdd);
  overflow:hidden;
}

h1{
  margin-top:100px;
}

button{
  font-size:20px;
  padding:10px 20px;
  margin:20px;
  border:none;
  border-radius:10px;
  cursor:pointer;
  position:absolute;
  transition:0.3s;
}

#yes{
  background:#ff66b2;
  color:white;
  left:40%;
  top:50%;
}

#no{
  background:#ddd;
  left:55%;
  top:50%;
}
</style>

</head>
<body>

<h1>Ты будешь моей валентинкой? 💖</h1>

<button id="yes">Да 💕</button>
<button id="no">Нет 😢</button>

<script>
let size = 20;

let yesBtn = document.getElementById("yes");
let noBtn = document.getElementById("no");

function moveNo(){
  size += 8;
  yesBtn.style.fontSize = size + "px";

  let x = Math.random() * (window.innerWidth - 100);
  let y = Math.random() * (window.innerHeight - 100);

  noBtn.style.left = x + "px";
  noBtn.style.top = y + "px";
}

noBtn.onclick = moveNo;
noBtn.onmouseover = moveNo;

yesBtn.onclick = function(){
  document.body.innerHTML = `
    <h1>Мен тоже сені любить💖</h1>
    <img src="https://media2.giphy.com/media/v1.Y2lkPTZjMDliOTUyYTdmZnJhdG1mejUzd3dkZWVmMngxN3VwdjJpcGI5ZXNoZDN4dnV1dyZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/3I8H8VvG9D7FRqd92Q/giphy.gif" alt="❤️">
  `;
}
</script>

</body>
</html>
