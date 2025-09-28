# Love-card
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Love Card for You</title>
<style>
  body {
    margin: 0;
    font-family: 'Segoe UI', sans-serif;
    background: linear-gradient(135deg, #ff9a9e, #fad0c4, #a18cd1, #fbc2eb);
    background-size: 400% 400%;
    animation: gradientBG 15s ease infinite;
    overflow: hidden;
  }

  @keyframes gradientBG {
    0% {background-position: 0% 50%;}
    50% {background-position: 100% 50%;}
    100% {background-position: 0% 50%;}
  }

  .container {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    height: 100vh;
    text-align: center;
    color: #fff;
    text-shadow: 2px 2px 8px rgba(0,0,0,0.4);
    padding: 20px;
  }

  .teddy {
    font-size: 100px;
    margin-bottom: 20px;
  }

  h1 {
    font-size: 36px;
    margin-bottom: 10px;
  }

  p {
    font-size: 22px;
    max-width: 600px;
    line-height: 1.5;
  }

  .heart {
    position: absolute;
    color: #ff6b81;
    font-size: 24px;
    animation: floatHeart linear infinite;
  }

  @keyframes floatHeart {
    0% {transform: translateY(0) scale(1);}
    50% {transform: translateY(-100px) scale(1.2);}
    100% {transform: translateY(-200px) scale(1);}
  }
</style>
</head>
<body>
<div class="container">
  <div class="teddy">🧸</div>
  <h1>Hey Sweetheart ❤️</h1>
  <p>You mean a lot to me. Just talking to you or thinking about you makes my day brighter. I'm really happy that you're in my life. You're my closest friend and the person I feel most comfortable with. I feel lucky to have you. I'll always be there for you. 🥰💖</p>
</div>

<!-- Floating hearts -->
<script>
function createHeart() {
  const heart = document.createElement('div');
  heart.className = 'heart';
  heart.innerText = '❤️';
  heart.style.left = Math.random() * window.innerWidth + 'px';
  heart.style.fontSize = (20 + Math.random() * 20) + 'px';
  heart.style.animationDuration = (4 + Math.random() * 3) + 's';
  document.body.appendChild(heart);

  setTimeout(() => {
    heart.remove();
  }, 7000);
}

// Create hearts continuously
setInterval(createHeart, 400);
</script>
</body>
</html>
