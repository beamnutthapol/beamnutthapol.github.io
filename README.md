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

      .float {
        position: fixed;
        bottom: 0;
        left: 50%;
        transform: translateX(-50%);
        width: 120px; /* ขนาดรูป */
        border-radius: 20px; /* มุมโค้งน่ารัก ๆ */
        animation: floatUp 6s infinite;
      }

      @keyframes floatUp {
        0%   { transform: translate(-50%, 0) scale(0.8); opacity: 1; }
        100% { transform: translate(-50%, -600px) scale(1.2); opacity: 0; }
      }
    </style>
  </head>
  <body>
    <h1>💖 Forever with You 💖</h1>

    <!-- ใส่รูปของหนูกับแฟน (แทนที่ myphoto.jpg ด้วยไฟล์จริง) -->
    <img src="myphoto.jpg" class="float" style="animation-delay:0s;">
    <img src="myphoto.jpg" class="float" style="left:40%; animation-delay:2s;">
    <img src="myphoto.jpg" class="float" style="left:60%; animation-delay:4s;">
  </body>
</html>
