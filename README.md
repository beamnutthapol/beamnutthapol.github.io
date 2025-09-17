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
      opacity: 0; /* เริ่มต้นมองไม่เห็น */
      animation-name: floatUpAppear;
      animation-iteration-count: infinite;
      animation-timing-function: ease-in-out;
      animation-fill-mode: forwards;
    }

    /* อีโมจิลอยขึ้น */
    .float-heart {
      position: fixed;
      bottom: 0;
      font-size: 40px;
      opacity: 0; /* เริ่มต้นมองไม่เห็น */
      animation-name: floatUpAppear;
      animation-iteration-count: infinite;
      animation-timing-function: ease-in-out;
      animation-fill-mode: forwards;
    }

    /* Animation ให้ลอยขึ้นพร้อมปรากฏ */
    @keyframes floatUpAppear {
      0%   { transform: translateY(0) scale(0.8); opacity: 0; }
      10%  { opacity: 1; }
      100% { transform: translateY(-600px) scale(1.2); opacity: 0; }
    }

    /* คลิปวิดีโอ */
    #surpriseVideo {
      display: none;
      margin-top: 50px;
      border: 5px solid white;
      border-radius: 20px;
      box-shadow: 0 0 30px red;
    }
  </style>
</head>
<body>
  <h1>💖 Forever With You 💖</h1>

  <!-- รูปของหนูกับแฟน -->
  <img src="WIN_20250823_00_47_30_Pro.jpg" class="float-photo" style="left:10%; animation-delay:0s; animation-duration:6s;">
  <img src="IMG_20250916_215741_611.webp" class="float-photo" style="left:25%; animation-delay:2s; animation-duration:7s;">
  <img src="IMG_20250901_123521_660.webp" class="float-photo" style="left:40%; animation-delay:4s; animation-duration:6.5s;">
  <img src="IMG_20250826_195857_461.webp" class="float-photo" style="left:55%; animation-delay:1s; animation-duration:7.5s;">
  <img src="IMG20250908222630.webp" class="float-photo" style="left:70%; animation-delay:3s; animation-duration:6.2s;">
  <img src="IMG20250908222556.webp" class="float-photo" style="left:85%; animation-delay:5s; animation-duration:7.1s;">
  <img src="IMG20250907142012.webp" class="float-photo" style="left:20%; animation-delay:6s; animation-duration:6.8s;">
  <img src="IMG20250903161723.webp" class="float-photo" style="left:75%; animation-delay:8s; animation-duration:7.3s;">

  <!-- อีโมจิหัวใจ -->
  <div class="float-heart" style="left:15%; animation-delay:0s;">❤️</div>
  <div class="float-heart" style="left:35%; animation-delay:1s;">💖</div>
  <div class="float-heart" style="left:55%; animation-delay:2s;">💕</div>
  <div class="float-heart" style="left:75%; animation-delay:3s;">💘</div>

  <!-- คลิปวิดีโอ -->
  <video id="surpriseVideo" width="480" controls>
    <source src="VID20250818204341.mp4" type="video/mp4">
    Your browser does not support the video tag.
  </video>

  <script>
    // รอ 10 วิ แล้วโชว์วิดีโอ + เล่นเสียง
    setTimeout(() => {
      const vid = document.getElementById("surpriseVideo");
      vid.style.display = "block";
      vid.play();
    }, 10000);
  </script>
</body>
</html>
