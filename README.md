# SCAM
SCAMMM!!!
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>💖 Valentine Surprise 💖</title>
  <style>
    body {
      margin: 0;
      height: 100vh;
      background: linear-gradient(135deg, #ff758c, #ff7eb3);
      display: flex;
      align-items: center;
      justify-content: center;
      font-family: 'Segoe UI', sans-serif;
      overflow: hidden;
    }

    .card {
      background: white;
      padding: 35px;
      border-radius: 25px;
      text-align: center;
      box-shadow: 0 20px 40px rgba(0,0,0,0.25);
      max-width: 400px;
      animation: pop 1s ease;
      z-index: 2;
    }

    h1 {
      color: #ff2e63;
      font-size: 1.9rem;
    }

    p {
      color: #555;
      margin-bottom: 15px;
    }

    .heart {
      font-size: 3rem;
      animation: beat 1.5s infinite;
    }

    img {
      width: 100%;
      border-radius: 15px;
      margin: 15px 0;
    }

    .buttons {
      margin-top: 15px;
    }

    button {
      padding: 12px 25px;
      border-radius: 30px;
      border: none;
      font-size: 1rem;
      cursor: pointer;
      margin: 5px;
      transition: transform 0.2s;
    }

    #yes {
      background: #ff2e63;
      color: white;
    }

    #yes:hover {
      transform: scale(1.1);
    }

    #no {
      background: #ddd;
      color: #333;
      position: relative;
    }

    @keyframes beat {
      0%,100% { transform: scale(1); }
      50% { transform: scale(1.25); }
    }

    @keyframes pop {
      from { transform: scale(0.5); opacity: 0; }
      to { transform: scale(1); opacity: 1; }
    }

    .floating-heart {
      position: absolute;
      font-size: 20px;
      color: rgba(255, 255, 255, 0.8);
      animation: float 6s linear infinite;
    }

    @keyframes float {
      from { transform: translateY(100vh); opacity: 1; }
      to { transform: translateY(-10vh); opacity: 0; }
    }

    .message {
      display: none;
      font-size: 1.4rem;
      color: #ff2e63;
      margin-top: 15px;
    }
  </style>
</head>
<body>

  <div class="card" id="card">
    <div class="heart">❤️</div>
    <h1>Will you be my Valentine,<br>Marina Haddad?</h1>
    <p>You make my heart smile every single day.</p>

    <img src="https://media.giphy.com/media/l4pTdcifPZLpDjL1e/giphy.gif" alt="cute love gif">

    <div class="buttons">
      <button id="yes">💌 YES</button>
      <button id="no">🙈 NO</button>
    </div>

    <div class="message" id="message">
      💖 Yay!! I knew it 💖<br>
      You’re my forever Valentine 😘
    </div>
  </div>

  <script>
    // Floating hearts
    function createHeart() {
      const heart = document.createElement("div");
      heart.className = "floating-heart";
      heart.innerHTML = "❤️";
      heart.style.left = Math.random() * 100 + "vw";
      heart.style.fontSize = Math.random() * 25 + 15 + "px";
      document.body.appendChild(heart);
      setTimeout(() => heart.remove(), 6000);
    }
    setInterval(createHeart, 250);

    // NO button runs away
    const noBtn = document.getElementById("no");
    noBtn.addEventListener("mouseover", () => {
      noBtn.style.left = Math.random() * 200 - 100 + "px";
      noBtn.style.top = Math.random() * 200 - 100 + "px";
    });

    // YES button celebration
    document.getElementById("yes").onclick = () => {
      document.getElementById("message").style.display = "block";
    };
  </script>

</body>
</html>
