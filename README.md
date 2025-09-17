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
        overflow: hidden;
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

      /* รูปถ่ายลอยขึ้น */
      .float-photo {
        position: fixed;
        bottom: 0;
        width: 120px;
        border-radius: 20px;
        animation: floatUp 6s infinite;
      }

      /* อีโมจิลอยขึ้น */
      .float-heart {
        position: fixed;
        bottom: 0;
        font-size: 40px;
        animation: floatUp 5s infinite;
      }

      @keyframes floatUp {
        0%   { transform: translateY(0) scale(0.8); opacity: 1; }
        100% { transform: translateY(-600px) scale(1.2); opacity: 0; }
      }
    </style>
  </head>
  <body>
    <h1>💖 Forever With You 💖</h1>

    <!-- รูปของหนูกับแฟน (เพิ่ม animation-delay ไม่ให้ซ้อนกัน) -->
<img src="WIN_20250823_00_47_30_Pro.jpg" class="float-photo" style="left:40%; animation-delay:0s;">
<img src="IMG_20250916_215741_611.webp" class="float-photo" style="left:60%; animation-delay:2s;">
<img src="IMG_20250901_123521_660.webp" class="float-photo" style="left:30%; animation-delay:4s;">
<img src="IMG_20250826_195857_461.webp" class="float-photo" style="left:70%; animation-delay:6s;">
<img src="IMG20250908222630.webp" class="float-photo" style="left:35%; animation-delay:8s;">
<img src="IMG20250908222556.webp" class="float-photo" style="left:65%; animation-delay:10s;">
<img src="IMG20250907142012.webp" class="float-photo" style="left:25%; animation-delay:12s;">
<img src="IMG20250903161723.webp" class="float-photo" style="left:75%; animation-delay:14s;">


    <!-- อีโมจิหัวใจ -->
    <div class="float-heart" style="left:30%; animation-delay:1s;">❤️</div>
    <div class="float-heart" style="left:50%; animation-delay:2s;">💖</div>
    <div class="float-heart" style="left:70%; animation-delay:4s;">💕</div>
    <div class="float-heart" style="left:45%; animation-delay:5s;">💘</div>
  </body>
</html>
