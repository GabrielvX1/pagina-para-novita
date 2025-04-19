<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <title>Para mi Novita 💖</title>
  <style>
    body {
      margin: 0;
      padding: 0;
      background: linear-gradient(to right, #ff9a9e, #fad0c4);
      font-family: 'Segoe UI', sans-serif;
      overflow: hidden;
    }

    .container {
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
      text-align: center;
      padding: 20px;
    }

    .card {
      background: rgba(255, 255, 255, 0.9);
      padding: 40px;
      border-radius: 25px;
      box-shadow: 0 20px 40px rgba(0,0,0,0.2);
      max-width: 700px;
      position: relative;
      z-index: 2;
    }

    h1 {
      font-size: 3em;
      color: #e91e63;
      margin-bottom: 20px;
    }

    p {
      font-size: 1.3em;
      color: #555;
      line-height: 1.6em;
    }

    .corazones {
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      pointer-events: none;
      overflow: hidden;
      z-index: 1;
    }

    .corazon {
      position: absolute;
      width: 30px;
      height: 30px;
      background: url('https://upload.wikimedia.org/wikipedia/commons/thumb/f/f0/Heart_corazón.svg/1024px-Heart_corazón.svg.png') no-repeat center;
      background-size: contain;
      animation: flotar 8s infinite;
      opacity: 0.6;
    }

    @keyframes flotar {
      0% {
        transform: translateY(100vh) scale(0.5) rotate(0deg);
        opacity: 0;
      }
      50% {
        opacity: 1;
      }
      100% {
        transform: translateY(-10vh) scale(1.2) rotate(360deg);
        opacity: 0;
      }
    }
  </style>
</head>
<body>

<div class="corazones" id="corazones"></div>

<div class="container">
  <div class="card">
    <h1>Hola Novita 🌸</h1>
    <p>
      Eres una persona increíble, llena de luz y alegría, y cada día me contagias esa energía hermosa que llevas dentro. ❤️<br><br>
      Gracias por hacerme sentir como el chico más afortunado del mundo solo con tu presencia, tus palabras, tus locuras. <br><br>
      Tu voz tiene la magia de calmar mis días, como si me regalaras años de vida cada vez que hablas. <br><br>
      No puedo dejar de agradecerte por ser tú, por estar ahí, por tu risa, tus abrazos, tus silencios y tus “te quiero”.<br><br>
      ¡Te amo mucho, mi Novita, mi Angie hermosa! 😍<br><br>
      Siempre voy a estar acompañándote, sosteniéndote, ayudándote a calmar cada pensamiento, cada tormenta interna. <br><br>
      Eres la mejor, única e irrepetible. ✨<br><br>
      Jamas olvides lo mucho que vales y todo lo que significas para mí. 💖<br><br>
      Te mereces lo mejor del mundo, hoy, mañana y siempre. 🌈<br><br>
      Con todo mi amor,<br>
      Tu principito 💌
    </p>
  </div>
</div>

<script>
  const corazones = document.getElementById('corazones');

  function crearCorazon() {
    const corazon = document.createElement('div');
    corazon.classList.add('corazon');
    corazon.style.left = Math.random() * 100 + 'vw';
    corazon.style.animationDuration = (6 + Math.random() * 4) + 's';
    corazones.appendChild(corazon);
    setTimeout(() => {
      corazon.remove();
    }, 10000);
  }

  setInterval(crearCorazon, 300);
</script>

</body>
</html>

