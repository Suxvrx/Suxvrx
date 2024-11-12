<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Corazón Animado</title>
  <style>
    .heart {
      width: 100px;
      height: 100px;
      position: relative;
      background-color: red;
      transform: rotate(45deg);
      animation: heartbeat 1s infinite;
    }

    .heart::before,
    .heart::after {
      content: "";
      width: 100px;
      height: 100px;
      background-color: red;
      border-radius: 50%;
      position: absolute;
    }

    .heart::before {
      top: -50px;
      left: 0;
    }

    .heart::after {
      left: 50px;
      top: 0;
    }

    @keyframes heartbeat {
      0%, 100% {
        transform: scale(1) rotate(45deg);
      }
      50% {
        transform: scale(1.2) rotate(45deg);
      }
    }
  </style>
</head>
<body>
  <div class="heart"></div>
</body>
</html> 
