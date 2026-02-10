# Mi-enamorada
<!doctype html>
<html lang="en">

<head>
<meta charset="UTF-8">
<title>My Surprise 💖</title>

<style>
body {
  margin: 0;
  height: 100vh;
  background: black;
  display: flex;
  justify-content: center;
  align-items: center;
  font-family: 'Courier New', monospace;
  color: white;
}

.container {
  text-align: center;
}

#text {
  font-size: 18px;
  line-height: 1.8;
  white-space: pre-line;
  min-height: 150px;
}

button {
  margin-top: 25px;
  padding: 10px 25px;
  font-size: 14px;
  border: none;
  border-radius: 5px;
  cursor: pointer;
  background: #f2f2f2;
  color: black;
  display: none;
}

button:hover {
  background: #ddd;
}

.hearts {
  margin-top: 15px;
  font-size: 18px;
}
</style>
</head>

<body>

<div class="container">
  <div id="text"></div>

  <div class="hearts">
    ( ˘ ³˘)♥ ( ˘ ³˘)♥ ( ˘ ³˘)♥
  </div>

  <button id="btn">Continue</button>
</div>

<script>
const message = [
  "💌 Hey my love, Jane 🤍",
  "",
  "I have a surprise for you...",
  "",
  "So I made you this computer program 💻✨",
  "",
  "Recuerda que siempre te amo, eres mi vida entera 🤍"
];

let i = 0;
let j = 0;
const speed = 50;
const textDiv = document.getElementById("text");
const button = document.getElementById("btn");

function typeWriter() {
  if (i < message.length) {
    if (j < message[i].length) {
      textDiv.innerHTML += message[i].charAt(j);
      j++;
      setTimeout(typeWriter, speed);
    } else {
      textDiv.innerHTML += "<br>";
      j = 0;
      i++;
      setTimeout(typeWriter, speed);
    }
  } else {
    button.style.display = "inline-block";
  }
}

typeWriter();

button.onclick = () => {
  alert("💖 Te amo 💖");
};
</script>

</body>
</html>

