<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>For Sunita ❤️</title>
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <style>
    body {
      margin: 0;
      font-family: 'Segoe UI', sans-serif;
      background: linear-gradient(135deg, #ff758c, #ff7eb3);
      color: white;
      height: 100vh;
      display: flex;
      align-items: center;
      justify-content: center;
      text-align: center;
      overflow: hidden;
    }
    .card {
      max-width: 340px;
      padding: 25px;
      animation: fadeIn 2s ease;
    }
    h1 {
      font-size: 28px;
      margin-bottom: 10px;
    }
    .quote {
      font-size: 18px;
      margin: 20px 0;
      opacity: 0;
      animation: slideUp 2s ease forwards;
      animation-delay: 1s;
    }
    button {
      background: white;
      color: #ff4d6d;
      border: none;
      padding: 12px 22px;
      font-size: 16px;
      border-radius: 30px;
      cursor: pointer;
      margin-top: 15px;
      box-shadow: 0 5px 15px rgba(0,0,0,0.2);
    }
    button:hover {
      transform: scale(1.05);
    }
    .hidden {
      display: none;
    }
    @keyframes fadeIn {
      from { opacity: 0; }
      to { opacity: 1; }
    }
    @keyframes slideUp {
      from { transform: translateY(20px); opacity: 0; }
      to { transform: translateY(0); opacity: 1; }
    }
    .heart {
      position: absolute;
      font-size: 20px;
      animation: float 6s infinite;
      opacity: 0.7;
    }
    @keyframes float {
      0% { transform: translateY(0); }
      100% { transform: translateY(-600px); }
    }
  </style>
</head>
<body>

<div class="card" id="step1">
  <h1>💖 Hi Sunita 💖</h1>
  <div class="quote">
    "Some names feel like home…<br> and yours is one of them."
  </div>
  <button onclick="playSong()">Play Song 🎶</button>
</div>

<div class="card hidden" id="step2">
  <h1>🌹 Happy Valentine’s Day 🌹</h1>
  <p style="font-size:17px;">
    Tumhari smile meri favourite habit ban chuki hai 😊<br><br>
    Agar Valentine ka matlab koi hota,<br>
    toh shayad woh <b>tum</b> hoti ❤️
  </p>
</div>

<audio id="song">
  <source src="https://www.soundhelix.com/examples/mp3/SoundHelix-Song-1.mp3" type="audio/mpeg">
</audio>

<script>
  function playSong() {
    document.getElementById("song").play();
    document.getElementById("step1").classList.add("hidden");
    document.getElementById("step2").classList.remove("hidden");
  }

  // floating hearts
  for (let i = 0; i < 20; i++) {
    let heart = document.createElement("div");
    heart.className = "heart";
    heart.innerHTML = "❤️";
    heart.style.left = Math.random() * 100 + "vw";
    heart.style.bottom = "-20px";
    heart.style.animationDuration = (4 + Math.random() * 4) + "s";
    document.body.appendChild(heart);
  }
</script>

</body>
</html>
