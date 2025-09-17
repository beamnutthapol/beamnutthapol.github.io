<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <title>For My Love</title>
    <style>
      body {
        background: pink;
        text-align: center;
        font-family: 'Comic Sans MS', cursive, sans-serif;
      }
      h1 {
        font-size: 50px;
        color: white;
        text-shadow: 2px 2px 5px red;
        animation: glow 2s infinite alternate;
      }
      @keyframes glow {
        from { text-shadow: 0 0 10px red; }
        to { text-shadow: 0 0 30px yellow; }
      }
      .heart {
        position: fixed;
        bottom: 0;
        left: 50%;
        font-size: 30px;
        animation: float 5s infinite;
      }
      @keyframes float {
        0%   { transform: translateY(0)   scale(1); opacity: 1; }
        100% { transform: translateY(-500px) scale(1.5); opacity: 0; }
      }
    </style>
  </head>
  <body>
    <h1>💖 You are my sunshine 💖</h1>
    <div class="heart">💖</div>
    <div class="heart" style="left:40%; animation-delay:1s;">💕</div>
    <div class="heart" style="left:60%; animation-delay:2s;">💘</div>
    <div class="heart" style="left:45%; animation-delay:3s;">💓</div>
  </body>
</html>
