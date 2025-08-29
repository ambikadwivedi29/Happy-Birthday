<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Happy Birthday</title>
  <style>
    body {
      margin: 0;
      height: 100vh;
      display: flex;
      justify-content: center;
      align-items: center;
      flex-direction: column;
      background: linear-gradient(to top, #ffe6f0, #e6f7ff);
      overflow: hidden;
      font-family: 'Comic Sans MS', cursive;
    }

    h1 {
      font-size: 3rem;
      color: #ff4da6;
      text-shadow: 0 0 10px #ff99cc, 0 0 20px #ff66b2;
      animation: glow 2s infinite alternate;
    }

    @keyframes glow {
      from { text-shadow: 0 0 5px #ff99cc, 0 0 10px #ff66b2; }
      to { text-shadow: 0 0 20px #ff3399, 0 0 30px #ff0066; }
    }

    .balloon {
      position: absolute;
      bottom: -100px;
      width: 40px;
      height: 60px;
      background: pink;
      border-radius: 50% 50% 50% 50% / 60% 60% 40% 40%;
      animation: floatUp 8s linear infinite;
    }

    @keyframes floatUp {
      from { transform: translateY(100vh); }
      to { transform: translateY(-120vh); }
    }

    .balloon::after {
      content: '';
      position: absolute;
      bottom: -20px;
      left: 50%;
      width: 2px;
      height: 20px;
      background: #555;
    }

    .heart {
      position: absolute;
      width: 20px;
      height: 20px;
      background: pink;
      transform: rotate(45deg);
      animation: floatHeart 6s ease-in-out infinite;
    }

    .heart::before,
    .heart::after {
      content: '';
      position: absolute;
      width: 20px;
      height: 20px;
      background: pink;
      border-radius: 50%;
    }

    .heart::before { top: -10px; left: 0; }
    .heart::after { left: -10px; top: 0; }

    @keyframes floatHeart {
      0% { transform: translateY(100vh) scale(0.8) rotate(45deg); opacity: 0; }
      50% { opacity: 1; }
      100% { transform: translateY(-100vh) scale(1.2) rotate(45deg); opacity: 0; }
    }
  </style>
</head>
<body>
  <h1>🎂 Happy Birthday, My Love 💖</h1>

  <!-- Balloons -->
  <div class="balloon" style="left: 20%; background: #ff99cc; animation-delay: 0s;"></div>
  <div class="balloon" style="left: 50%; background: #99ccff; animation-delay: 2s;"></div>
  <div class="balloon" style="left: 80%; background: #ffcc99; animation-delay: 4s;"></div>

  <!-- Hearts -->
  <div class="heart" style="left: 30%; animation-delay: 1s;"></div>
  <div class="heart" style="left: 60%; animation-delay: 3s;"></div>
  <div class="heart" style="left: 90%; animation-delay: 5s;"></div>
</body>
</html>
