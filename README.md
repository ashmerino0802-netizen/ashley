<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Mi San Valentín 💘</title>

  <style>
    body {
      font-family: "Poppins", sans-serif;
      text-align: center;
      margin: 0;
      height: 100vh;
      overflow: hidden;
      background: linear-gradient(to bottom, #ff4d6d, #ffb3c6);
      display: flex;
      justify-content: center;
      align-items: center;
      color: white;
    }

    .contenedor {
      width: 90%;
      max-width: 400px;
      background: rgba(255, 255, 255, 0.15);
      padding: 30px 20px;
      border-radius: 25px;
      box-shadow: 0 0 25px rgba(0,0,0,0.25);
      backdrop-filter: blur(10px);
      animation: aparecer 0.8s ease;
    }

    h1 {
      font-size: 28px;
      margin-bottom: 15px;
    }

    p {
      font-size: 18px;
      line-height: 1.5;
    }

    button {
      width: 85%;
      padding: 15px;
      font-size: 18px;
      border: none;
      border-radius: 20px;
      cursor: pointer;
      margin-top: 15px;
      transition: 0.3s;
      font-weight: bold;
    }

    button:hover {
      transform: scale(1.05);
    }

    .btn-si {
      background: white;
      color: #ff2e63;
    }

    .btn-si:active {
      transform: scale(0.95);
    }

    .btn-no {
      background: black;
      color: white;
      position: absolute;
      padding: 15px 25px;
      border-radius: 20px;
      font-size: 18px;
    }

    .pantalla {
      display: none;
    }

    .activa {
      display: block;
    }

    /* Animación */
    @keyframes aparecer {
      from {
        opacity: 0;
        transform: scale(0.9);
      }
      to {
        opacity: 1;
        transform: scale(1);
      }
    }

    /* Corazones flotando */
    .corazon {
      position: absolute;
      font-size: 20px;
      animation: flotar 6s linear infinite;
      opacity: 0.7;
    }

    @keyframes flotar {
      from {
        transform: translateY(100vh);
      }
      to {
        transform: translateY(-10vh);
      }
    }
  </style>
</head>

<body>

  <!-- Corazones -->
  <div class="corazon" style="left:10%; animation-delay:0s;">💖</div>
  <div class="corazon" style="left:30%; animation-delay:1s;">💘</div>
  <div class="corazon" style="left:50%; animation-delay:2s;">💕</div>
  <div class="corazon" style="left:70%; animation-delay:3s;">❤️</div>
  <div class="corazon" style="left:90%; animation-delay:4s;">💞</div>

  <!-- 💘 Pantalla 1 -->
  <div id="pantalla1" class="pantalla activa contenedor">
    <h1>Sthefany... <br>¿Quieres ser mi San Valentín?💘</h1>

    <button class="btn-si" onclick="cambiarPantalla(2)">
      Si
    </button>

    <button id="no" class="btn-no">
      No.
    </button>
  </div>

  <!-- 💕 Pantalla 2 -->
  <div id="pantalla2" class="pantalla contenedor">
    <h1>Amooor <br>¿Estás 100% segura?</h1>

    <button class="btn-si" onclick="cambiarPantalla(3)">
      Tii, mi vida 💖
    </button>

    <button class="btn-si" onclick="cambiarPantalla(3)">
      Shi, amorcito, acepto 💘
    </button>
  </div>

  <!-- ❤️ Pantalla 3 -->
  <div id="pantalla3" class="pantalla contenedor">
    <h1>Amor, ya eres mi San Valentín 💘</h1>

    <p>
      Amor, ahora ya eres mi San Valentín.<br>
      SOY MUY FELIZ Y AFORTUNADA WIWIWIIWIWIWIWWIW
       Te amo mucho mi bebé pisiosa.<br>
       Eres el amor de mi vida, TE AMO DEMASIADO, DE AQUI A LA LUNA Y DE REGRESO 💘💘💘
    </p>
  </div>

  <script>
    // Cambiar pantallas
    function cambiarPantalla(numero) {
      document.querySelectorAll(".pantalla").forEach(p => {
        p.classList.remove("activa");
      });

      document.getElementById("pantalla" + numero).classList.add("activa");
    }

    // Botón NO que se escapa
    const botonNo = document.getElementById("no");

    botonNo.addEventListener("mouseover", () => {
      const x = Math.random() * (window.innerWidth - 150);
      const y = Math.random() * (window.innerHeight - 80);

      botonNo.style.left = x + "px";
      botonNo.style.top = y + "px";
    });
  </script>

</body>
</html>
