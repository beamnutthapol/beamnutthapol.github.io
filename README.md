<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <title>Hello Page</title>
    <style>
      .animated-text {
        font-size: 40px;
        font-weight: bold;
        color: green;
        animation: moveText 3s linear infinite alternate;
      }

      @keyframes moveText {
        0%   { transform: translateX(0);   color: red;   }
        50%  { transform: translateX(100px); color: blue; }
        100% { transform: translateX(0);   color: green; }
      }
    </style>
  </head>
  <body>
    <h1 class="animated-text">Hello Nutthapol Bovaree 🌈✨</h1>
  </body>
</html>
