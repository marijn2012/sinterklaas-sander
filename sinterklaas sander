<!DOCTYPE html>
<html lang="nl">
<head>
  <meta charset="UTF-8">
  <title>Sinterklaas Code Zoeker</title>

  <style>
    body {
      font-family: 'Arial', sans-serif;
      background-color: #007BFF; /* helder blauw */
      color: #fff4d6;
      text-align: center;
      padding: 40px;
    }

    h1 {
      font-size: 2.5rem;
      margin-bottom: 20px;
      text-shadow: 2px 2px #000;
    }

    .card {
      background: rgba(0, 0, 0, 0.5);
      border: 2px solid gold;
      border-radius: 12px;
      padding: 20px;
      max-width: 400px;
      margin: 0 auto;
      box-shadow: 0 0 15px gold;
    }

    input, button {
      font-size: 1.2rem;
      padding: 10px;
      margin-top: 10px;
      border-radius: 8px;
      border: none;
    }

    input {
      width: 80%;
    }

    button {
      background: gold;
      color: #8b0000;
      font-weight: bold;
      cursor: pointer;
    }

    #result {
      margin-top: 20px;
      font-size: 1.4rem;
      font-weight: bold;
    }

    .icons {
      font-size: 2rem;
      margin-bottom: 10px;
    }

    @keyframes confetti {
      0% { transform: translateY(-100vh); opacity: 1; }
      100% { transform: translateY(100vh); opacity: 0; }
    }

    .confetti {
      position: fixed;
      top: -10px;
      width: 10px;
      height: 10px;
      background: gold;
      animation: confetti 3s linear infinite;
      z-index: 9999;
    }
  </style>
</head>
<body>

  <audio id="goodSound">
    <source src="https://www.soundjay.com/buttons/sounds/button-3.mp3" type="audio/mpeg">
  </audio>

  <div class="icons">🎁🎅✨</div>
  <h1>Sinterklaas Code Zoeker</h1>

  <div class="card">
    <p>Vul je geheime code in:</p>
    <input id="codeInput" type="text">
    <br>
    <button onclick="zoekLocatie()">Zoek locatie</button>

    <div id="result"></div>
  </div>

  <script>
    const locaties = {
      "sander": "je kamer sander",
      "1234": "kamer marijn",
      "1111": "kamer ruben",
      "2222": "kamer papa en mama",
      "0624": "de schuur"
    };

    function zoekLocatie() {
      const code = document.getElementById("codeInput").value.trim();
      const resultDiv = document.getElementById("result");
      const sound = document.getElementById("goodSound");

      if (locaties[code]) {
        sound.play();
        resultDiv.textContent = "🎅 Ga naar: " + locaties[code] + " 🎁";

        if (code === "0624") {
          startFinaleAnimatie();
        }

      } else {
        resultDiv.textContent = "❌ Onbekende code. Probeer het opnieuw.";
      }
    }

    function startFinaleAnimatie() {
      for (let i = 0; i < 50; i++) {
        const confetti = document.createElement("div");
        confetti.classList.add("confetti");
        confetti.style.left = Math.random() * 100 + "vw";
        confetti.style.backgroundColor = ["gold", "red", "white"][Math.floor(Math.random()*3)];
        confetti.style.animationDuration = (2 + Math.random() * 3) + "s";
        document.body.appendChild(confetti);

        setTimeout(() => confetti.remove(), 5000);
      }
    }
  </script>

</body>
</html>
