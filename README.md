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

    .float-item {
      position: fixed; /* สำคัญมาก! */
      bottom: 0;
      opacity: 0;
      animation-name: floatUpAppear;
      animation-iteration-count: infinite;
      animation-timing-function: ease-in-out;
      animation-fill-mode: forwards;
    }

    @keyframes floatUpAppear {
      0%   { transform: translateY(0) scale(0.8); opacity: 0; }
      10%  { opacity: 1; }
      100% { transform: translateY(-600px) scale(1.2); opacity: 0; }
    }

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

  <video id="surpriseVideo" width="480" controls>
    <source src="myvideo.mp4" type="video/mp4">
    Your browser does not support the video tag.
  </video>

  <script>
    const images = [
      "WIN_20250823_00_47_30_Pro.jpg",
      "IMG_20250916_215741_611.webp",
      "IMG_20250901_123521_660.webp",
      "IMG_20250826_195857_461.webp",
      "IMG20250908222630.webp",
      "IMG20250908222556.webp",
      "IMG20250907142012.webp",
      "IMG20250903161723.webp"
    ];

    const hearts = ["❤️","💖","💕","💘"];

    function createFloatingItem(content, isImage = true) {
      const item = isImage ? document.createElement("img") : document.createElement("div");

      if (isImage) {
        item.src = content;
        item.style.width = "120px";
        item.style.borderRadius = "20px";
      } else {
        item.innerText = content;
        item.style.fontSize = "40px";
      }

      item.classList.add("float-item");

      // สุ่มตำแหน่ง horizontal
      item.style.left = Math.random() * 80 + "%";

      // สุ่ม delay และ duration
      item.style.animationDelay = (Math.random() * 5) + "s";
      item.style.animationDuration = (5 + Math.random() * 3) + "s";

      document.body.appendChild(item);
    }

    // สร้างรูป
    images.forEach(img => createFloatingItem(img, true));

    // สร้างหัวใจ
    hearts.forEach(h => createFloatingItem(h, false));

    // คลิปวิดีโอหลัง 10 วิ
    setTimeout(() => {
      const vid = document.getElementById("surpriseVideo");
      vid.style.display = "block";
      vid.play();
    }, 10000);
  </script>
</body>
</html>
