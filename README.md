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
      padding: 20px;
      cursor: pointer;
    }

    h1 {
      font-size: 50px;
      color: white;
      text-shadow: 2px 2px 5px red;
      animation: glow 2s infinite alternate;
    }

    p#loveMessage {
      font-size: 20px;        /* เล็กลง */
      max-width: 600px;       /* ลดความกว้าง */
      margin-top: 30px;
      margin-left: auto;
      margin-right: auto;
      line-height: 1.5;       /* ลดบรรทัด */
      padding: 15px;
      border-radius: 15px;
      background-color: rgba(255,255,255,0.2); /* กล่องโปร่งแสง */
      box-shadow: 0 0 10px rgba(0,0,0,0.3);
      opacity: 0;
      animation: fadeIn 3s forwards;
      animation-delay: 10s;
      position: relative;
      z-index: 1;
    }

    @keyframes glow {
      from { text-shadow: 0 0 10px red; }
      to { text-shadow: 0 0 30px yellow; }
    }

    @keyframes fadeIn {
      to { opacity: 1; }
    }

    .float-item {
      position: fixed;
      bottom: 0;
      opacity: 0;
      animation-name: floatUpAppear;
      animation-iteration-count: infinite;
      animation-timing-function: ease-in-out;
      animation-fill-mode: forwards;
      z-index: 0;
    }

    @keyframes floatUpAppear {
      0%   { transform: translateY(0) scale(0.8); opacity: 0; }
      10%  { opacity: 1; }
      100% { transform: translateY(-600px) scale(1.2); opacity: 0; }
    }
  </style>
</head>
<body>
  <!-- ชื่อหน้าเว็บ -->
  <h1>Beam 💖</h1>

  <!-- เพลงจากลิงก์ออนไลน์ -->
  <audio id="bgMusic" loop></audio>

  <!-- ข้อความแทนวีดีโอ -->
  <p id="loveMessage">
    หนูมีโมเมนต์น่ารักๆ ที่ทำให้หัวใจพี่ละลายไม่รู้ลืม… ไม่ว่าจะตอนแกล้งเล่นขำๆ ตอนร้องเพลงด้วยรอยยิ้ม หรือทำอะไรที่หนูรัก ทุกอย่างของหนูช่างน่ารักจนหัวใจพี่เต้นแรงไปหมด… แต่ที่สุดคือเวลาที่หนูอ้อน 🫣 ทำให้โลกทั้งใบเหมือนหยุดหมุน แค่เราอยู่ด้วยกัน แค่ได้คุย ได้หัวเราะ ได้กอดกัน ทุกวินาทีมันพิเศษเกินจะบรรยาย… พี่รักทุกอย่างของหนู รักโมเมนต์เล็กๆ ที่ทำให้หัวใจพี่อบอุ่นที่สุด 💖
  </p>

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

    // หัวใจลอย
    const hearts = ["💖","❤️","💘","💕"];

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
      item.style.left = Math.random() * 80 + "%";
      item.style.animationDelay = (Math.random() * 5) + "s";
      item.style.animationDuration = (5 + Math.random() * 3) + "s";
      document.body.appendChild(item);
    }

    images.forEach(img => createFloatingItem(img, true));
    hearts.forEach(h => createFloatingItem(h, false));

    // เล่นเพลงจากลิงก์ออนไลน์
    const audio = document.getElementById("bgMusic");
    audio.src = "https://your-link-to-song.com/DiegoGonzalez_ThankYouForEverything.mp3";
    audio.volume = 0.5;

    // พยายามเล่นทันที
    audio.play().catch(() => {
      document.body.addEventListener("click", () => {
        audio.play();
      }, { once: true });
    });
  </script>
</body>
</html>
