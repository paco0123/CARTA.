<html lang="es">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Para Mi Amor 💖</title>
  <link href="https://fonts.googleapis.com/css2?family=Great+Vibes&display=swap" rel="stylesheet">
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    html, body {
      height: 100%;
      font-family: 'Great Vibes', cursive;
      background: linear-gradient(135deg, #ffc0cb, #ffe4e1);
      overflow-x: hidden;
    }

    .page {
      width: 100vw;
      min-height: 100vh;
      position: absolute;
      top: 0;
      left: 100vw;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      text-align: center;
      padding: 2rem;
      transition: left 1s ease-in-out;
    }

    .page.active {
      left: 0;
    }

    h1 {
      font-size: 3rem;
      color: #c71585;
      text-shadow: 2px 2px 5px #fff;
    }

    p {
      font-size: 1.5rem;
      color: #800040;
      max-width: 600px;
      margin-top: 1rem;
    }

    button {
      margin-top: 2rem;
      padding: 1rem 2rem;
      font-size: 1rem;
      background: #ff69b4;
      color: white;
      border: none;
      border-radius: 20px;
      cursor: pointer;
      box-shadow: 0 4px 10px rgba(0,0,0,0.2);
      transition: background 0.3s;
    }

    button:hover {
      background: #ff1493;
    }

    .heart {
      position: absolute;
      width: 20px;
      height: 20px;
      background: red;
      transform: rotate(45deg);
      animation: float 10s infinite ease-in;
      opacity: 0.6;
    }

    .heart::before, .heart::after {
      content: '';
      position: absolute;
      width: 20px;
      height: 20px;
      background: red;
      border-radius: 50%;
    }

    .heart::before {
      top: -10px;
      left: 0;
    }

    .heart::after {
      top: 0;
      left: -10px;
    }

    @keyframes float {
      0% {
        transform: translateY(100vh) rotate(45deg);
      }
      100% {
        transform: translateY(-10vh) rotate(45deg);
      }
    }

    /* 👇 ADAPTACIÓN A CELULARES */
    @media (max-width: 600px) {
      h1 {
        font-size: 2rem;
      }

      p {
        font-size: 1.2rem;
      }

      button {
        font-size: 0.9rem;
        padding: 0.8rem 1.5rem;
      }

      .page {
        padding: 1rem;
      }
    }
  </style>
</head>
<body>

  <!-- Páginas -->
  <div class="page active" id="page1">
    <h1>Hola mi niña 💌</h1>
    <p>Hoy quiero regalarte algo especial… una pequeña carta hecha con todo mi corazón, solo para ti.</p>
    <button onclick="nextPage()">Ver más</button>
  </div>

  <div class="page" id="page2">
    <h1>Gracias por existir 💖</h1>
    <p>Gracias por hacerme feliz, por aguantarme y simplemente gracias por aparecer en mi vida, me encantas como eres, me encanta tu forma de ser, me encantan tus defectos que te hacen una persona tan especial y única, me encanta tu sonrisa, me encantan esos ojitos tan hermosos que tienes, pero más me encantas tú, eres tú la que me vuelve loco cada día y gracias por escogerme cada día.❤‍🩹💞</p>
    <button onclick="nextPage()">Siguiente</button>
  </div>

  <div class="page" id="page3">
    <h1>Siempre juntos 💘</h1>
    <p>No miento cuando enserio te digo que te amo, eres esa niña que tanto deseaba que llegara y quiero verte triunfar porque sé lo mucho que te esfuerzas para salir adelante. Estoy orgulloso de ti. Soy tu gran admirador y tu fan número 1. Prometo cuidarte, respetarte y hacerte sentir amada todos los días de nuestras vidas. Eres mi todo.🖤</p>
    <button onclick="nextPage()">Última</button>
  </div>

  <div class="page" id="page4">
    <h1>Te amo 💞</h1>
    <p>Siempre te amaré, más allá del tiempo y de la vida. Gracias por ser tú. A mi corazón le agrada estar contigo, eres su lugar favorito. Quiero que seas mi último amor. Nunca olvides que este loco te ama inefablemente y mi amor por ti es sempiterno. TE AMO❤.</p>
    <button onclick="restart()">Volver a leer</button>
  </div>

  <!-- Corazones flotantes -->
  <script>
    const totalHearts = 35;
    for (let i = 0; i < totalHearts; i++) {
      const heart = document.createElement('div');
      heart.className = 'heart';
      heart.style.left = Math.random() * 100 + 'vw';
      heart.style.animationDuration = (5 + Math.random() * 5) + 's';
      heart.style.opacity = Math.random();
      document.body.appendChild(heart);
    }

    let currentPage = 1;
    function nextPage() {
      document.getElementById(page${currentPage}).classList.remove('active');
      currentPage++;
      document.getElementById(page${currentPage}).classList.add('active');
    }

    function restart() {
      document.getElementById(page${currentPage}).classList.remove('active');
      currentPage = 1;
      document.getElementById(page${currentPage}).classList.add('active');
    }
  </script>
</body>
</html>
